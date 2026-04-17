---
titulo: Como LLMs funcionam
criado: 2025-01-01
tags: [permanente, ia, llm]
status: em-desenvolvimento
---

# Como LLMs funcionam

## 💡 Ideia Central

> LLMs são modelos que aprenderam padrões estatísticos de enormes corpora de texto e geram a próxima palavra mais provável dado um contexto — mas emergem capacidades surpreendentes desse processo simples.

---

## 🧠 Desenvolvimento

### O processo de treinamento

1. **Pré-treinamento** — O modelo vê bilhões de tokens e aprende a prever o próximo. Aqui emergem o conhecimento e raciocínio.
2. **Fine-tuning supervisionado (SFT)** — Humanos mostram exemplos de boas respostas.
3. **RLHF** — Feedback humano treina um modelo de recompensa que guia o comportamento.

### Por que funcionam tão bem?

A atenção (*attention mechanism*) permite que o modelo pese a relevância de cada token do contexto ao gerar cada palavra. Isso cria uma espécie de "memória de curto prazo" dentro da janela de contexto.

### Limitações importantes

- Não têm memória entre conversas (sem contexto externo)
- Podem alucinar — geram texto fluente mas factualmente errado
- Conhecimento cortado na data de treinamento

---

## 🔗 Conexões

- Expande: [[RAG — Retrieval Augmented Generation]]
- Relacionado com: [[Prompt Engineering — técnicas]]
- Relacionado com: [[Embeddings e Bancos Vetoriais]]

#permanente #ia #llm
