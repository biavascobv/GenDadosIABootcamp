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
- [ ] Produzir um conjunto de prompts reutilizáveis para revisar esse conteúdo rapidamente no futuro (ex: antes de uma entrevista técnica ou de uma reunião sobre compliance de dados).

---

## 📚 Curadoria de Fontes

Fontes abertas selecionadas e carregadas no NotebookLM (mix de normas oficiais, guias práticos e relatórios de referência — cobrindo governança, privacidade e ameaças):

| # | Fonte | Tipo | Por que foi escolhida |
|---|-------|------|------------------------|
| 1 | [NIST Cybersecurity Framework (CSF) 2.0](https://www.nist.gov/cyberframework) | Framework técnico (PDF/HTML) | Referência global de segurança; a versão 2.0 adicionou a função **Govern**, conectando explicitamente governança e cibersegurança. |
| 2 | [Lei nº 13.709/2018 — LGPD](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) | Texto legal (BR) | Base regulatória brasileira; define papéis (controlador, operador, DPO) e princípios que sustentam qualquer programa de governança de dados no Brasil. |
| 3 | [Guia de Boas Práticas para Implementação da LGPD (ANPD/Governo Federal)](https://www.gov.br/governodigital/pt-br/privacidade-e-seguranca/guias/guia_lgpd.pdf) | Guia prático (PDF) | Traduz a lei em passos operacionais — útil para conectar teoria jurídica com rotina de um time de dados. |
| 4 | [NIST Privacy Framework 1.1](https://www.nist.gov/privacy-framework) | Framework técnico (PDF) | Foi redesenhado para ter a mesma estrutura do CSF 2.0, facilitando o uso conjunto de gestão de privacidade e de risco cibernético — ótimo para comparar com a fonte 1. |
| 5 | [ENISA Threat Landscape (relatório anual)](https://www.enisa.europa.eu/publications) | Relatório de referência (PDF) | Dá o "porquê" da governança: mostra quais ameaças e vetores de ataque tornam controles de dados necessários na prática. |

> 💡 **Como usei no NotebookLM:** fiz upload dos 5 documentos (ou dos links, quando o NotebookLM permite importar por URL) como fontes de um único caderno chamado *"Governança de Dados & Cibersegurança"*, para poder fazer perguntas cruzadas entre eles.

---

## 🧠 Engenharia de Prompts e "Cicatrizes"

> Esta seção documenta o raciocínio por trás das perguntas — não só o resultado, mas as tentativas que não funcionaram bem e como ajustei o prompt.
> **📝 Preencha os campos `[cole aqui a resposta do NotebookLM]` com as respostas reais que você recebeu ao rodar cada prompt no seu caderno.**

### Rodada 1 — Perguntas exploratórias (abertura do tema)

**Prompt inicial (muito genérico):**
```
O que é governança de dados?
```
**Problema encontrado:** resposta correta, mas rasa — o NotebookLM apenas parafraseou uma fonte, sem cruzar com as demais nem trazer a conexão com segurança.

**Prompt ajustado (mais estratégico):**
```
Com base nas fontes carregadas, explique como o conceito de governança de dados
aparece no NIST CSF 2.0 e como ele se relaciona com os princípios da LGPD.
Cite explicitamente de qual documento vem cada ideia.
```
**Resposta obtida:** `[cole aqui a resposta do NotebookLM]`

**Aprendizado:** pedir para a IA **citar a fonte de cada afirmação** obriga o NotebookLM a cruzar os documentos em vez de responder com uma única fonte — e facilita conferir se ele não está inventando nada (alucinação).

---

### Rodada 2 — Aprofundamento técnico

**Prompt:**
```
Quais são as funções do NIST CSF 2.0? Explique em detalhe a função "Govern" e
por que ela é considerada uma novidade importante em relação à versão 1.1.
```
**Resposta obtida:** `[cole aqui a resposta do NotebookLM]`

**Prompt:**
```
Compare os papéis de "controlador" e "operador" definidos na LGPD com os
conceitos de "data owner" e "data steward" usados em governança de dados.
Existe equivalência? Onde as fontes divergem ou não cobrem o assunto?
```
**Resposta obtida:** `[cole aqui a resposta do NotebookLM]`

**Dificuldade encontrada (troubleshooting):** ao pedir comparação entre um termo jurídico brasileiro (LGPD) e um termo de mercado em inglês (não presente nas fontes), o NotebookLM tende a **generalizar demais ou misturar conceitos**. Foi preciso adicionar a instrução explícita *"se o conceito não estiver em nenhuma fonte, diga isso claramente em vez de inferir"* para reduzir esse risco.

---

### Rodada 3 — Aplicação prática / conexão com o mercado

**Prompt:**
```
Imagine uma equipe de BI que trabalha com um cliente do setor financeiro no
Reino Unido usando Power BI e Databricks. Com base nas fontes sobre NIST CSF,
LGPD e ENISA Threat Landscape, liste 5 riscos práticos de governança/segurança
que essa equipe deveria monitorar e a que framework/fonte cada risco se conecta.
```
**Resposta obtida:** `[cole aqui a resposta do NotebookLM]`

**Aprendizado:** dar um **cenário concreto e familiar** (em vez de pedir teoria pura) gera respostas muito mais úteis para revisão futura — é o tipo de prompt que vale a pena guardar como reutilizável (ver seção final).

---

### Cicatrizes gerais (resumo do troubleshooting)

- Perguntas genéricas → respostas rasas de uma fonte só. **Solução:** sempre pedir cruzamento explícito entre fontes.
- Termos fora do escopo das fontes → risco de alucinação. **Solução:** instruir a IA a admitir lacunas.
- Perguntas muito teóricas → respostas difíceis de aplicar depois. **Solução:** ancorar prompts em cenários práticos do seu contexto de trabalho.
- `[adicione aqui outras dificuldades reais que você encontrou ao testar]`

---

## 📖 Miniguia de Estudo (Entrega Final)

### 🔹 Resumos estruturados

**1. Governança de dados — o essencial**
Governança de dados é o conjunto de políticas, papéis e processos que definem **quem é responsável por quê** em relação aos dados de uma organização: quem pode acessar, como os dados são classificados por sensibilidade, como a qualidade é garantida e como mudanças são rastreadas. Sem governança, controles de segurança técnica (criptografia, controle de acesso) perdem eficácia, porque ninguém sabe ao certo o que precisa ser protegido nem quem é o responsável.

**2. NIST Cybersecurity Framework (CSF) 2.0 — a função Govern**
O CSF 2.0 organiza a gestão de risco cibernético em seis funções: **Govern, Identify, Protect, Detect, Respond, Recover**. A grande mudança da versão 2.0 foi elevar **Govern** a função própria (antes era tratada apenas como parte de "Identify"), reconhecendo que decisões de governança — estratégia de risco, papéis, políticas, gestão de fornecedores — são pré-requisito para que as demais funções técnicas funcionem. Isso reflete exatamente a interseção que este projeto explora: segurança técnica sem governança é reativa; governança sem controles técnicos é apenas papel.

**3. LGPD — a base legal brasileira**
A Lei nº 13.709/2018 (LGPD) regula o tratamento de dados pessoais no Brasil, com base em princípios como respeito à privacidade, autodeterminação informativa e livre desenvolvimento da personalidade. Ela define papéis centrais para qualquer programa de governança — **controlador** (quem decide o tratamento), **operador** (quem trata em nome do controlador) e a **ANPD** (autoridade fiscalizadora) — e é aplicável a qualquer organização que trate dados de pessoas localizadas no Brasil, independentemente de onde a empresa está sediada.

**4. NIST Privacy Framework — a ponte entre privacidade e segurança**
Redesenhado para compartilhar a mesma estrutura do CSF 2.0, o NIST Privacy Framework facilita a gestão conjunta de risco de privacidade e de risco cibernético — em vez de tratá-los como programas paralelos e desconectados, como costuma acontecer na prática.

**5. ENISA Threat Landscape — o "porquê" da governança**
O relatório anual da ENISA (agência de cibersegurança da União Europeia) mapeia as principais ameaças e tendências de ataque na Europa. Ele mostra, de forma concreta, por que controles de governança (classificação de dados, gestão de acesso, resposta a incidentes) não são burocracia: são resposta direta a padrões de ataque reais e recorrentes.

`[depois de rodar seus prompts no NotebookLM, enriqueça estes resumos com os pontos específicos que a IA destacou e que você achou mais relevantes]`

---

### 🔹 Glossário

| Termo | Definição |
|---|---|
| **Governança de Dados** | Conjunto de políticas, papéis e processos que definem responsabilidade, qualidade e uso adequado dos dados de uma organização. |
| **Data Owner / Proprietário do Dado** | Pessoa ou área responsável por decisões sobre um determinado conjunto de dados. |
| **Data Steward** | Papel operacional responsável por aplicar as políticas de governança no dia a dia (qualidade, catalogação, documentação). |
| **CSF (Cybersecurity Framework)** | Framework do NIST para gestão de risco cibernético, estruturado em seis funções: Govern, Identify, Protect, Detect, Respond, Recover. |
| **Função Govern (GV)** | Função do CSF 2.0 dedicada a estratégia de risco, políticas, papéis e supervisão — a "camada de governança" da segurança cibernética. |
| **LGPD** | Lei Geral de Proteção de Dados Pessoais (Lei nº 13.709/2018), lei brasileira que regula o tratamento de dados pessoais. |
| **Controlador** | Na LGPD, quem toma as decisões sobre o tratamento de dados pessoais. |
| **Operador** | Na LGPD, quem realiza o tratamento de dados em nome do controlador. |
| **ANPD** | Autoridade Nacional de Proteção de Dados — órgão fiscalizador da LGPD no Brasil. |
| **Privacy by Design** | Princípio de incorporar proteção de dados desde a concepção de um sistema ou processo, não como correção posterior. |
| **Threat Landscape** | Panorama das ameaças, técnicas de ataque e tendências de risco cibernético observadas em um período. |
| **Classificação de Dados** | Processo de categorizar dados por nível de sensibilidade (ex: público, interno, confidencial, restrito) para aplicar controles proporcionais. |

`[adicione termos novos que aparecerem nas respostas do NotebookLM]`

---

### 🔹 Prompts reutilizáveis (para revisão futura)

Guarde estes prompts para revisitar o tema rapidamente no futuro (ex: antes de uma entrevista ou reunião):

1. **Revisão rápida de conceito:**
   `"Resuma em 5 bullets o conceito de [TERMO] com base nas fontes, citando de qual documento vem cada ponto."`

2. **Comparação entre fontes:**
   `"Compare como [FONTE A] e [FONTE B] tratam o tema [ASSUNTO]. Onde elas concordam e onde divergem?"`

3. **Aplicação prática:**
   `"Dado um cenário onde [DESCREVA SEU CONTEXTO DE TRABALHO], quais riscos de governança/segurança das fontes se aplicam e como eu mitigaria cada um?"`

4. **Checagem de lacunas:**
   `"Existe algum aspecto importante de [TEMA] que NÃO é coberto pelas fontes atuais? O que eu precisaria buscar em outra fonte?"`

5. **Simulado de entrevista:**
   `"Me faça 5 perguntas de entrevista técnica sobre governança de dados e segurança da informação, no nível de um especialista com 8+ anos de experiência, baseadas no conteúdo das fontes."`

---

## ✅ Checklist antes de entregar

- [ ] Repositório criado no GitHub com nome descritivo (ex: `miniguia-governanca-dados-cyber`)
- [ ] Este README preenchido com as respostas reais do NotebookLM (campos `[cole aqui...]`)
- [ ] Fontes conferidas e acessíveis pelos links
- [ ] Resumos revisados e enriquecidos com os insights do seu caderno
- [ ] Link do repositório colado na entrega do desafio na DIO
