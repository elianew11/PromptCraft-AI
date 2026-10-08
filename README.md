# PromptCraft AI: Segundo Cérebro para Engenharia de Prompts e Arquitetura de LLMs

## 🎯 Tema e Objetivo
**Tema:** Engenharia de Prompts e Arquiteturas Avançadas de LLMs.  
**Objetivo:** Criar uma base de conhecimento interativa no Gemini Notebook que atue como um consultor técnico sênior para desenvolvedores, pesquisadores e engenheiros de IA, auxiliando no design de prompts, escolha de modelos, técnicas de encadeamento (*chaining*) e arquiteturas RAG (*Retrieval-Augmented Generation*).

---

## 📚 Fontes Utilizadas e Causalidade de Confiança

Para garantir o rigor técnico, o alinhamento com a indústria e a ausência de alucinações, foram selecionadas as seguintes fontes de dados:

### 1. Artigos Acadêmicos Fundamentais (Papers do arXiv)
* **[Chain-of-Thought Prompting Elicits Reasoning in Large Language Models (Wei et al., 2022)](https://arxiv.org/abs/2201.11903)**  
  * *Por que é confiável:* É o trabalho seminal publicado pela equipe do Google Research que introduziu e validou cientificamente a técnica de raciocínio passo a passo em LLMs.
* **[ReAct: Synergizing Reasoning and Acting in Language Models (Yao et al., 2022)](https://arxiv.org/abs/2210.03629)**  
  * *Por que é confiável:* Desenvolvido em parceria entre a Universidade de Princeton e o Google Research, é o paper que estabeleceu a base teórica e prática para o funcionamento de Agentes Autônomos de IA.
* **[Tree of Thoughts: Deliberate Problem Solving with Large Language Models (Yao et al., 2023)](https://arxiv.org/abs/2305.10601)**  
  * *Por que é confiável:* Trabalho de referência internacional em resolução de problemas lógicos e estratégicos em LLMs via busca em árvore.

### 2. Documentação e Guias Técnicos
* **[Prompt Engineering Guide (DAIR.AI)](https://www.promptingguide.ai/)**  
  * *Por que é confiável:* É a documentação open-source de referência global mantida por pesquisadores e especialistas de mercado, amplamente adotada pela comunidade de IA.

### 3. Tutoriais e Análises em Vídeo (YouTube)
* **Vídeos selecionados de canais como *DeepLearning.AI* e *LangChain***  
  * *Por que são confiáveis:* Produzidos por referências globais do setor (como Andrew Ng e a equipe do LangChain), fornecendo a visão de implementação de código, integração de APIs e arquitetura de RAG do mundo real.

---

## ⚙️ Diretriz de Comportamento (Prompt de Sistema)

A seguinte instrução (System Instructions) foi configurada para orientar a persona e as respostas do Gemini Notebook:

> *"Você é um Especialista Sênior em Engenharia de Prompts e Arquitetura de LLMs. Sua função é atuar como um consultor técnico para desenvolvedores e pesquisadores. Responda sempre com clareza, precisão e embasamento nas fontes fornecidas no caderno. Ao recomendar técnicas, forneça o raciocínio por trás da escolha e inclua exemplos práticos de prompts ou pseudocódigo quando aplicável. Embase rigorosamente suas afirmações citando as fontes originais e evite extrapolar informações além do material de referência."*

---

## 🧪 Perguntas, Respostas e Citações de Fontes

*(Substitua os textos abaixo pelos testes reais realizados no seu Gemini Notebook)*

### Teste 1: Comparação de Técnicas
* **Pergunta feita:**  
  > *"Com base nas fontes fornecidas, qual a diferença prática entre as técnicas Chain-of-Thought (CoT) e ReAct, e quando devo usar cada uma?"*
* **Resposta gerada:**  
  > *"A técnica Chain-of-Thought (CoT) foca em decompor problemas complexos de raciocínio em etapas intermediárias antes da resposta final. Já a técnica ReAct combina o raciocínio em etapas (Reasoning) com a capacidade de executar ações externas (Acting), como consultar APIs ou bases de dados. Use CoT para tarefas exclusivamente analíticas/lógicas e ReAct quando o modelo precisar interagir com ferramentas externas."*
* **Fontes citadas:**  
  * Paper *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models* (Wei et al.)  
  * Paper *ReAct: Synergizing Reasoning and Acting in Language Models* (Yao et al.)

---

### Teste 2: Refatoração de Prompt
* **Pergunta feita:**  
  > *"Tenho um prompt simples: 'Analise este texto e diga os erros'. Como posso refatorá-lo usando as melhores práticas da documentação?"*
* **Resposta gerada:**  
  > *"Para refatorar este prompt, adicione a atribuição de papel (Role Prompting), delimitação do texto de entrada e especificação do formato de saída esperado. Exemplo refatorado: 'Atue como um revisor gramatical sênior. Analise o texto delimitado por ###. Liste os erros encontrados em formato de tabela contendo: Erro, Tipo e Sugestão de Correção.'"*
* **Fontes citadas:**  
  * *Prompt Engineering Guide (DAIR.AI)*

---

## 🔗 Link do Gemini Notebook Compartilhado

* 📌 **Acesse o caderno completo:** [Cole aqui o link de compartilhamento do seu Gemini Notebook]
