# Chatbot_especialista_em_receitas
Um chatbot criado para responder perguntas relacionadas ao ramo da culinária. Ele te ensina receitas, dá dicas para a receita, substitui ingredientes. Tudo isso enquanto interpreta o famoso Chef, Gordon Ramsay. 

# 🍳 AI Recipe Assistant

Plataforma de chatbot inteligente focada em recomendações culinárias, geração dinâmica de receitas e assistência gastronômica utilizando Inteligência Artificial Conversacional, Engenharia de Prompt e gerenciamento contextual.

---

# 📌 Visão Geral

O **AI Recipe Assistant** é um sistema conversacional projetado para auxiliar usuários na descoberta, personalização e organização de receitas culinárias através de IA.

O projeto combina:

* Engenharia de Prompt
* IA Conversacional
* Estruturação de contexto
* Fluxo lógico de respostas
* Arquitetura escalável
* Integração com APIs de linguagem

A plataforma foi desenvolvida seguindo princípios modernos de engenharia de software, priorizando:

* modularidade;
* organização;
* extensibilidade;
* manutenibilidade;
* experiência conversacional inteligente.

---

# 🎯 Objetivo Principal

Criar um assistente culinário inteligente capaz de:

* recomendar receitas personalizadas;
* sugerir pratos com base em ingredientes disponíveis;
* adaptar receitas para restrições alimentares;
* manter contexto conversacional;
* estruturar respostas coerentes;
* oferecer experiência natural e dinâmica.

---

# 🧠 Tecnologias Utilizadas

## Backend

* Node.js
* TypeScript
* Express.js

## Inteligência Artificial

* OpenAI API
* Prompt Engineering
* Context Memory Management

## Infraestrutura

* Docker
* GitHub Actions
* REST APIs

## Qualidade e Organização

* ESLint
* Prettier
* Conventional Commits

---

# 🚀 Funcionalidades

## 🔹 Recomendações Inteligentes

* Sugestão de receitas
* Receitas por ingredientes
* Personalização alimentar

## 🔹 IA Conversacional

* Fluxo conversacional contextual
* Respostas dinâmicas
* Conversas multi-etapas

## 🔹 Gestão de Contexto

* Histórico de interação
* Memória contextual
* Continuidade conversacional

## 🔹 Estruturação de Prompts

* Prompts especializados
* Organização modular
* Ajuste contextual automático

## 🔹 Organização Escalável

* Arquitetura desacoplada
* Estrutura modular
* Facilidade de expansão

---

# 🔄 Demonstração do Fluxo

```txt id="p7n4b8"
Usuário
   ↓
API Gateway
   ↓
Gerenciador Conversacional
   ↓
Context Manager
   ↓
Prompt Engine
   ↓
API de IA
   ↓
Processador de Resposta
   ↓
Resposta Final
```

---

# 🍽️ Exemplo de Conversa

## Entrada do usuário

```txt id="xj9c3n"
Tenho arroz, frango e cenoura. O que posso cozinhar?
```

## Resposta do chatbot

```txt id="d3w0ks"
Você pode preparar um risoto simples de frango com cenoura.

Ingredientes:
- arroz
- frango
- cenoura
- alho
- cebola

Modo de preparo:
...
```

---

# 📁 Estrutura de Pastas

```txt id="v6n8yk"
project/
│
├── src/
│   ├── controllers/
│   ├── services/
│   ├── prompts/
│   ├── context/
│   ├── integrations/
│   ├── middlewares/
│   └── utils/
│
├── docs/
│   ├── architecture.md
│   ├── prompts.md
│   ├── flows.md
│   └── challenges.md
│
├── tests/
│
├── assets/
│
├── .env.example
├── docker-compose.yml
├── package.json
└── README.md
```

---

# ⚙️ Como Executar Localmente

## 1. Clonar o repositório

```bash id="3v4m0l"
git clone https://github.com/seuusuario/ai-recipe-assistant.git
```

---

## 2. Instalar dependências

```bash id="f1l9nv"
npm install
```

---

## 3. Configurar variáveis de ambiente

Crie um arquivo `.env`:

```env id="f9b5ry"
OPENAI_API_KEY=your_api_key
PORT=3000
MODEL=gpt-4
CONTEXT_LIMIT=10
```

---

## 4. Executar aplicação

```bash id="r4b2zu"
npm run dev
```

---

# 🔐 Variáveis de Ambiente

| Variável       | Descrição                      |
| -------------- | ------------------------------ |
| OPENAI_API_KEY | Chave da API de IA             |
| PORT           | Porta da aplicação             |
| MODEL          | Modelo de IA utilizado         |
| CONTEXT_LIMIT  | Limite de histórico contextual |

---

# 🧩 Contexto do Projeto

## Problema Resolvido

Usuários frequentemente enfrentam dificuldades para:

* decidir o que cozinhar;
* utilizar ingredientes disponíveis;
* adaptar receitas;
* encontrar receitas rápidas;
* organizar preferências alimentares.

Além disso, muitos sistemas culinários tradicionais:

* possuem pouca personalização;
* não mantêm contexto;
* apresentam experiência limitada.

---

## Cenário de Uso

A plataforma pode ser utilizada em:

* aplicativos culinários;
* assistentes domésticos;
* sistemas de recomendação;
* plataformas gastronômicas;
* automação de atendimento alimentar.

---

## Público-Alvo

* Usuários domésticos
* Entusiastas culinários
* Aplicativos de receitas
* Plataformas food-tech
* Assistentes inteligentes

---

## Motivação Técnica

O projeto foi criado para explorar:

* IA aplicada à conversação;
* engenharia de prompt;
* gestão contextual;
* arquitetura modular;
* construção de sistemas conversacionais escaláveis.

---

# 🏗️ Visão Geral da Solução

## Funcionamento do Sistema

O chatbot processa mensagens do usuário, organiza contexto, monta prompts especializados e consulta APIs de IA para gerar respostas contextualizadas.

A arquitetura foi desenhada para:

* reduzir inconsistências;
* melhorar coerência;
* facilitar escalabilidade;
* modularizar componentes.

---

## Fluxo Conversacional

```txt id="t2v5o7"
Entrada do usuário
↓
Validação
↓
Recuperação de contexto
↓
Montagem do prompt
↓
Consulta IA
↓
Processamento da resposta
↓
Entrega final
```

---

## Gestão de Contexto

O sistema mantém:

* histórico resumido;
* preferências culinárias;
* restrições alimentares;
* continuidade da conversa.

Isso melhora:

* coerência;
* personalização;
* qualidade da experiência.

---

## Estrutura de Prompts

Os prompts são divididos em:

* system prompts;
* prompts culinários;
* prompts contextuais;
* prompts dinâmicos.

Exemplo:

```txt id="e7m4xj"
Você é um chef especializado em receitas rápidas e econômicas.
```

---

# 🧱 Arquitetura da Solução

## Arquitetura em Camadas

```txt id="d7m4tu"
Presentation Layer
↓
Conversation Layer
↓
Prompt Engine
↓
AI Integration Layer
↓
Context Storage
```

---

## Camadas do Sistema

### Presentation Layer

Responsável por:

* entrada de mensagens;
* APIs REST;
* validação inicial.

---

### Conversation Layer

Gerencia:

* fluxo conversacional;
* regras de interação;
* sessões.

---

### Prompt Engine

Responsável por:

* composição de prompts;
* enriquecimento contextual;
* padronização de instruções.

---

### AI Integration Layer

Comunicação com:

* OpenAI API;
* modelos de linguagem;
* serviços externos.

---

### Context Storage

Armazena:

* histórico;
* contexto resumido;
* preferências do usuário.

---

## Escalabilidade

O sistema foi preparado para:

* múltiplos modelos de IA;
* expansão modular;
* microsserviços futuros;
* cache contextual;
* integração multi-plataforma.

---

# 📖 Instruções de Uso

## Exemplo de Requisição

```json id="2j4t9o"
{
  "message": "Quero uma receita vegana com batata",
  "sessionId": "session_001"
}
```

---

## Exemplo de Resposta

```json id="pk0v4m"
{
  "response": "Você pode preparar um escondidinho vegano de batata...",
  "contextUpdated": true
}
```

---

## Estrutura dos Prompts

```txt id="w6k9cx"
[System Prompt]
Define comportamento global

[Recipe Prompt]
Especialização culinária

[Context Prompt]
Histórico do usuário

[User Prompt]
Mensagem atual
```

---

# ⚠️ Desafios Superados

## 🔹 Controle de Contexto

Problema:

* perda de coerência em conversas longas.

Solução:

* memória contextual;
* resumo inteligente de sessões.

---

## 🔹 Respostas Inconsistentes

Problema:

* receitas incoerentes ou repetitivas.

Solução:

* engenharia de prompt modular;
* refinamento contextual.

---

## 🔹 Escalabilidade

Problema:

* crescimento desorganizado da aplicação.

Solução:

* arquitetura modular;
* desacoplamento de componentes.

---

## 🔹 Performance

Problema:

* excesso de contexto aumentando latência.

Solução:

* otimização contextual;
* compressão de histórico.

---

## 🔹 Fluxo Conversacional

Problema:

* quebra de continuidade.

Solução:

* gerenciamento de estado conversacional.

---

# 🌟 Diferenciais Técnicos

## Engenharia de Prompt Estratégica

A solução utiliza:

* prompts especializados;
* modularização contextual;
* refinamento dinâmico.

---

## Organização Arquitetural

O projeto aplica:

* clean architecture;
* separação de responsabilidades;
* modularização por domínio.

---

## Escalabilidade

Preparado para:

* múltiplos providers;
* APIs externas;
* expansão contínua.

---

## Uso Estratégico de IA

A IA é utilizada para:

* interpretação contextual;
* personalização culinária;
* geração dinâmica de conteúdo;
* adaptação de respostas.

---

## Boas Práticas Aplicadas

* Conventional Commits
* CI/CD
* Estrutura modular
* Versionamento semântico
* Documentação técnica
* Padronização arquitetural

---

# 🛣️ Roadmap

## Próximas Evoluções

* Memória vetorial
* Sistema de favoritos
* Geração de lista de compras
* Sugestão nutricional
* Dashboard administrativo
* Integração com voz

---

# 🔮 Melhorias Futuras

* Multi-language support
* Integração mobile
* Recomendação baseada em perfil
* Fine-tuning culinário
* Analytics conversacional

---

# 📌 Conclusão

O AI Recipe Assistant foi desenvolvido como uma plataforma moderna de IA conversacional aplicada ao universo culinário.

O projeto demonstra:

* organização arquitetural;
* engenharia de prompt;
* gestão contextual;
* modularidade;
* escalabilidade;
* e maturidade técnica em engenharia de software.

Mais do que um chatbot, o sistema representa uma base sólida para construção de assistentes inteligentes orientados por IA.
