<div align="center">

<img src="https://img.shields.io/badge/Bootcamp-HEINEKEN-green?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PC9zdmc+" />
<img src="https://img.shields.io/badge/DIO-Projeto%20Final-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/IA-Aplicada%20a%20Vendas-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen?style=for-the-badge" />

# 🤖 Copiloto de Vendas com IA — FYS
### Atendimento Inteligente para o Vendedor de Campo

*Projeto Final do Bootcamp HEINEKEN — Inteligência Artificial Aplicada a Vendas | DIO*

</div>

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [O Problema](#-o-problema)
- [A Solução](#-a-solução)
- [Usuário Principal](#-usuário-principal)
- [Abordagem Técnica](#-abordagem-técnica)
- [Base de Conhecimento](#-base-de-conhecimento)
- [Estrutura do Repositório](#-estrutura-do-repositório)
- [Como Usar](#-como-usar)
- [Exemplo de Conversa Real](#-exemplo-de-conversa-real)
- [Resultados Esperados](#-resultados-esperados)
- [Melhorias Futuras](#-melhorias-futuras)
- [Conclusão](#-conclusão)
- [Autor](#-autor)

---

## 🎯 Sobre o Projeto

Este projeto é o **Copiloto de Vendas com IA para Atendimento ao Cliente**, desenvolvido como projeto final do **Bootcamp HEINEKEN — Inteligência Artificial Aplicada a Vendas** pela plataforma [DIO](https://dio.me).

A solução foi construída com foco na marca **FYS** — refrigerante do grupo Heineken com 50% menos açúcar, tom de voz direto, ácido e autêntico — aplicando os conceitos de **Engenharia de Prompt**, **Agentes de IA** e **Base de Conhecimento** aprendidos ao longo da trilha.

> *"O objetivo não é substituir a pessoa vendedora, mas apoiar o atendimento com respostas mais claras, úteis e contextualizadas."*

---

## 🔍 O Problema

A **FYS** enfrenta um desafio real e urgente: apesar de as padarias serem o **principal canal de venda de refrigerantes no Brasil**, a marca tem **menos de 1% de penetração** nesse canal.

Por quê? Porque:

- A força de vendas da Heineken prioriza bares e baladas (maior volume de cerveja)
- Quando o vendedor chega numa padaria, tem **pouco tempo** (1 a 3 minutos) para argumentar
- Faltam respostas prontas e contextualizadas para as **objeções mais comuns**
- A comunicação genérica não reflete o **tom de voz único da FYS** — direto, levemente ácido e sem frescura

**Resultado:** oportunidades de venda perdidas por falta de argumentação rápida e alinhada à marca.

---

## 💡 A Solução

Um **Copiloto de Vendas com IA** que atua como assistente de campo para o vendedor da FYS. A solução usa engenharia de prompt avançada e uma base de conhecimento real para:

| Capacidade | Descrição |
|---|---|
| 🗣️ **Argumentação de Objeções** | Responde as 6 objeções mais comuns do dono de padaria |
| ✍️ **Reescrita no Tom FYS** | Transforma mensagens comerciais genéricas no estilo ácido da marca |
| 📍 **Priorização de Pontos de Venda** | Sugere critérios para o vendedor focar nos PDVs com mais potencial |
| 🔄 **Follow-up Inteligente** | Gera mensagens de acompanhamento para leads que "vão pensar" |
| 📚 **Conhecimento da Marca** | Responde dúvidas sobre posicionamento, produto e diferenciais da FYS |

---

## 👤 Usuário Principal

**Vendedor externo da FYS** — profissional que visita padarias, mercadinhos e pequenos comércios para ampliar a distribuição da marca.

**Perfil:**
- Pouco tempo por abordagem (1 a 3 minutos)
- Enfrenta as mesmas objeções repetidamente
- Precisa comunicar a proposta de valor da FYS de forma rápida e autêntica
- Às vezes não tem as palavras certas para contornar resistências sem soar forçado

---

## ⚙️ Abordagem Técnica

A solução utiliza a arquitetura de **Agente de IA com Base de Conhecimento**, seguindo o padrão **agents.md** (compatível com Antigravity, Claude Code, Open Code e outros harnesses):

```
Harness (ex: Antigravity/Claude Code)
        │
        ▼
   agents.md  ←── Persona + Regras + Tom de Voz
        │
        ▼
  knowledge/  ←── Contexto Real da FYS
   ├── contexto-fys.md
   ├── objecoes.md
   ├── produtos.md
   └── perguntas-frequentes.md
```

**Stack utilizado:**
- 🧠 **IA:** Engenharia de Prompt (estruturação de agentes com agents.md)
- 🔧 **Harness:** Antigravity (Gemini 2.5 Flash) — gratuito e com bom limite semanal
- 📁 **Base de Conhecimento:** Arquivos .md com transcrição real da live FYS + dados da marca
- 💾 **Versionamento:** GitHub
- 🤝 **Referência:** DIO Agent como mentor para escolha de recorte e estruturação

---

## 📚 Base de Conhecimento

A base de conhecimento foi construída a partir de **dados reais** da marca FYS, incluindo:

- **Transcrição da live** *"FYS: Por Dentro da Marca, Desafios e Ideias para o Projeto Final"* (DIO, 02/06/2026)
- Dados de mercado: penetração <1% no canal de padarias, +72.000 padarias no Brasil
- Tom de voz oficial da marca: direto, levemente ácido, honesto, sem frescura
- Posicionamento: "a gente não finge que é o melhor — a gente é diferente"
- Diferenciais do produto: 50% menos açúcar, formato individual, grupo Heineken

```
knowledge/
├── contexto-fys.md        # Histórico, posicionamento e dados de mercado
├── objecoes.md            # 6 objeções + respostas no tom FYS
├── produtos.md            # Linha de produtos, formatos e diferenciais
└── perguntas-frequentes.md # FAQ para o vendedor de campo
```

---

## 📁 Estrutura do Repositório

```
copiloto-vendas-ia-fys/
│
├── README.md                    # Este arquivo — documentação completa do projeto
├── agents.md                    # Definição do agente (persona, regras, capacidades)
├── cloud.md                     # Atalho para Claude Code (aponta para agents.md)
│
└── knowledge/                   # Base de conhecimento do copiloto
    ├── contexto-fys.md          # Contexto real da marca FYS
    ├── objecoes.md              # Objeções de vendas + respostas no tom da marca
    ├── produtos.md              # Produtos, formatos e diferenciais
    └── perguntas-frequentes.md  # Perguntas frequentes do vendedor
```

---

## 🚀 Como Usar

### Opção 1 — Antigravity (Recomendado, Gratuito)

1. Acesse [aistudio.google.com/gemini](https://aistudio.google.com) ou instale o [Antigravity](https://antigravity.ai)
2. Clone ou baixe este repositório
3. Abra a pasta `copiloto-vendas-ia-fys` no Antigravity
4. O agente será carregado automaticamente a partir do `agents.md`
5. Comece a conversar!

### Opção 2 — Claude Code

1. Instale o [Claude Code](https://claude.ai/code)
2. Abra a pasta do projeto
3. O `cloud.md` redirecionará para o `agents.md` automaticamente

### Opção 3 — Qualquer IA (sem harness)

Copie o conteúdo do `agents.md` e cole como **system prompt** em qualquer IA (ChatGPT, Gemini, Claude).

---

## 💬 Exemplo de Conversa Real

**Contexto:** Vendedor está na porta de uma padaria. O dono acabou de dizer a objeção mais comum.

---

**🧑 Vendedor →** *"O dono da padaria acabou de falar: 'Nunca ouvi falar dessa marca. Meus clientes compram Coca-Cola mesmo.' O que eu respondo?"*

**🤖 Copiloto FYS →**

> *"Entendo. Faz sentido — a Coca tem décadas de estante aqui. Mas olha: você já colocou produto novo antes e deu certo? A FYS não tá disputando o espaço da Coca. Ela tá ocupando o espaço que já tá vazio — o do cliente que tá saindo da fila do caixa sem comprar porque não quer tanto açúcar. Coloca 6 unidades pra testar uma semana. Se não vender, a gente conversa."*

---

**🧑 Vendedor →** *"Ele disse que vai pensar. Como mando uma mensagem de follow-up pro WhatsApp sem parecer chato?"*

**🤖 Copiloto FYS →**

> *"Ei, [nome]! Fui eu que passei semana passada com a FYS. Só queria avisar que a promoção de entrada tá valendo até sexta. Nada de pressão — mas se quiser garantir o preço de teste, é essa semana. Qualquer dúvida, tô aqui."*

---

**🧑 Vendedor →** *"Preciso de uma mensagem de apresentação no WhatsApp para mandar antes de visitar a padaria. Nada corporativo."*

**🤖 Copiloto FYS →**

> *"Oi, [nome]! Passo na sua padaria amanhã de manhã com uma novidade do grupo Heineken. Não é cerveja — prometo. Leva 3 minutinhos. Posso passar lá pelas 9h?"*

---

## 📈 Resultados Esperados

Com o Copiloto FYS em campo, o vendedor consegue:

- ⚡ **Reduzir o tempo de resposta** a objeções de minutos para segundos
- 🎯 **Aumentar a taxa de conversão** em padarias com argumentos contextualizados
- 🗣️ **Manter o tom de voz da marca** sem precisar memorizar scripts
- 📱 **Gerar mensagens de WhatsApp** prontas para uso, alinhadas ao DNA da FYS
- 📊 **Priorizar PDVs** com maior potencial de conversão

---

## 🔮 Melhorias Futuras

| Melhoria | Descrição | Prioridade |
|---|---|---|
| 🗺️ **Mapa de PDVs** | Integração com dados geográficos para priorizar padarias por região | Alta |
| 📊 **Dashboard de Objeções** | Painel com as objeções mais frequentes por região para treinar o time | Alta |
| 🔊 **Versão por Voz** | Copiloto ativado por voz via smartphone durante a visita | Média |
| 🌍 **Expansão de Canal** | Adaptar o copiloto para bares, mercados e restaurantes | Média |
| 📈 **Análise de Desempenho** | Registro de conversões por vendedor para mensurar impacto da IA | Baixa |
| 🤝 **Treinamento de Novos Vendedores** | Usar o copiloto como simulador de onboarding | Baixa |

---

## 🏁 Conclusão

Este projeto demonstra como a **Inteligência Artificial aplicada a vendas** pode transformar o trabalho de campo de uma equipe comercial — não substituindo o vendedor, mas amplificando sua capacidade de argumentação, adaptação e comunicação.

A marca **FYS** foi o cenário perfeito para esse desafio: produto real, problema real, dados reais e uma identidade de marca forte o suficiente para guiar até o tom de voz das respostas da IA. Isso fez toda a diferença entre um projeto genérico e uma solução que poderia ser colocada em produção amanhã.

Mais do que uma entrega técnica, este projeto representa uma mudança de mentalidade: **qualquer profissional de vendas, com o prompt certo e o contexto certo, pode ter um especialista de marca disponível 24h no bolso.**

A jornada pelo **Bootcamp HEINEKEN — IA Aplicada a Vendas** foi transformadora. Os conceitos de Engenharia de Prompt, Agentes de IA, Bases de Conhecimento e uso estratégico de ferramentas como o DIO Agent provaram que a IA não é um tema distante — é uma habilidade prática, acessível e que já gera impacto real no mercado.

> *"Não é sobre tecnologia. É sobre resolver problemas reais com as ferramentas certas."*

---

## 👨‍💻 Autor

<div align="center">

| | |
|---|---|
| **Nome** | rodrigofonsecahod-rgb |
| **Bootcamp** | HEINEKEN — Inteligência Artificial Aplicada a Vendas |
| **Plataforma** | [DIO — Digital Innovation One](https://dio.me) |
| **Conclusão** | Junho de 2026 |
| **GitHub** | [@rodrigofonsecahod-rgb](https://github.com/rodrigofonsecahod-rgb) |

</div>

---

### 🙏 Agradecimentos

À **HEINEKEN** pelo patrocínio deste bootcamp gratuito e por abrir os bastidores da marca **FYS** como contexto real para o projeto final.

À equipe da **DIO** — em especial ao **Venilton FalvoJr** pelas lives e mentorias que tornaram este projeto possível.

À comunidade de mais de **5.866 alunos** que percorreram essa jornada junto.

---

<div align="center">

*Feito com 💚 e muito contexto durante o Bootcamp HEINEKEN IA Aplicada a Vendas — DIO 2026*

[![DIO](https://img.shields.io/badge/DIO-Bootcamp%20Conclu%C3%ADdo-green?style=flat-square)](https://dio.me)
[![HEINEKEN](https://img.shields.io/badge/HEINEKEN-IA%20Aplicada%20a%20Vendas-darkgreen?style=flat-square)](https://www.heineken.com/br)

</div>
