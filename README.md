# Chatbot_especialista_em_receitas
Um chatbot criado para responder perguntas relacionadas ao ramo da culinária. Ele te ensina receitas, dá dicas para a receita, substitui ingredientes. Tudo isso enquanto interpreta o famoso Chef, Gordon Ramsay. 

# ================================
# 1. INSTALAR BIBLIOTECAS
# ================================

# Instala dependências necessárias
!pip install langchain langchain-groq requests beautifulsoup4 -q


# ================================
# 2. IMPORTAR BIBLIOTECAS
# ================================

import os  # Para usar variáveis de ambiente
import requests  # Para acessar páginas da internet
from bs4 import BeautifulSoup  # Para extrair dados do HTML
from langchain_groq import ChatGroq  # Para usar o modelo da Groq


# ================================
# 3. CONFIGURAR API KEY
# ================================

# Defina sua chave da Groq aqui
os.environ['GROQ_API_KEY'] = "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"


# ================================
# 4. INICIALIZAR O MODELO
# ================================

# Cria o modelo de linguagem
llm = ChatGroq(
    model_name="llama-3.3-70b-versatile",  # Modelo solicitado
    temperature=0.7  # Nível de criatividade
)


# ================================
# 5. FUNÇÃO DE BUSCA (SCRAPING MELHORADO)
# ================================

def buscar_receita(consulta):
    # URL de busca no site
    url = f"https://www.receiteria.com.br/?s={consulta}"

    # Header para simular navegador (evita bloqueio)
    headers = {
        "User-Agent": "Mozilla/5.0"
    }

    # Faz requisição HTTP
    response = requests.get(url, headers=headers)

    # Se der erro, retorna mensagem
    if response.status_code != 200:
        return "Erro ao acessar receitas."

    # Converte HTML em objeto analisável
    soup = BeautifulSoup(response.text, "html.parser")

    # Lista de resultados
    resultados = []

    # Procura todos os links da página
    for link in soup.find_all("a", href=True):
        href = link["href"]  # Pega o link

        # Filtra apenas links que parecem ser receitas
        if "/receita/" in href:
            titulo = link.get_text(strip=True)  # Pega o título

            # Evita títulos vazios
            if titulo:
                resultados.append(f"{titulo} - {href}")

        # Limita a 5 resultados
        if len(resultados) >= 5:
            break

    # Retorna resultados ou mensagem padrão
    return "\n".join(resultados) if resultados else "Nenhuma receita encontrada."


# ================================
# 6. PERSONA (PROMPT ENGINEERING)
# ================================

system_prompt = """
Você é o chef Gordon Ramsay.

Características:
- Extremamente exigente
- Sarcástico, mas útil
- Explica receitas de forma clara

REGRAS:
- Use APENAS o conteúdo fornecido
- NÃO invente receitas
- Se não houver dados, diga:
  "Não encontrei isso na Receiteria."
- Sempre dê dicas de chef
"""


# ================================
# 7. FUNÇÃO DO CHAT
# ================================

def chat(user_input):
    # Busca receitas relacionadas
    contexto = buscar_receita(user_input)

    # Monta prompt completo
    prompt = f"""
    {system_prompt}

    CONTEXTO:
    {contexto}

    Pergunta:
    {user_input}

    Responda usando somente o contexto acima.
    """

    # Chama o modelo
    response = llm.invoke(prompt)

    # Retorna resposta
    return response.content


# ================================
# 8. LOOP DE CONVERSA
# ================================

print("👨‍🍳 Chat com Gordon Ramsay (Receiteria)")
print("Digite 'x' para sair\n")

while True:
    # Entrada do usuário
    user_input = input("Você: ")

    # Condição de saída
    if user_input.lower() == "x":
        print("Saindo da cozinha... finalmente.")
        break

    # Gera resposta
    resposta = chat(user_input)

    # Mostra resposta
    print("\nGordon Ramsay:")
    print(resposta)
    print("\n" + "="*50 + "\n")
