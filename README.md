# Introdução

---

O projeto em questão tem como objetivo analisar a estratégia de releases presentes no repositório [MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo), utilizando de LLMs para tal. A realização do projeto ocorreu mediante a etapa de análise manual, seguida da análise com LLMs.

# Análise Manual do Projeto

---

Inicialmente foram feitas análises manuais no projeto investigando o escopo do projeto, seus pull requests, commits, configuração de branches, forks e contribuidores. Para assim termos uma base da frequência e análise a qual as LLMs deveriam retornar.

# Análise com LLMs

---

Utilizamos algumas LLMs do [HuggingFace](https://huggingface.co/models), aqui estão as LLMs escolhidas e o por quê de sua escolha.

|                                             Modelo(s)                                              |                                                                                                                                                                                  Justificativa                                                                                                                                                                                  |
| :------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| [<i>meta-llama/Llama-3.2-3B-Instruct</i>](https://huggingface.co/meta-llama/Llama-3.2-3B-Instruct) | O LLaMA 3B é particularmente adequado para essa tarefa porque possui forte capacidade de mapeamento entre observações empíricas e modelos conceituais abstratos, mesmo quando as observações são escassas ou incompletas. Dessa forma, ele não força a existência de um padrão no projeto quando não há e identifica implementações parciais de padrões de branches e releases. |
|    [<i>Mistral-7B-Instruct-v0.2</i>](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.3)    |                                        O Mistral 7B se destaca por um perfil mais operacional e descritivo, com menor tendência a extrapolação conceitual. Isso é desejável em projetos pequenos. O modelo tende a descrever o que efetivamente ocorre no repositório, em vez de tentar encaixar o comportamento em um framework formal.                                        |
|   [<i>Qwen/Qwen2.5-Coder-3B-Instruct</i>](https://huggingface.co/Qwen/Qwen2.5-Coder-3B-Instruct)   |                          O Qwen Coder 3B consegue separar inferência conceitual de verificação factual, sendo uma boa escolha para essa análise. O modelo foi treinado para lidar com nomes e papéis de branches, histórico de commits, tags e releases. Essas constatações servem como fundamentação empírica para as conclusões dos outros modelos.                           |

# Como executar

---

Para executar, basta baixar os arquivos da pasta colab_notebooks e fazer upload no [GoogleColab](https://colab.google/). Cada arquivo representa um notebook diferente no colab e deve ser executado separadamente. As dependências necessárias serão baixadas automaticamente ao executar. Um tutorial mais detalhado se encontra no relatório, localizado na pasta docs deste repositório ou através do link abaixo.

# Links úteis

---

Relatório da atividade, contendo uma análise e explicação mais aprofundada do projeto: [Relatório](https://docs.google.com/document/d/13JeSUXYwiZQ4xPF2bBD3F7DLP3tkuZYV6Az2UTz_q3k/edit?tab=t.0)

Vídeo explicando o trabalho realizado:

[Vídeo](https://drive.google.com/file/d/1QRbIvG6-zgJnzAhjgf_Tbnc6klCskXNz/view?usp=drive_link)

# Relação dos participantes

---

|             Nome             |  Matrícula   |                                                                                   Contribuição                                                                                    |
| :--------------------------: | :----------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|   Fernanda da Silva Santos   | 202300061581 |                            Uso da LLM meta-llama/Llama-3.2-3B-Instruct para análise dos metadados do projeto, escrita do relatório, gravação do vídeo.                            |
| Gustavo Rodrigues dos Santos | 202300061939 | Uso da LLM Qwen2.5-Coder-3B-Instruct (com quantização 4-bit) para auditoria técnica detalhada de fluxo de trabalho, ritmo de releases e gravação do vídeo e revisão do relatório. |
|      Joao Santos Rocha       | 202300061948 |                   Uso da LLM Mistral-7B-Instruct-v0.2 (com quantização 4-bit) para análise da governança do projeto, escrita do relatório e gravação do vídeo.                    |
| Jose Henrique Souza Santana  | 202300061699 |                                  Análise manual no repositório, escrita do relatório, gravação do vídeo, auxílios gerais aos demais integrantes.                                  |
|   Jose Luiz de Jesus Souza   | 201800138910 |                                                                   O integrante não contribuiu com a atividade.                                                                    |
|     Lais Santos de Sousa     | 202100115364 |                            Uso da LLM meta-llama/Llama-3.2-3B-Instruct para análise dos metadados do projeto, escrita do relatório, gravação do vídeo.                            |
|    Rafael de Jesus Santos    | 202300114489 |            Uso da LLM Qwen2.5-Coder-3B-Instruct (com quantização 4-bit) para auditoria técnica detalhada de fluxo de trabalho e ritmo de releases e gravação do vídeo             |
|   Tasso Marcel de Oliveira   | 202300061984 |                   Uso da LLM Mistral-7B-Instruct-v0.2 (com quantização 4-bit) para análise da governança do projeto, escrita do relatório e gravação do vídeo.                    |
