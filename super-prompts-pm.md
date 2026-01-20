# 🧠 Super Prompts for Product Managers (AI Engineering)

Este repositório contém prompts estruturados usando a técnica **Chain-of-Thought**.
Os prompts estão em **Inglês** (para melhor performance dos modelos), mas as explicações de uso estão em Português.

---

## 1. O Arquiteto de Software (Validação Técnica)
**Quando usar:** Antes de levar uma ideia para o time de engenharia, para validar viabilidade e riscos.

> **Prompt (Copy & Paste):**
> "Act as a Senior Software Architect at Google. I am a Product Manager.
>
> **Context:** I want to build a feature for [INSERT FEATURE - e.g., Real-time Order Tracking].
> **Stack:** We use [React, Supabase, Node.js].
>
> **Your Task:**
> 1. Design the high-level technical architecture for this solution considering scalability for 100k users.
> 2. List 3 critical technical risks (Edge Cases) and security concerns (e.g., RLS policies).
> 3. Estimate technical complexity (Low/Medium/High) and justify.
>
> Constraint: Be critical and technical. Ignore marketing jargon."

---

## 2. O Gerador de Testes (QA & BDD)
**Quando usar:** Para transformar requisitos em testes automatizáveis.

> **Prompt (Copy & Paste):**
> "Act as a QA Automation Engineer specialized in BDD (Behavior Driven Development).
>
> **Feature:** [INSERT FEATURE - e.g., Social Login].
>
> **Your Task:**
> Write Test Scenarios covering the 'Happy Path' and specifically the 'Unhappy Paths' (Errors).
> Strictly use the Gherkin format (Given / When / Then).
>
> Example Format:
> Scenario: User attempts login with invalid token
> Given I am on the login screen
> When I send an expired auth token
> Then I should receive a 401 Unauthorized response
> And I should see error message 'X'."

---

## 3. O Tradutor de Dívida Técnica (Engenharia -> C-Level)
**Quando usar:** Para convencer a diretoria a investir em refatoração.

> **Prompt (Copy & Paste):**
> "Act as a Chief Product Officer (CPO) focused on Business Value.
>
> **Technical Problem:** [PASTE DEV EXPLANATION - e.g., 'Database indexing is causing locks'].
>
> **Your Task:**
> Rewrite this technical problem for a non-technical audience (CEO/Sales VP).
> 1. Explain the Business Impact (Revenue loss, Churn risk, or operational cost).
> 2. Use a simple analogy.
> 3. Justify the engineering time investment in terms of ROI or risk mitigation.
>
> Tone: Professional, urgent, and money-focused."

---
*Criado por [Pablo F. Pulido](https://www.linkedin.com/in/pablofpulido/)*
