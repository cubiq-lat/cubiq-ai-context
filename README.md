# cubiq-ai-context
Centralized knowledge base for AI agents working with Cubiq projects.

# 🤖 Cubiq AI Context & Memory

> **Impulsionados por IA, geridos por humanos: criamos, operamos e escalamos negócios digitais em LATAM 🚀**

---

## 📌 Sobre Este Repositório

Este repositório centraliza toda a **memória institucional, diretrizes e contexto** necessários para que Inteligências Artificiais (LLMs) trabalhem alinhadas com a **Cubiq**.

Funciona como uma **Fonte Única de Verdade (Single Source of Truth)** para agentes de IA, assistentes de código (Cursor, Copilot) e fluxos de automação. O objetivo é garantir consistência, qualidade e aderência à nossa identidade em todas as interações.

---

## 🏢 Identidade Cubiq

*Esta seção define o "quem somos" para qualquer IA que acesse este repositório.*

### Visão Geral
A Cubiq é uma **Software Factory orientada a produtos**, atuando como **Plataforma Digital para PMEs** e **Backend-as-a-Service (BaaS) para Startups** na região da LATAM.

### Pilares de Atuação
1.  **Plataforma Digital para PMEs:** Foco em transformação digital, escalabilidade e otimização de processos. Entregamos soluções tecnológicas que resolvem dores de mercado, permitindo que pequenas e médias empresas cresçam com estrutura de nível enterprise.
2.  **Backend-as-a-Service (BaaS) para Startups:** Fornecemos a infraestrutura de backend necessária para que startups reduzam seu *time-to-market*. Focamos em permitir que founders validem suas ideias e escalem seus produtos sem a fricção de construir do zero.
3.  **Diferencial Competitivo (O DNA Cubiq):**
    *   **IA + Humanos:** A tecnologia (IA) é utilizada para ganho de escala e eficiência, enquanto a gestão humana atua como o filtro crítico de qualidade, estratégia e viabilidade de negócio.
    *   **Orientação a Produto:** Não somos uma fábrica de código passiva. Entendemos o negócio, o usuário final e o objetivo comercial antes da implementação.

### Diretrizes de Tom de Voz
*   **Autoridade:** Falamos como especialistas que dominam o ecossistema de tecnologia e negócios na LATAM.
*   **Direto e Prático:** Evitamos excesso de jargões técnicos. O foco é valor e resultado.
*   **Humano e Confiável:** Valorizamos a curadoria humana em nossos processos automatizados.
*   **Ambição:** Focados em "criar, operar e escalar".

### Objetivos Estratégicos
*   Ser o parceiro tecnológico definitivo para a jornada de crescimento de negócios digitais.
*   Democratizar o acesso a desenvolvimento de alta performance.
*   Estabelecer a Cubiq como referência em qualidade e eficiência no mercado de desenvolvimento da América Latina.

---

## 📁 Estrutura do Repositório

```text
.
├── README.md                 # Você está aqui
├── llms.txt                  # Padrão para descoberta automática por LLMs
├── .cursorrules              # Regras específicas para IDE Cursor
├── context/
│   ├── company_profile.md    # Detalhes expandidos sobre a identidade Cubiq
│   ├── tech_stack.md         # Stack tecnológico preferencial (Langs, Cloud, DB)
│   ├── coding_standards.md   # Padrões de código, linting e testes
│   ├── product_logic.md      # Regras de negócio para PMEs e Startups
│   └── latam_guidelines.md   # Considerações regionais (i18n, compliance)
├── prompts/
│   ├── code_review.md        # Prompt base para review de código
│   ├── feature_spec.md       # Prompt base para geração de especificações
│   └── support tone.md       # Diretrizes para atendimento ao cliente
└── .gitignore                # Ignora secrets, .env e arquivos locais