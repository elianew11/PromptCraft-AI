PromptCraft AI: Segundo Cérebro para Engenharia de Prompts e Arquitetura de LLMs
Este repositório registra o mapeamento técnico, a diretriz operacional e o histórico de consultas fundamentadas sobre Engenharia de Prompts e Arquitetura de Sistemas RAG (Retrieval-Augmented Generation).
---
🎯 Tema e Objetivo
Tema: Engenharia de Prompts e Arquitetura de LLMs.  
Objetivo: Atuar como consultor técnico para desenvolvedores e pesquisadores, fornecendo respostas claras, precisas e rigorosamente embasadas nas fontes do caderno, cobrindo técnicas de raciocínio de LLMs (como Chain-of-Thought) e arquiteturas de recuperação de informação (estratégias de Chunking para RAG).
---
📚 Fontes Utilizadas e Justificativa de Confiança
O conhecimento compilado neste repositório deriva das fontes do caderno, categorizadas e validadas pela seguinte fundamentação:
Artigos Científicos e Literatura de Fronteira (arXiv / Peer-Reviewed):
`2201.11903v6.pdf` (Wei et al. - Google Research): Artigo seminal que introduziu o Chain-of-Thought Prompting e provou sua emergência em modelos de grande escala (~100B+ parâmetros).
`2210.03629v3.pdf` (Yao et al. - Princeton / Google Brain): Artigo do framework ReAct, demonstrando a integração entre raciocínio verbal e execução de ações externas.
`2305.10601v2.pdf` (Yao et al. - Princeton / DeepMind): Artigo do framework Tree of Thoughts (ToT), introduzindo busca em árvore e autorreflexão para LLMs.
Por que confiamos: São publicações científicas de ponta revisadas por pares e produzidas pelos principais laboratórios de pesquisa em IA do mundo (Google, Princeton, DeepMind).
Guias e Documentações Oficiais de Referência:
`Guia de Engenharia Prompt | Prompt Engineering Guide`: Plataforma de referência aberta e amplamente adotada pela comunidade global de desenvolvimento em IA.
Cursos Especializados e Tutoriais Técnicos:
DeepLearning.AI / Andrew Ng: `Full AI Prompting Course with Andrew Ng` (referência pedagógica global em aprendizado de máquina).
Google: `Google's 9 Hour AI Prompt Engineering Course In 20 Minutes` (diretrizes oficiais de engenharia de prompts da Google).
Frameworks de Mercado (LangChain / LlamaIndex / Agentic AI): Cursos e guias práticos sobre RAG e Agentes (`LangChain Full Course`, `Complete Agentic AI Course`, `How to Chunk Documents for RAG`, `Chunk Size vs Chunk Overlap in RAG Explained`, `RAG Preprocessing Explained`, `RAG Chunking Strategies Explained`, entre outros).
Por que confiamos: Cobrem a implementação prática, padrões de código de produção e arquiteturas de dados reais validadas por engenheiros e desenvolvedores de IA.
---
⚙️ Diretriz de Comportamento do Notebook
A seguinte diretriz (System Prompt) foi definida para governar a atuação do modelo neste caderno:
> *"Você é um Especialista Sênior em Engenharia de Prompts e Arquitetura de LLMs. Sua função é atuar como um consultor técnico para desenvolvedores e pesquisadores. Responda sempre com clareza, precisão e embasamento nas fontes fornecidas no caderno. Ao recomendar técnicas, forneça o raciocínio por trás da escolha e inclua exemplos práticos de prompts ou pseudocódigo quando aplicável. Embase rigorosamente suas afirmações citando as fontes originais e evite extrapolar informações além do material de referência."*
---
❓ Perguntas Realizadas, Respostas e Fontes Associadas
1. Pergunta: "Como funciona a técnica Chain-of-Thought?"
Resumo da Resposta:
A técnica Chain-of-Thought (CoT) reestrutura a geração do LLM para resolver problemas complexos dividindo a resposta em etapas intermediárias de raciocínio explicadas em linguagem natural. Em vez de mapear diretamente a entrada para a saída (Standard Prompting), o CoT aloca mais capacidade computacional sequencial, pois cada token gerado aciona um forward pass adicional. Pode ser implementado via Few-Shot CoT (exemplos com raciocínio) ou Zero-Shot CoT ("Let's think step by step"). Trata-se de uma habilidade emergente de escala, apresentando ganhos significativos em modelos com ~100B+ parâmetros.
Fontes Utilizadas:
`2201.11903v6.pdf` (Wei et al., 2022)
`Chain-of-Thought Prompting - Explained`
`Aula Gratuita: Chain of Thought Prompting (passo a passo)`
`How AI “Thinks” Step by Step`
`Google's 9 Hour AI Prompt Engineering Course In 20 Minutes`
---
2. Pergunta: "Quais são as limitações do Chain-of-Thought?"
Resumo da Resposta:
As principais limitações apontadas incluem:
Dependência de Escala: Ineficaz ou prejudicial em modelos menores (<10B a 60B parâmetros), gerando raciocínios ilógicos.
Ausência de Garantia Lógica: Risco de alucinação ou falsos positivos (raciocínio errado com resposta final correta).
Raciocínio Estático/Fechado: Ausência de conexão com o mundo externo (APIs, bancos de dados ou busca web), motivando técnicas como ReAct.
Alto Custo Computacional: Aumento drástico na contagem de tokens intermediários, gerando maior latência e custo de inferência.
Ineficiência em Tarefas Simples: Overhead desnecessário em problemas diretos de passo único.
Custo de Anotação: Alto esforço humano para criar datasets de raciocínio para fine-tuning.
Fontes Utilizadas:
`2201.11903v6.pdf`
`2210.03629v3.pdf` (ReAct)
`2305.10601v2.pdf` (Tree of Thoughts)
`Chain-of-Thought Prompting - Explained`
---
3. Pergunta: "Como funcionam as estratégias de chunking?"
Resumo da Resposta:
No contexto de RAG, chunking é o processo de segmentação de documentos extensos em blocos menores (chunks) antes da geração de embeddings e armazenamento vetorial. Ele é essencial para respeitar limites de janela de contexto e otimizar a precisão da busca. Os parâmetros principais são Chunk Size (tamanho do bloco) e Chunk Overlap (sobreposição entre blocos adjacentes). As 6 estratégias principais são:
Fixed-Size Chunking (divisão rígida por caracteres/tokens).
Sliding Window / Overlap (janela deslizante com sobreposição).
Recursive / Structure-Aware Chunking (respeita a hierarquia do texto: parágrafos, frases, palavras).
Sentence & Paragraph Chunking (unidades gramaticais completas).
Semantic Chunking (divisão por mudança de similaridade vetorial/tópico).
Hierarchical / Metadata-Aware Chunking (blocos pequenos para busca vinculados a blocos pai/metadados).
Fontes Utilizadas:
`Chunk Size vs Chunk Overlap in RAG Explained`
`How to Chunk Documents for RAG`
`RAG Chunking Strategies Explained`
`RAG Preprocessing Explained`
`LangChain Full Course in One Shot`
`Complete Agentic AI Course`
---
Documentação gerada para compor o repositório de referência em Engenharia de Prompts e Arquitetura RAG.
