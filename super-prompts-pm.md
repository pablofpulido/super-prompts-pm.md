# 🧠 Super Prompts for Product Managers (AI Engineering)

Este repositório contém uma coleção de **10 Prompts Avançados** estruturados para Product Managers Técnicos.
O objetivo é utilizar a IA como um par de engenharia e estratégia.

**Idioma:** Os prompts estão em **Inglês** para garantir a melhor performance lógica dos modelos (GPT-4o, Claude 3.5 Sonnet, Gemini 1.5 Pro).
**Como usar:** Copie o bloco de código, preencha os campos entre colchetes `[ ]` e execute no seu modelo de IA preferido.

---

## 🏗️ Technical & Architecture

### 1. O Arquiteto de Software (Validação Técnica)
**Quando usar:** Antes de levar uma ideia para o time de engenharia, para validar viabilidade e antecipar riscos.

> **Prompt:**
> "Act as a Senior Software Architect at Google. I am a Product Manager.
>
> **Context:** I want to build a feature for [INSERT FEATURE - e.g., Real-time Order Tracking].
> **Stack:** We use [React, Supabase, Node.js].
>
> **Your Task:**
> 1. Design the high-level technical architecture for this solution considering scalability for 100k users.
> 2. List 3 critical technical risks (Edge Cases) and security concerns (e.g., RLS policies, API rate limits).
> 3. Estimate technical complexity (Low/Medium/High) and justify.
>
> **Constraint:** Be critical and technical. Ignore marketing jargon. Focus on data flow and latency."

### 2. O Especialista em API (Especificação Técnica)
**Quando usar:** Para escrever documentação técnica ou explicar para o Front-end como consumir dados do Back-end.

> **Prompt:**
> "Act as a Senior Backend Engineer.
>
> **Context:** We need an API endpoint to [INSERT GOAL - e.g., Retrieve User Transaction History].
> **Data Points Needed:** [Date, Amount, Merchant, Category, Status].
>
> **Your Task:**
> 1. Write the Swagger/OpenAPI specification (YAML or JSON) for this endpoint `GET /transactions`.
> 2. Define the JSON Response structure, including correct data types (integers, strings, timestamps).
> 3. List the potential HTTP Error Codes (400, 401, 403, 500) and what triggers them.
>
> **Constraint:** Follow RESTful best practices."

### 3. O Analista de Dados (Gerador de SQL)
**Quando usar:** Quando você precisa extrair dados sozinho sem depender do time de Dados.

> **Prompt:**
> "Act as a Senior Data Analyst.
>
> **Context:** I need to analyze retention. We have a table named `users` and a table named `logins`.
> **Schema:**
> - `users`: user_id, signup_date, country
> - `logins`: login_id, user_id, login_timestamp
>
> **Your Task:**
> 1. Write an optimized PostgreSQL query to calculate the Day-1, Day-7, and Day-30 retention rates for users who signed up in the last 3 months.
> 2. Explain the query logic step-by-step so I can double-check it.
>
> **Constraint:** Use Common Table Expressions (CTEs) for readability."

---

## 🚀 Strategy & Growth

### 4. O Cientista de Growth (Design de Experimento)
**Quando usar:** Para estruturar testes A/B com rigor estatístico.

> **Prompt:**
> "Act as a Head of Growth.
>
> **Hypothesis:** I believe that [INSERT HYPOTHESIS - e.g., removing the credit card field from the trial signup] will increase conversion by [X%].
>
> **Your Task:**
> 1. Design an A/B test to validate this. Define the Control Group vs. Variant Group.
> 2. Define the Primary Metric (Success) and Guardrail Metrics (what we shouldn't break).
> 3. Calculate the sample size needed for statistical significance (assume current conversion is 2% and MDE is 0.5%).
> 4. List potential threats to validity (e.g., seasonality, novelty effect).
>
> **Format:** Present as a structured Experiment Doc."

### 5. O Estrategista de Produto (Opportunity Solution Tree)
**Quando usar:** Para conectar entregas de engenharia com objetivos de negócio.

> **Prompt:**
> "Act as a Product Leader (ref: Teresa Torres).
>
> **North Star Metric:** [INSERT METRIC - e.g., Increase Weekly Active Users].
> **Problem:** Users are churning after 2 weeks.
>
> **Your Task:**
> 1. Create an Opportunity Solution Tree.
> 2. Identify 3 distinct Opportunities (Customer Pain Points) that cause this churn.
> 3. For each Opportunity, propose 2 potential Solutions (Features/Experiments).
> 4. Rank the solutions based on ICE Score (Impact, Confidence, Ease).
>
> **Constraint:** Focus on outcomes, not outputs."

### 6. O Analista de Mercado (Análise de Competidores)
**Quando usar:** Para entender como diferenciar seu produto.

> **Prompt:**
> "Act as a Competitive Intelligence Expert.
>
> **My Product:** [INSERT DESCRIPTION].
> **Competitor:** [INSERT COMPETITOR URL or NAME].
>
> **Your Task:**
> 1. Conduct a SWOT analysis of the competitor specifically regarding their [Specific Feature - e.g., Onboarding Flow].
> 2. Identify a 'Gap in the Market' that they are ignoring but users are complaining about (simulate user reviews).
> 3. Propose a 'Killer Feature' that would give us an unfair advantage."

---

## ⚙️ Execution & Operations

### 7. O Engenheiro de QA (Caçador de Bugs)
**Quando usar:** Para encontrar furos na sua User Story antes dos devs.

> **Prompt:**
> "Act as a Senior QA Automation Engineer.
>
> **Feature:** [INSERT USER STORY - e.g., As a user, I want to transfer money to a friend].
>
> **Your Task:**
> 1. Generate 10 distinct Test Cases.
> 2. Include 3 'Happy Paths' and 7 'Edge Cases' (e.g., negative balance, network timeout, emojis in text fields, SQL injection attempts).
> 3. Write these in Gherkin syntax (Given/When/Then).
>
> **Goal:** Try to break the logic of the feature."

### 8. O Negotiator (Gestão de Stakeholders)
**Quando usar:** Quando você precisa dizer "Não" para um stakeholder importante ou pedir mais prazo.

> **Prompt:**
> "Act as a Diplomatic Product Director.
>
> **Situation:** The Sales Director wants feature X delivered next week to close a deal, but the Engineering team says it will take 3 weeks and introduce tech debt if rushed.
>
> **Your Task:**
> 1. Draft a response (email or script) to the Sales Director.
> 2. The tone must be collaborative but firm on the timeline.
> 3. Offer a 'Workaround' or an 'MVP version' that can be done sooner to unblock the deal without breaking the platform.
>
> **Key Principle:** Validate their need, but protect the product quality."

### 9. O Engenheiro de Prompt (System Design para IA)
**Quando usar:** Se você estiver construindo features que usam LLMs (como chatbots ou summaries).

> **Prompt:**
> "Act as an LLM Prompt Engineer.
>
> **Goal:** We are building a feature that [INSERT GOAL - e.g., summarizes legal contracts for non-lawyers].
>
> **Your Task:**
> 1. Write the 'System Instruction' (System Prompt) for the AI.
> 2. Include safeguards to prevent hallucinations or legal advice liability.
> 3. Provide 3 'Few-Shot Examples' (Input -> Desired Output) to train the model's behavior.
>
> **Constraint:** The output must be simple, 8th-grade reading level."

### 10. O Agile Coach (Retrospectiva & Melhoria)
**Quando usar:** Para diagnosticar problemas no time e melhorar a velocidade.

> **Prompt:**
> "Act as an Agile Coach.
>
> **Symptom:** My team is consistently missing Sprint goals. The devs complain about 'unclear requirements' and 'too many meetings'.
>
> **Your Task:**
> 1. Diagnose the potential root causes.
> 2. Propose a specific Retrospective Format (e.g., 'Start, Stop, Continue' or 'Sailboat') to discuss this without blaming.
> 3. Suggest 3 concrete Action Items I can take as a PM to fix the 'unclear requirements' issue (e.g., Definition of Ready checklist)."

---
*Criado por [Pablo F. Pulido](https://www.linkedin.com/in/pablofpulido/)*
