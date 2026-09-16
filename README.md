# Meet Ahalpara

**Software & AI Systems Engineer | High-Throughput APIs, Distributed RDBMS/Vector Engines, Cloud Automation & CI/CD Pipelines**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/meetahalpara/)
[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?style=flat-square&logo=github)](https://github.com/MeetAhalpara)
[![Email](https://img.shields.io/badge/Email-Contact-red?style=flat-square&logo=gmail)](mailto:Meetahalpara1@gmail.com)

---

## About Me

I am a Software and AI Systems Engineer specializing in high-throughput backend runtimes, distributed transactional systems, and deterministic AI retrieval architectures. My engineering focus centers on systems-level resilience: eliminating latency bottlenecks, mitigating state mutation race conditions, and enforcing strict data layer invariants. From architecting hybrid lexical/vector search pipelines with zero hallucinations to engineering 3-tier enterprise data warehouses processing millions of financial records, I build fault-tolerant backends designed for deterministic execution under dynamic load.

My practical experience spans concurrent async API microservices, distributed enterprise applications, and automated quality infrastructure. I design and operate across the stack—orchestrating containerized AWS cloud workflows, implementing database-level Row-Level Security and transaction isolation, and enforcing strict SLAs through end-to-end load testing and continuous deployment pipelines.

---

## Technical Core & Specializations

| Domain | Technologies, Runtimes & Frameworks |
| :--- | :--- |
| **Languages & Runtimes** | Python 3.11/3.12/3.13, Java 21 / 8, TypeScript 5.x, JavaScript (ES6+), Kotlin 2.0, SQL, T-SQL, PL/pgSQL, Bash |
| **Backend & Distributed Systems** | FastAPI, Node.js, Express.js, Java 21 Jakarta EE (EJB, JPA, JAX-RS), Payara Server, Flask, Uvicorn, Asyncio, RESTful APIs |
| **Databases & Vector Stores** | PostgreSQL, pgvector (HNSW Indexing), PostGIS, Microsoft SQL Server (SSMS, SSIS), MySQL, MongoDB (WiredTiger), SQLite, Redis |
| **Cloud & DevOps** | AWS (EC2, S3, IAM, EventBridge), Docker, Docker Compose, Linux (Ubuntu, Debian), Nginx, Git, GitHub Actions CI/CD, Jenkins |
| **Testing & Reliability** | Grafana k6, Pytest, Jest, Robot Framework, Selenium WebDriver, Postman / Newman CLI, JUnit 5, OWASP ZAP |

---

## Featured Engineering Projects

### Full-Scale Inventory & Operations Platform
A decoupled, multi-tenant inventory control and operational state management platform engineered for strict data isolation and high-concurrency mutation workloads.
* **Architecture & Storage:** Engineered an Express.js and Node.js REST API with Mongoose ODM, utilizing compound B-tree indexes (`{ ownerUserId: 1, purchased: 1 }`) and resilient multi-stage database bootstrapping with automatic failover from persistent WiredTiger disk storage to in-memory instances.
* **Ownership Enforcement:** Implemented stateless JWT Bearer token authentication with multi-tenant object-level access verification, eliminating unauthorized cross-tenant mutations.
* **Performance & Verification:** Validated under concurrent stress using Grafana k6 pipelines to guarantee SLAs ($p(95) < 200\text{ms}$, failure rate $< 1\%$ across 100 concurrent VUs) alongside Newman/Postman automated collection regression suites.
* **Tech Stack:** Node.js | Express.js | MongoDB (WiredTiger) | Jest | Grafana k6 | Postman / Newman
* **Source:** [Institutional Repository — Access Available by Request]

### NityaGeeta — High-Throughput Grounded Scriptural RAG Platform
An asynchronous scriptural intelligence engine engineered to eliminate LLM hallucinations across 1,296 pages of printed commentaries through deterministic dual-source retrieval.
* **Hybrid Retrieval Pipeline:** Architected an in-memory lexical BM25Okapi search engine (Robertson-Spärck Jones IDF with document-length normalization) coupled with Reciprocal Rank Fusion ($k=60$) across 5 weighted datasets ($W=3.0$ down to $W=1.0$) and $O(1)$ citation extraction to ground responses without hallucination.
* **Resilience & Streaming:** Implemented an asynchronous 3-state circuit breaker (`CLOSED`, `OPEN`, `HALF-OPEN`) with 30s backoff cooldowns to isolate upstream inference rate limits, serving responses via chunked Server-Sent Events (SSE) streaming tokens.
* **Validation & CI/CD:** Hardened with strict Pydantic v2 boundary models, a 34-test Pytest verification suite covering citation scrubbers and wire protocols, and an automated GitHub Actions CI/CD pipeline.
* **Tech Stack:** FastAPI | Python 3.12 | Next.js 15 | React 19 | PostgreSQL | Docker | Pytest | Groq API
* **Source:** [![Repository](https://img.shields.io/badge/View-Repository-24292e?style=flat&logo=github)](https://github.com/MeetAhalpara/NityaGeeta)

### ConsultHub — Two-Sided Marketplace & Geospatial Engine
A full-stack professional marketplace platform featuring vector-based semantic matchmaking, spatial distance filtering, and atomic contract lifecycle workflows.
* **Semantic & Spatial Discovery:** Implemented Supabase PostgreSQL RPCs combining 384-dimensional pgvector embeddings via HNSW cosine indexing (`vector_cosine_ops`) with PostGIS GiST spatial queries (`ST_DWithin`) and composite scoring algorithms ($0.7 \times \text{similarity} + 0.3 \times \text{skill\_overlap}$).
* **Relational Security & Triggers:** Enforced 100% database-level Row-Level Security (RLS) across all entities, isolated mutations within `SECURITY DEFINER` procedures, and automated messaging states via PL/pgSQL database triggers.
* **Client Architecture:** Built a unified cross-platform client with React Native (Expo SDK 54) and Next.js 16 App Router, utilizing TanStack Query caching and atomic transaction boundaries.
* **Tech Stack:** Next.js 16 | React Native (Expo) | Supabase | PostgreSQL | pgvector | PostGIS | TypeScript
* **Source:** [Private Enterprise Platform — Source Protected under NDA]

### Distributed Enterprise Systems (REST-ACMEMedical & PTFMS)
A suite of high-availability enterprise applications engineered with strict design patterns and distributed transaction processing capabilities.
* **Jakarta EE Enterprise Platform (ACMEMedical):** Architected a multi-tier clinical management platform on Java 21 and Payara Server using JAX-RS, stateless EJBs, and JPA/Hibernate with optimistic locking (`@Version`), RFC 7617 HTTP Basic authentication, and Soteria PBKDF2 credential hashing (2048 iterations, 32-byte salt, 256-bit key).
* **Transit Fleet Operations (PTFMS):** Built an enterprise transit coordination platform using Java 8 / Servlets, JDBC PreparedStatement pools, and GoF patterns (Strategy for polymorphic propulsion fuel tracking, Adapter for external GPS feeds, and Observer for maintenance dispatching).
* **Enterprise Persistence:** Engineered normalized schemas across MySQL instances with connection pooling, declarative role-based access control, and JUnit 5 / Jersey Client integration suites.
* **Tech Stack:** Java 21 / 8 | Jakarta EE | EJB | JPA / Hibernate | Payara | Servlets | JDBC | MySQL
* **Source:** [![Repository](https://img.shields.io/badge/View-Repository-24292e?style=flat&logo=github)](https://github.com/MeetAhalpara/Public-Transport-Fleet-Management-System)

### Banking Analytics Data Warehouse & Risk Default Engine
A decision-support banking data warehouse modeled on a 3-tier Kimball analytical pattern to ingest, model, and analyze transactional ledgers and forecast credit risk.
* **High-Volume ETL Architecture:** Engineered SSIS memory-buffered pipelines with upstream physical sort contracts and cascading merge joins to extract, cleanse, and transform $1.05\text{M}+$ financial records and regional socio-economic indicators.
* **Predictive Risk Analytics:** Authored multi-level Transact-SQL CTEs, rolling aggregations, and window functions to compute liquidity depletion velocity flags ($>5$ withdrawals $> \$500$), forecasting loan defaults 2–3 months prior to delinquency.
* **Dimensional Modeling:** Designed star/snowflake schemas in SQL Server with clustered indexing, categorical domain mapping, and interactive Power BI analytical dashboards.
* **Tech Stack:** Microsoft SQL Server | T-SQL | SSIS | SSMS | Power BI
* **Source:** [![Repository](https://img.shields.io/badge/View-Repository-24292e?style=flat&logo=github)](https://github.com/MeetAhalpara/Banking-Analytics-Data-Warehouse)

### SauceDemo Quality Engineering & CI/CD Test Harness
An enterprise-grade test automation and regression framework designed to evaluate single-page web applications against complex shopping and checkout flows.
* **DOM Synchronization Engine:** Engineered a Page Object Model (POM) test architecture in Python and Selenium WebDriver, injecting custom JavaScript into React’s internal `_valueTracker` to dispatch synthetic bubbling `input` and `change` events and eliminate headless synchronization race conditions.
* **Dual Automation Engine:** Implemented 22 parameterized Pytest scenarios and 14 keyword-driven Robot Framework specifications with zero implicit waits and explicit condition polling.
* **Continuous Integration Pipelines:** Configured dual execution pipelines across Jenkins (declarative Jenkinsfile archiving JUnit XML trends) and GitHub Actions with automated failure screenshot capture and interactive HTML test reporting.
* **Tech Stack:** Python | Selenium WebDriver | Robot Framework | Pytest | Jenkins | GitHub Actions
* **Source:** [![Repository](https://img.shields.io/badge/View-Repository-24292e?style=flat&logo=github)](https://github.com/MeetAhalpara/QA-Test-Automation)

---

## Education & Credentials

### Academic Foundations
* **Algonquin College** (Ottawa, ON)
  * Advanced Diploma in Computer Programming and Analysis
  * Cumulative GPA: 3.52 / 4.00 | Multi-Term Dean's Honours List
* **Sir Bhavsinhji Polytechnic Institute** (Gujarat, India)
  * Diploma in Information Technology
  * Cumulative GPA: 7.91 / 10.0 CGPA

### Professional Certifications
* AWS Certified Cloud Practitioner (CLF-C02) — In Progress
* AWS Educate – Introduction to Cloud 101
* Microsoft – Describe Cloud Computing Principles
* LinkedIn Learning Certificate – Software Architecture Patterns
