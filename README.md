# 📚 Miniguia de Estudos: Inteligência Artificial e Engenharia de Prompts

> **Projeto Prático da DIO** | Construção de Caderno Temático no **NotebookLM** e Documentação de Aprendizagem Ativa.

---

## 🎯 Contexto e Objetivos

Este repositório foi criado como parte do desafio prático da plataforma **DIO (Digital Innovation One)**. O objetivo é demonstrar o uso da Inteligência Artificial como ferramenta de **aprendizagem ativa**, combinando curadoria de fontes de qualidade, engenharia de prompts e pensamento crítico.

### 🎯 Objetivos de Estudo:
* Compreender os fundamentos da **Engenharia de Prompts**.
* Aprender e catalogar as principais técnicas de estruturação de mensagens para IAs Gerativas.
* Identificar boas práticas e estratégias para mitigar alucinações de LLMs.
* Criar um repositório reutilizável de prompts para consultas futuras.

---

## 📚 Curadoria de Fontes

Para alimentar e embasar o **Caderno Temático no NotebookLM**, foram selecionadas 4 fontes abertas de referência internacional sobre o tema:

1. **[OpenAI - Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering)**  
   * *Descrição:* Documentação oficial de boas práticas e estratégias recomendadas pela OpenAI.
2. **[DAIR.AI - Prompt Engineering Guide](https://www.promptingguide.ai/pt)**  
   * *Descrição:* Guia completo e em português contendo teorias, técnicas e papers sobre Engenharia de Prompts.
3. **[Google Cloud - Visão Geral de Design de Prompts](https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/introduction-prompt-design)**  
   * *Descrição:* Conceitos fundamentais de estruturação e parametrização de modelos no ambiente Google Vertex AI.
4. **[FreeCodeCamp - How to Write Effective Prompts for AI](https://www.freecodecamp.org/news/how-to-write-effective-prompts-for-ai/)**  
   * *Descrição:* Tutorial prático direcionado a iniciantes e desenvolvedores.

---

## 🧪 Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Durante a interação com o NotebookLM, foram testados prompts estratégicos para extrair o conhecimento das fontes. Abaixo estão registrados o raciocínio, o prompt utilizado e os resultados obtidos.

### 🔹 Teste 1: Conceito e Pilares
* **Prompt:** *"Com base nas fontes fornecidas, explique de forma simples e direta o que é Engenharia de Prompts e quais são os seus principais pilares ou boas práticas."*
* **Resultado Obtido:** A IA identificou que a Engenharia de Prompts é o processo de projetar instruções eficazes para LLMs e destacou componentes como Tarefa, Identidade, Exemplos e Contexto, além de sugerir o uso de marcas em Markdown e tags XML.

### 🔹 Teste 2: Mitigação de Alucinações (Troubleshooting)
* **Prompt:** *"Quais são as melhores estratégias citadas nos textos para evitar alucinações da IA e garantir respostas mais precisas? Dê exemplos práticos de como estruturar o prompt."*
* **Dificuldade/Cicatriz:** Para evitar que o modelo inventasse respostas gerais da internet, foi necessário reforçar nas instruções do prompt para ele consultar **estritamente** a seção de contexto.
* **Resultado Obtido:** A IA sugeriu uma estrutura completa utilizando tags XML (`<contexto>`, `<pergunta>`, `<exemplo>`) e regras explícitas para declarar quando uma informação não for encontrada no material de apoio.

### 🔹 Teste 3: Comparativo de Técnicas
* **Prompt:** *"Crie uma tabela ou lista resumida comparando 3 técnicas de prompting diferentes presentes nas fontes (por exemplo: Zero-Shot, Few-Shot e Chain-of-Thought)."*
* **Resultado Obtido:** Síntese em formato de tabela comparando o funcionamento e os benefícios de cada abordagem.

---

## 📖 Miniguia de Estudo (Entrega Final)

### 📌 Resumos Estruturados do Assunto
* **Engenharia de Prompts:** Conjunto de habilidades e estratégias para instruir modelos de linguagem a realizarem tarefas específicas com qualidade e segurança.
* **Ancoragem (Grounding / RAG):** Técnica que limita a resposta da IA a documentos e dados fornecidos pelo usuário, reduzindo drasticamente o risco de alucinações fáticas.
* **Decomposição de Tarefas:** Dividir um problema complexo em sub-tarefas encadeadas (*Prompt Chaining*) garante maior precisão e controle sobre a resposta.

### 📖 Glossário de Conceitos Aprendidos
* **Zero-Shot Prompting:** Enviar uma instrução direta ao modelo sem fornecer nenhum exemplo prévio.
* **Few-Shot Prompting:** Incluir demonstrações de "entrada ➔ saída" no próprio prompt para calibrar o tom, formato e estilo da resposta.
* **Chain-of-Thought (CoT):** Estimular o modelo a explicar seu raciocínio passo a passo antes de apresentar a conclusão final.
* **Alucinação:** Quando a IA gera informações incorretas, inventadas ou desconectadas da realidade com aparência de verdade.
* **Tags XML:** Marcadores usados para organizar e delimitar seções de texto (ex: `<instrucoes>`, `<contexto>`).

### 📊 Tabela Comparativa de Técnicas
| Técnica | Como Funciona | Principais Aplicações |
| :--- | :--- | :--- |
| **Zero-Shot** | Instrução direta sem exemplos prévios. | Tarefas simples e diretas. |
| **Few-Shot** | Inclusão de exemplos de "entrada e saída". | Padronização de formato, tom e estilo. |
| **Chain-of-Thought** | Estímulo ao raciocínio lógico passo a passo. | Resolução de problemas complexos e cálculos. |

---

## 🛠️ Prompts Reutilizáveis para Revisões Futuras

Abaixo está o modelo de **Prompt Estruturado Padrão** desenvolvido para reutilização em estudos futuros:

```text
# Identidade
Você é um especialista em ensino e síntese de conhecimento focado em clareza e precisão.

# Instruções
1. Analise o material contido na seção <contexto>.
2. Responda à pergunta utilizando apenas os fatos presentes nas fontes.
3. Se a resposta não estiver no contexto, responda: "Informação não encontrada no material de referência."
4. Pense passo a passo antes de formular a resposta.

# Contexto
<contexto>
[Cole aqui seus resumos, artigos ou notas de estudo]
</contexto>


Projeto desenvolvido por Ângelo Oliveira como entrega de desafio na plataforma DIO.

# Pergunta
<pergunta>
[Insira sua dúvida aqui]
</pergunta>
