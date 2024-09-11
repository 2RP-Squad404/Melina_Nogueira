# Automação de estratégia de criação de views

**Nome do Estagiário:** Melina Nogueira  
**Data:** /09/2024

---
## **Tarefa**
A partir de um payload json, gerar um modelo com GenAI para criação do script SQLX no Dataform
Apresentar estretégia de criação de views automatizadas utilizando Dataform a partir de um payload json de dados.

---

## **Acompanhamento**

**11/09**
- Comecei criando um arquivo [test.json](arquivos\test.json), para servir de teste;
- Depois criei tópicos no Pub/Sub, um para JSON (`json-input-topic`) e um para SQLX (`sqlx-output-topic`). Junto do tópico do json, foi criado uma assinatura do tipo pull, já que ele enviaria o conteúdo para o modelo do genAI;
- 