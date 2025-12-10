# 🚀 Pipeline ETL com Análise de Sentimento e Tópicos (OpenAI + Pandas)

Este projeto demonstra a criação de um pipeline **E**xtract, **T**ransform, **L**oad (ETL) utilizando a biblioteca Pandas para manipulação de dados e a API da OpenAI (GPT-4o-mini) para enriquecimento dos dados através de Inteligência Artificial.

O objetivo é transformar avaliações de clientes (texto não estruturado) em dados tabulares estruturados, classificando o sentimento e identificando o tópico principal de cada avaliação.

## 🌟 Visão Geral do Projeto

O pipeline é executado em um ambiente Google Colab e segue os seguintes passos:

1.  **Extração (E):** Carrega dados de avaliações de clientes de um arquivo `.csv`.
2.  **Transformação (T):** Itera sobre cada avaliação, enviando o texto para o GPT-4o-mini, que retorna o sentimento (`Positivo`, `Negativo`, `Neutra`) e o tópico principal em formato JSON.
3.  **Carregamento (L):** Persiste os dados originais, enriquecidos com as novas colunas geradas pela IA, em um novo arquivo `.csv`.

## ⚙️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas
* **Transformação por IA:** OpenAI API (GPT-4o-mini)
* **Ambiente de Desenvolvimento:** Google Colab

## 🔒 Configuração e Segurança

Este projeto exige uma chave de API da OpenAI. Para manter a segurança, utilizamos o recurso **Segredos (Secrets)** do Google Colab.

### 1. Requisitos

Certifique-se de ter instalado as bibliotecas necessárias no seu ambiente Colab:

```bash
!pip install openai pandas
