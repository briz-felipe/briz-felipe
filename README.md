## 👋 Olá! Eu sou o Felipe Briz

**Software Engineer** no time de **Martech**, onde engenharia de software e engenharia de dados se encontram. Construo **data products** e os **serviços que nascem deles** — plataformas internas idealizadas junto aos times de Produto e Marketing, com todo o desenho técnico, a arquitetura e o planejamento de desenvolvimento feitos dentro do time. Sistemas que lidam com bases analíticas na casa de **dezenas de milhões de registros** e comunicação em larga escala.

---

<div align="center">
  <img src="https://github-readme-stats-red-five-42.vercel.app/api?username=briz-felipe&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=true&theme=dracula&locale=pt-BR&hide_border=false" height="160" />

  <img src="https://github-readme-stats-red-five-42.vercel.app/api/top-langs?username=briz-felipe&locale=pt-BR&hide_title=false&layout=compact&card_width=320&langs_count=10&theme=dracula&hide_border=false" height="160" />
</div>

---

## 💼 O que eu construo

- **Data products**: plataformas internas sobre bases analíticas — CDP, catálogo de rotas e visões agregadas para times de CX, Comercial e Financeiro
- **Serviços ligados aos data products**: APIs em **Go** e **Python/FastAPI**, workers de processamento em massa, SPAs em React para os times operarem em cima do dado
- **Arquitetura orientada a eventos**: integrações entre serviços via plataforma de eventos, com contrato versionado, idempotência de ponta a ponta e reconciliação assíncrona
- **Pipelines de dados** no **Airflow**: cargas incrementais lakehouse → Postgres, watermarks, schema evolution e índices como responsabilidade da carga

---

## 🧭 Como eu desenho sistemas

Convicções que aplico em todo projeto:

- **Evento é contrato, não notificação.** Envelope canônico, versionamento, `idempotency_key` de ponta a ponta e DLQ com replay. Consumidor idempotente por escrita condicional: reentrega vira no-op, nunca dado duplicado.
- **Fila como fronteira entre sistemas.** SQS com visibility timeout, backoff por receive count e lease com fencing token para trabalho distribuído. Em integração cross-account, IAM dos **dois** lados — produtor e consumidor — validado no dia 1.
- **Cache-aside com propósito.** Redis/Valkey separando **estado** (noeviction, persistência) de **cache** (TTL derivado da cadência do dado, não de um número mágico). Warm-up fora do caminho crítico.
- **Agregação na ingestão, não na leitura.** Contadores e rollups mantidos no momento da escrita para leitura O(1) — dashboards não fazem GROUP BY em milhões de linhas.
- **Grandes volumes como premissa.** Todo caminho síncrono protegido (cache, debounce, teto); escrita em massa vai por fila com atomicidade.
- **Simplicidade é decisão de arquitetura.** DDD pragmático, packages como bounded contexts, zero camada especulativa.

---

## 🏗️ Infraestrutura como padrão

Todo projeto nasce padronizado — infra não é etapa posterior:

- **Terraform em 100% dos projetos**: plan gerado e revisado no PR, apply só no merge, nunca aplicação manual
- **GitOps** (Flux) para deploy em Kubernetes: o repositório é o estado do cluster
- **AWS** como plataforma: SQS, DynamoDB, S3, Lambda, RDS, Secrets Manager, IAM com least privilege, EKS Pod Identity
- **Observabilidade primeiro**: logs estruturados, métricas por evento de negócio (enviado vs entregue), alarmes sobre DLQs — silêncio nunca é sucesso

---

## 📊 Um pé em engenharia de dados

- Orquestração com **Apache Airflow**: DAGs incrementais, idempotentes e com recuperação por checkpoint
- Movimentação lakehouse (**Iceberg**) → bancos operacionais, com atenção a schema evolution e custo de full refresh
- Modelagem SQL para consumo operacional: SCD2, chaves surrogate, hidratação on-read de dados sensíveis
- Integrações de analytics: **Amplitude**, GA4, padrões de UTM como contrato entre disparo e conversão

---

## 🤖 Desenvolvimento assistido por IA

- Fluxos com **Claude Code** e **MCP servers** no dia a dia de engenharia
- **CLAUDE.md** e memória persistente como contexto de longo prazo por projeto
- IA amplifica quem tem fundamento: contrato claro, testes e revisão continuam sendo o alicerce

---

## 🧠 Stack técnica

<div align="left">
  <img src="https://skillicons.dev/icons?i=go" height="40" alt="go" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=py" height="40" alt="python" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=fastapi" height="40" alt="fastapi" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=postgres" height="40" alt="postgresql" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=redis" height="40" alt="redis-valkey" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=dynamodb" height="40" alt="dynamodb" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=aws" height="40" alt="aws" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=terraform" height="40" alt="terraform" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=kubernetes" height="40" alt="kubernetes" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=docker" height="40" alt="docker" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=react" height="40" alt="react" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=ts" height="40" alt="typescript" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=git" height="40" alt="git" />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=linux" height="40" alt="linux" />
</div>

**Também no cinto:** Apache Airflow · SQS · Valkey · Flux/GitOps · Datadog & Grafana · Iceberg/DuckDB · Django

---

## 📫 Vamos conversar

<div align="left">
  <a href="https://www.linkedin.com/in/felipebriz/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="40" />
  </a>
  <a href="https://discordapp.com/users/855468172387942430" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="40" />
  </a>
  <a href="mailto:briz.felipe@gmail.com" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="40" />
  </a>
  <a href="https://wa.me/5511978187157" target="_blank">
    <img src="https://img.shields.io/static/v1?message=WhatsApp&logo=whatsapp&label=&color=25D366&logoColor=white&labelColor=&style=for-the-badge" height="40" />
  </a>
</div>
