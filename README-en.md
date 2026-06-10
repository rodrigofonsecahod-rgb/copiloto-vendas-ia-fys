<div align="center">

<img src="https://img.shields.io/badge/Bootcamp-HEINEKEN-green?style=for-the-badge" />
<img src="https://img.shields.io/badge/DIO-Final%20Project-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/AI-Applied%20to%20Sales-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

# 🤖 AI Sales Copilot — FYS
### Intelligent Field Sales Assistant

*Final Project — HEINEKEN Bootcamp: Artificial Intelligence Applied to Sales | DIO*

> 🇧🇷 [Versão em Português](./README.md)

</div>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [The Problem](#-the-problem)
- [The Solution](#-the-solution)
- [Primary User](#-primary-user)
- [Technical Approach](#-technical-approach)
- [Knowledge Base](#-knowledge-base)
- [Repository Structure](#-repository-structure)
- [How to Use](#-how-to-use)
- [Real Conversation Example](#-real-conversation-example)
- [Expected Results](#-expected-results)
- [Future Improvements](#-future-improvements)
- [Conclusion](#-conclusion)
- [Author](#-author)

---

## 🎯 About the Project

This project is the **AI Sales Copilot for Customer Service**, developed as the final project for the **HEINEKEN Bootcamp — Artificial Intelligence Applied to Sales** on the [DIO](https://dio.me) platform.

The solution was built with a focus on the **FYS** brand — a Heineken Group sparkling beverage with 50% less sugar, a direct, sharp, and authentic tone of voice — applying the concepts of **Prompt Engineering**, **AI Agents**, and **Knowledge Base** learned throughout the program.

> *"The goal is not to replace the salesperson, but to support customer interactions with clearer, more useful, and more contextualized responses."*

---

## 🔍 The Problem

**FYS** faces a real and urgent challenge: despite bakeries being the **main soft drink retail channel in Brazil**, the brand has **less than 1% penetration** in that channel.

Why? Because:

- Heineken's sales force prioritizes bars and nightclubs (higher beer volume)
- When a sales rep visits a bakery, they have **very little time** (1 to 3 minutes) to make their case
- There are no ready-made, contextualized responses for the **most common objections**
- Generic messaging doesn't reflect **FYS's unique tone of voice** — direct, slightly sharp, and no-nonsense

**Result:** lost sales opportunities due to lack of fast, brand-aligned argumentation.

---

## 💡 The Solution

An **AI Sales Copilot** that acts as a field assistant for FYS sales reps. The solution uses advanced prompt engineering and a real knowledge base to:

| Capability | Description |
|---|---|
| 🗣️ **Objection Handling** | Responds to the 6 most common bakery owner objections |
| ✍️ **FYS Tone Rewriter** | Transforms generic commercial messages into the brand's sharp style |
| 📍 **Point-of-Sale Prioritization** | Suggests criteria for the sales rep to focus on the highest-potential PDVs |
| 🔄 **Smart Follow-up** | Generates follow-up messages for leads that said "I'll think about it" |
| 📚 **Brand Knowledge** | Answers questions about FYS positioning, product, and differentiators |

---

## 👤 Primary User

**FYS field sales representative** — a professional who visits bakeries, convenience stores, and small retailers to expand the brand's distribution.

**Profile:**
- Very little time per approach (1 to 3 minutes)
- Faces the same objections repeatedly
- Needs to communicate FYS's value proposition quickly and authentically
- Sometimes lacks the right words to overcome resistance without sounding forced

---

## ⚙️ Technical Approach

The solution uses the **AI Agent with Knowledge Base** architecture, following the **agents.md** open standard (compatible with Antigravity, Claude Code, Open Code, and other harnesses):

```
Harness (e.g. Antigravity / Claude Code)
        │
        ▼
  agents-en.md  ←── Persona + Rules + Tone of Voice
        │
        ▼
  knowledge/    ←── Real FYS Context
   ├── context-fys-en.md
   ├── objections-en.md
   ├── products-en.md
   └── faq-en.md
```

**Stack used:**
- 🧠 **AI:** Prompt Engineering (agent structuring with agents.md)
- 🔧 **Harness:** Antigravity (Gemini 2.5 Flash) — free tier with generous weekly limits
- 📁 **Knowledge Base:** .md files with real FYS live transcription + brand data
- 💾 **Version Control:** GitHub
- 🤝 **Reference:** DIO Agent as mentor for project scoping and structuring

---

## 📚 Knowledge Base

The knowledge base was built from **real FYS brand data**, including:

- **Live transcript** from *"FYS: Inside the Brand, Challenges and Ideas for the Final Project"* (DIO, June 2, 2026)
- Market data: <1% penetration in bakery channel, 72,000+ bakeries in Brazil
- Official brand tone of voice: direct, slightly sharp, honest, no-nonsense
- Positioning: "we don't pretend to be the best — we're just different"
- Product differentiators: 50% less sugar, individual format, Heineken Group

```
knowledge/
├── context-fys-en.md       # Brand history, positioning, and market data
├── objections-en.md        # 6 objections + ready responses in FYS brand voice
├── products-en.md          # Product line, formats, and differentiators
└── faq-en.md               # Field sales rep FAQ
```

---

## 📁 Repository Structure

```
copiloto-vendas-ia-fys/
│
├── README.md                    # Portuguese version — full project documentation
├── README-en.md                 # This file — English version
├── agents.md                    # Agent definition in Portuguese
├── agents-en.md                 # Agent definition in English
│
└── knowledge/                   # Bilingual knowledge base
    ├── contexto-fys.md          # FYS brand context (PT)
    ├── context-fys-en.md        # FYS brand context (EN)
    ├── objecoes.md              # Sales objections (PT)
    ├── objections-en.md         # Sales objections (EN)
    ├── produtos.md              # Products (PT)
    ├── products-en.md           # Products (EN)
    ├── perguntas-frequentes.md  # FAQ (PT)
    └── faq-en.md                # FAQ (EN)
```

---

## 🚀 How to Use

### Option 1 — Antigravity (Recommended, Free)

1. Access [Antigravity](https://antigravity.ai) or install the desktop app
2. Clone or download this repository
3. Open the `copiloto-vendas-ia-fys` folder in Antigravity
4. Point to `agents-en.md` as your agent file
5. Start chatting!

### Option 2 — Claude Code

1. Install [Claude Code](https://claude.ai/code)
2. Open the project folder
3. The agent will load from `agents-en.md` automatically

### Option 3 — Any AI (no harness required)

Copy the contents of `agents-en.md` and paste it as a **system prompt** in any AI (ChatGPT, Gemini, Claude).

---

## 💬 Real Conversation Example

**Context:** Sales rep is visiting a bakery. The owner just raised the most common objection.

---

**🧑 Sales Rep →** *"The bakery owner just said: 'I've never heard of this brand. My customers always buy Coke.' What do I say?"*

**🤖 FYS Copilot →**

> *"That makes sense — Coke has been on the shelf for decades. But here's the thing: have you ever introduced a new product that worked out? FYS isn't competing with Coke. It's filling the gap — the customer who leaves without buying because they don't want that much sugar. Put 6 units in to test for a week. If it doesn't sell, we talk."*

---

**🧑 Sales Rep →** *"He said he'll think about it. How do I send a WhatsApp follow-up without being annoying?"*

**🤖 FYS Copilot →**

> *"Hey [name]! It's me — I stopped by last week with FYS. Just wanted to let you know the introductory promo is good until Friday. No pressure — but if you want to lock in the test price, this week's the window. I'm here if you have questions."*

---

**🧑 Sales Rep →** *"I need a WhatsApp intro message to send before visiting. Nothing corporate."*

**🤖 FYS Copilot →**

> *"Hey [name]! Stopping by your bakery tomorrow morning with something new from the Heineken Group. Not beer — promise. Takes 3 minutes. Can I come by around 9am?"*

---

## 📈 Expected Results

With the FYS Copilot in the field, sales reps can:

- ⚡ **Cut response time** to objections from minutes to seconds
- 🎯 **Increase conversion rates** at bakeries with contextualized arguments
- 🗣️ **Maintain brand tone** without memorizing scripts
- 📱 **Generate ready-to-use WhatsApp messages** aligned with FYS DNA
- 📊 **Prioritize high-potential PDVs** to maximize field efficiency

---

## 🔮 Future Improvements

| Improvement | Description | Priority |
|---|---|---|
| 🗺️ **PDV Map** | Geographic data integration to prioritize bakeries by region | High |
| 📊 **Objections Dashboard** | Panel with most frequent objections by region to train the team | High |
| 🔊 **Voice Version** | Voice-activated copilot via smartphone during visits | Medium |
| 🌍 **Channel Expansion** | Adapt the copilot for bars, markets, and restaurants | Medium |
| 📈 **Performance Analytics** | Track conversions per sales rep to measure AI impact | Low |
| 🤝 **Onboarding Simulator** | Use the copilot as a training tool for new sales reps | Low |

---

## 🏁 Conclusion

This project demonstrates how **Artificial Intelligence applied to sales** can transform the fieldwork of a commercial team — not by replacing the salesperson, but by amplifying their argumentation, adaptability, and communication skills.

The **FYS** brand was the perfect scenario for this challenge: a real product, a real problem, real data, and a brand identity strong enough to guide even the tone of voice of the AI's responses. That's what made the difference between a generic project and a solution that could be deployed in production tomorrow.

More than a technical deliverable, this project represents a mindset shift: **any sales professional, with the right prompt and the right context, can have a brand expert available 24/7 in their pocket.**

The journey through the **HEINEKEN Bootcamp — AI Applied to Sales** was transformative. The concepts of Prompt Engineering, AI Agents, Knowledge Bases, and strategic use of tools like the DIO Agent proved that AI is not a distant subject — it's a practical, accessible skill that already generates real impact in the market.

> *"It's not about technology. It's about solving real problems with the right tools."*

---

## 👨‍💻 Author

<div align="center">

| | |
|---|---|
| **Name** | rodrigofonsecahod-rgb |
| **Bootcamp** | HEINEKEN — Artificial Intelligence Applied to Sales |
| **Platform** | [DIO — Digital Innovation One](https://dio.me) |
| **Completed** | June 2026 |
| **GitHub** | [@rodrigofonsecahod-rgb](https://github.com/rodrigofonsecahod-rgb) |

</div>

---

### 🙏 Acknowledgements

To **HEINEKEN** for sponsoring this free bootcamp and for opening up the **FYS** brand as real-world context for the final project.

To the **DIO** team — especially **Venilton FalvoJr** for the live sessions and mentorships that made this project possible.

To the community of over **5,866 students** who walked this journey together.

---

<div align="center">

*Built with 💚 and a lot of context during the HEINEKEN AI Applied to Sales Bootcamp — DIO 2026*

[![DIO](https://img.shields.io/badge/DIO-Bootcamp%20Completed-green?style=flat-square)](https://dio.me)
[![HEINEKEN](https://img.shields.io/badge/HEINEKEN-AI%20Applied%20to%20Sales-darkgreen?style=flat-square)](https://www.heineken.com/br)

</div>
