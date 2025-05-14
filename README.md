### 🥸🏗️📈 Fundamentos de ETL - Curso Power BI.

- Projeto desenvolvido como prática dos **Fundamentos de ETL** e automação de ingestão de dados, utilizando Python para conectar diferentes fontes e simular um fluxo completo de coleta, transformação e análise de dados.

![OracleTrainingInOhioAwsCertificationTrainingInOhioGIF](https://github.com/user-attachments/assets/acf16631-f0d9-41a8-872a-dfe29907b545)


---

## 🚀 Fundamentos de ETL

**ETL (Extract, Transform, Load)** é um processo fundamental em engenharia e análise de dados. Envolve:

- **Extração (Extract)**: coleta de dados de múltiplas fontes (bancos, APIs, arquivos, filas).
- **Transformação (Transform)**: limpeza, normalização e preparação dos dados.
- **Carga (Load)**: envio dos dados para uma base final (banco de dados, data warehouse, etc.).

Este projeto aplica esse conceito com foco em automação, orquestração e organização de dados para análises futuras.

---

## 🧩 Fontes de Dados Utilizadas

O pipeline se conecta a **4 fontes distintas**:

| Fonte             | Tipo                     | Tecnologia         | Descrição rápida                             |
|-------------------|--------------------------|--------------------|----------------------------------------------|
| Legado            | Arquivo estruturado      | `.txt` (simulado)  | Simula um sistema antigo com layout fixo     |
| Banco SQL         | Relacional               | PostgreSQL         | Consulta registros diretamente via SQL       |
| Fila de Mensagens | Assíncrona               | RabbitMQ           | Consome mensagens em tempo real              |
| Nuvem             | Armazenamento em nuvem   | Azure Blob Storage | Faz download de arquivos de containers Azure |

---

## ⚙️ Funcionalidades

### ✅ Ingestão Agendada
O pipeline é executado automaticamente em intervalos definidos usando o pacote `schedule`.

### ✅ Interface CLI (linha de comando)

Execute partes do pipeline diretamente pelo terminal:

# Executar fonte legado
python main.py --legado

# Executar SQL + Azure
python main.py --sql --azure

### ✅ Interface Web (opcional)
Execute via navegador com Streamlit:
streamlit run app.py

### 💡 Insights Esperados

* Facilitar a integração de diferentes fontes de dados.

* Automatizar a coleta de dados brutos para futuras análises.

* Aprimorar a compreensão de pipelines ETL no contexto real.

* Criar base para geração de relatórios, painéis ou Machine Learning.

### 📊 Resultado Esperado

* Ao final da execução: Os dados extraídos de todas as fontes estarão disponíveis em arquivos .csv ou estruturas de DataFrame.

* Logs de execução serão armazenados e exibidos no terminal.

* Os dados estarão prontos para ser conectado a ferramentas de BI ou módulos de transformação/análise.

### 🛠️ Tecnologias e Bibliotecas

- Python 3.10+

- Pandas

- Psycopg2

- Pika (RabbitMQ)

- Azure Blob Storage SDK

- Schedule

### 📁 Estrutura do Projeto
ETL-DIO-CURSO-POWERBI/
├── README.md
├── requirements.txt
├── config/
│   └── settings.yaml
├── logs/
│   └── pipeline.log
├── data/
│   ├── dados_legado.txt
│   └── baixado.csv
├── src/
│   ├── legado.py
│   ├── postgres.py
│   ├── azure_blob.py
│   ├── fila.py
│   └── scheduler.py
├── main.py
└── app.py  # opcional (interface web)

### 👨‍💻 Autor
Raphael Travassos 
Analista de Dados • Projeto prático para a DIO
