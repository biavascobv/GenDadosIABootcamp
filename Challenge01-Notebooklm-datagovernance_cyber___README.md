# 🛡️ Miniguia de Estudos: Governança de Dados & Cibersegurança (NotebookLM)

> Projeto do desafio **"IA como Ferramenta de Aprendizagem Ativa"** — curso Dados, IA & Cyber (DIO).
> Caderno temático construído no NotebookLM para estudar a interseção entre **Governança de Dados** e **Cibersegurança**.

---

## 🎯 Contexto e Objetivos

### Por que esse tema?

Trabalho como especialista em BI/Analytics há mais de 8 anos, atualmente atuando com Power BI, DAX, SQL e Databricks (camada Gold) em um projeto para um cliente fintech no Reino Unido. No dia a dia, questões de **governança de dados** (quem pode acessar o quê, como os dados são classificados, como garantir rastreabilidade) e de **segurança** (proteção de dados sensíveis, conformidade regulatória) aparecem lado a lado — mas normalmente são tratadas como assuntos separados, um "de negócio" e outro "de TI".

Escolhi este tema porque queria entender melhor **onde governança e cibersegurança se cruzam na prática**: como frameworks de segurança (como o NIST CSF) incorporam governança como pilar formal, e como leis de proteção de dados (como a LGPD) exigem controles que são, ao mesmo tempo, decisões de governança e de segurança da informação.

### Objetivos de estudo

- [ ] Entender os conceitos centrais de governança de dados (propriedade, classificação, qualidade, catalogação) e como eles se relacionam com controles de segurança.
- [ ] Compreender a função **Govern (GV)** do NIST Cybersecurity Framework 2.0 e por que ela foi elevada a pilar próprio na versão 2.0.
- [ ] Mapear as obrigações que a LGPD impõe a áreas técnicas (BI, engenharia de dados, analytics) e como elas se traduzem em controles práticos.
- [ ] Construir um vocabulário técnico consistente entre os dois domínios (governança e segurança), incluindo os termos em inglês mais usados no mercado.
- [ ] Produzir um conjunto de prompts reutilizáveis para revisar esse conteúdo rapidamente no futuro (ex: antes de uma entrevista técnica ou de uma reunião sobre compliance de dados, uma diretriz para produção de código ou tratamento específco ).

---


🌂 GOVERNANÇA & PROTEÇÃO DE DADOS (guarda-chuva)
│
├── 📘 Data Governance (frameworks e papéis)
│     → quem decide, quem é dono do dado, como ele é catalogado e usado
│
├── ⚖️ Data Protection / LGPD (a camada legal)
│     → o que a lei exige na prática, não o texto jurídico cru
│
└── 🔐 Data Security / Cybersecurity (a camada técnica)
      → como proteger o dado de fato: criptografia, hardening, anonimização, ameaças


## 📚 Curadoria de Fontes

Fontes abertas selecionadas e carregadas no NotebookLM (mix de normas oficiais, guias práticos e relatórios de referência — cobrindo governança, privacidade e ameaças):


.

📚 Fontes por tópico
📘 Data Governance (frameworks e papéis)
Fonte	Link
DGI Data Governance Framework	https://datagovernance.com/the-dgi-data-governance-framework/
Os 10 componentes do DGI Framework	https://datagovernance.com/the-dgi-data-governance-framework/dgi-data-governance-framework-components/
NIST Cybersecurity Framework 2.0 — função Govern (papéis e responsabilidades de governança)	https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf
⚖️ Data Protection / LGPD (a camada legal, aplicada)
Fonte	Link
Lei nº 13.709/2018 — LGPD (texto integral)	https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm
Guia de Boas Práticas para Implementação da LGPD (ANPD)	https://www.gov.br/governodigital/pt-br/privacidade-e-seguranca/guias/guia_lgpd.pdf
🔐 Data Security / Cybersecurity (a camada técnica)
Fonte	Link
OWASP Database Security Cheat Sheet (hardening de banco de dados)	https://cheatsheetseries.owasp.org/cheatsheets/Database_Security_Cheat_Sheet.html
OWASP Cryptographic Storage Cheat Sheet (criptografia na prática)	https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html
ENISA Threat Landscape (panorama de ameaças reais)	https://www.enisa.europa.eu/publications
Google Hacking Database — GHDB (Exploit-DB/OffSec) — como buscas expõem bancos de dados	https://www.exploit-db.com/google-hacking-database
Microsoft Presidio — framework open source (Python) para detectar e anonimizar PII	https://microsoft.github.io/presidio/
Presidio aplicado a dados estruturados (DataFrames)	https://microsoft.github.io/presidio/structured/
Presidio + Faker para anonimizar dados antes de enviar a um LLM	https://python.langchain.com/docs/guides/privacy/presidio_data_anonymization
Presidio + PySpark no Microsoft Fabric (Lakehouse/pipelines de dados)	https://blog.fabric.microsoft.com/en-au/blog/privacy-by-design-pii-detection-and-anonymization-with-pyspark-on
      
