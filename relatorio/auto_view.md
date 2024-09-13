# Automação de estratégia de criação de views

**Nome do Estagiário:** Melina Nogueira  
**Data:** 13/09/2024

---
## **Tarefa**
A partir de um payload json, gerar um modelo com GenAI para criação do script SQLX no Dataform
Apresentar estretégia de criação de views automatizadas utilizando Dataform a partir de um payload json de dados.

1º Criar tabela com dados aleatórios com varias colunas
2º Pedir para a IA criar um payload JSON complexo com grandes volumes de dados correspondentes as colunas e a tabela criada anteriormente
3º Verificar o arquivo JSON
4º Pedir para a IA gerar com base no arquivo JSON um script SQLX
5º Gerar a view no dataform

---

## **O que foi feito**

**11/09**
Neste dia ainda não tinhamos certeza do que fazer, porém comecei a explorar ferramentas que poderiamos utilizar.
- Comecei criando um arquivo [test.json](arquivos\test.json), para servir de teste;
- Depois criei tópicos no Pub/Sub, um para JSON (`json-input-topic`) e um para SQLX (`sqlx-output-topic`). Junto do tópico do json, foi criado uma assinatura do tipo pull, já que ele enviaria o conteúdo para o modelo do genAI.

**12/09**
No final do dia recebemos um suporte o que facilitou a compreensão do que deveria ser realizado até o momento.
- Criei um bucket para armazenar meu arquivo json;
- Criei uma função para meu Pub/Sub receber o arquivo json;

**13/08**
- Comecei pedindo para o ChatGPT me gerar uma tabela pequena apenas para simulação, e utilizando o Gemini, a tabela foi convertida para um arquivo JSON e após a verificação para garantir que havia sido convertido corretamente, transformei em um arquivo SQLX para criar a view, com a ajuda de uma colega;
- Logo após importei as duas tabelas utilizadas anteriormente (`purchases` e `campaign`), e fiz o mesmo processo de transformação com o Gemini;
- Criei uma view referente a tabela purchases (`view1`) e outra referente a tabela campaign (`view2`).

---

## **Resultado**
- Tive um pouco de dificuldade para trabalhar com o Gemini e conseguir criar a primeira view, porém logo após entender como era feito, eu realizei as tarefas sem dificuldade;
- Pretendo criar outras views, selecionando apenas algumas colunas, ou até mesmo com outras tabelas.

---

## **Dúvidas**
- Ainda tenho dúvidas sobre o funcionamento do Gemini, por exemplo o comportamento dele e as suas respostas referentes a tabelas com esquemas diferentes.