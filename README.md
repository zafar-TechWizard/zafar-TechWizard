<div align="center">
  <img src="assets/dot-matrix-header.svg" width="100%" alt="Header Banner" />
  
  <br/>

  [![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=3000&pause=1000&color=9745F5&center=true&vCenter=true&multiline=true&repeat=true&random=false&width=700&height=100&lines=Product+Engineer+%7C+AI+Systems+Builder;SaaS+%7C+Microservices+%7C+Automation;Architecting+Systems+from+Zero+to+Production)](https://git.io/typing-svg)

  <br/>

  [![Portfolio](https://img.shields.io/badge/Portfolio-zafar--dev-7B2FF7?style=for-the-badge&logo=google-chrome&logoColor=white&labelColor=0D1117)](https://zafar-dev-portfolio.vercel.app/)
  &nbsp;
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Md_Zafar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117)](https://www.linkedin.com/in/md-zafar-41687b157)
  &nbsp;
  [![Email](https://img.shields.io/badge/Email-mdzafarddd-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117)](mailto:mdzafarddd@gmail.com)

  <br/><br/>
  
  ![Profile Views](https://komarev.com/ghpvc/?username=zafar-TechWizard&color=7B2FF7&style=flat-square&label=Profile+Views)
  &nbsp;
  ![Followers](https://img.shields.io/github/followers/zafar-TechWizard?label=Followers&style=flat-square&color=7B2FF7&labelColor=0D1117)

</div>

---

## 👨‍💻 Engineering Philosophy

I build software systems that solve real problems. My focus bridges the gap between **robust system design**, **highly-efficient web automation**, and **applied artificial intelligence**. I don't just build chatbots or basic CRUD interfaces—I design multi-tenant SaaS structures with fine-grained access isolation, architect microservice pipelines to scrape and orchestrate complex datasets, and build custom cognitive memory infrastructures for agentic AI applications.

---

## 🛠️ Tech Stack Matrix

| Domain | Technologies |
| :--- | :--- |
| **Languages** | `Python` &middot; `TypeScript` &middot; `JavaScript` &middot; `HTML/CSS` &middot; `C` |
| **Backend & Web APIs** | `FastAPI` &middot; `Flask` &middot; `Node.js` &middot; `REST APIs` &middot; `Microservices` |
| **Frontend & Mobile** | `Next.js` &middot; `React` &middot; `React Native` &middot; `Tailwind CSS` |
| **AI/ML & Cognitive Systems** | `LangChain` &middot; `RAG Pipelines` &middot; `Neo4j` &middot; `spaCy` &middot; `GLiNER` &middot; `OpenCV` &middot; `scikit-learn` &middot; `Hugging Face` |
| **Databases & Infrastructure** | `PostgreSQL` &middot; `MongoDB` &middot; `SQLite` &middot; `Docker` &middot; `Linux` &middot; `Git/GitHub` |

---

## 🏗️ Architectural Showcases

These architectural showcases outline the systems design and technical approaches behind my core builds.

### 🧠 Showcase A: Three-Tier Cognitive AI Memory (`assistant-memory`)
An open-source, modular Python library that gives AI agents a cognitive memory system inspired by the human brain—moving beyond simple vector retrieval to intent-aware graph traversal.

```mermaid
graph TD
    %% Query Flow
    UserQuery[User Input / Query] --> IntentRouter{Intent Router}
    IntentRouter -->|Fact / Concept| FactPath[Knowledge Nodes]
    IntentRouter -->|Emotion / Tone| EmotionPath[Emotion Nodes]
    IntentRouter -->|Time / Context| TemporalPath[Episodic Nodes]
    
    FactPath --> SpreadingActivation[Spreading Activation Traversal]
    EmotionPath --> SpreadingActivation
    TemporalPath --> SpreadingActivation
    
    SpreadingActivation --> ContextSynthesis[4-Pillar Working Context]
    ContextSynthesis --> SystemPrompt[LLM System Prompt]

    %% Database & Background Consolidator
    ConsolidationAgent[Memory Consolidation Agent] -. Runs Async .-> Neo4j[(Local Neo4j Graph DB)]
    Neo4j <--> SpreadingActivation
    ConsolidationAgent -. CREATE / UPDATE / CONTRADICT .-> Neo4j

    style UserQuery fill:#7B2FF7,stroke:#fff,stroke-width:2px,color:#fff
    style ContextSynthesis fill:#9745F5,stroke:#fff,stroke-width:2px,color:#fff
    style Neo4j fill:#1F2937,stroke:#7B2FF7,stroke-width:2px,color:#fff
    style ConsolidationAgent fill:#1F2937,stroke:#9745F5,stroke-width:2px,color:#fff
```

*   **Semantic Graph Traversals**: Implemented spreading-activation retrieval using Neo4j to find linked memories based on conversational context, preventing topic-drift.
*   **Intent-Aware Routing**: Boosts different memory edges dynamically based on whether the query is factual (knowledge-path), temporal (chronological-path), or emotional.
*   **Agentic Consolidation**: An asynchronous reasoning loop that parses past interactions, updates graph entities, and explicitly handles conflicting beliefs over time without destroying historic lineage.
*   **Zero Vendor Lock-In**: Operates locally using dockerized Neo4j, sentence embeddings, and local cross-encoder rerankers, requiring zero external SaaS bills.

---

### 🏢 Showcase B: Multi-Tenant SaaS & Data Pipelines (`CoWork-Pro`)
A coworking space management platform built to scale, showcasing multi-tenant Postgres schema isolation, role/location access rules, and automated browser automation microservices.

```mermaid
graph LR
    %% Tenancy Model
    Client[Next.js Client] --> Gateway[FastAPI Backend Gateway]
    Gateway --> Auth{RBAC & LBAC Guard}
    Auth --> Tenant1[(Tenant A Schema)]
    Auth --> Tenant2[(Tenant B Schema)]
    
    %% Automation pipelines
    ScraperCron[Scheduler] --> PlaywrightCluster[Playwright Workers]
    PlaywrightCluster -->|Extract & Transform| Queue[RabbitMQ / Process Queue]
    Queue --> Gateway

    style Client fill:#7B2FF7,stroke:#fff,stroke-width:2px,color:#fff
    style Auth fill:#9745F5,stroke:#fff,stroke-width:2px,color:#fff
    style Tenant1 fill:#1F2937,stroke:#7B2FF7,stroke-width:1px,color:#fff
    style Tenant2 fill:#1F2937,stroke:#7B2FF7,stroke-width:1px,color:#fff
```

*   **Granular Tenancy Security**: Architected robust schema-level data separation with Role-Based Access Control (RBAC) and Location-Based Access Control (LBAC) to handle secure corporate bookings and billing.
*   **Browser Automation Microservices**: Designed self-healing automated pipelines using Playwright to extract, sanitize, and update external resource availabilities into database records.
*   **Scalable Stack**: Combines a fast-loading React/Next.js frontend with an asynchronous FastAPI gateway executing optimized PostgreSQL transactions.

---

### 🔍 Showcase C: Search RAG & Real-Time Computer Vision (`InfoLytix` & `Surveillance`)
Applied AI implementations focused on real-time data retrieval and processing, bridging the gap between web databases and computer vision models.

```mermaid
graph TD
    UserQuery[Search Query] --> QueryExpansion[Query Optimizer]
    QueryExpansion --> SearchAPIs[Web Search APIs]
    SearchAPIs --> WebRetrieval[HTML Scrapers]
    WebRetrieval --> CrossEncoder[Cross-Encoder Reranker]
    CrossEncoder --> ContextChunking[Document Chunking & Vector Store]
    ContextChunking --> LLMGen[Context-Augmented LLM Generation]
    LLMGen --> VerifiedAnswer[Cited Natural Language Answer]

    style UserQuery fill:#7B2FF7,stroke:#fff,stroke-width:2px,color:#fff
    style VerifiedAnswer fill:#9745F5,stroke:#fff,stroke-width:2px,color:#fff
```

*   **Multi-Step RAG Pipeline (`InfoLytix`)**: A Perplexity-like research assistant that rewrites searches, crawls target web documents in real-time, reranks snippets, and generates cited, grounded answers.
*   **Real-Time CV Surveillance**: Built a computer vision threat detection prototype during the Startup Thrive Hackathon (Top 4 Finish) that processes video streams concurrently and dispatches automated SMTP alert notifications.

---

## 📂 Under-The-Hood Projects

Here are some other systems, prototypes, and experiments I've built during my development journey:

<details>
<summary><b>📱 SOFI-App & AI Agent Ecosystem</b></summary>

*   **SOFI**: My personal agentic assistant utilizing sub-agent structures, memory tools, and the `assistant-memory` engine to run background processes.
*   **SOFI-App**: A React Native (TypeScript) mobile application that acts as a secure, real-time control interface for interacting with my personal assistant.
</details>

<details>
<summary><b>📅 StudySync (Android Excel Schedule Parser)</b></summary>

*   An utility application built to solve schedule drift. It downloads university Excel timetables, filters them dynamically based on user sections and batch details, and sets local alarm managers to notify about classes, venues, and teachers 15 minutes before they begin.
</details>

<details>
<summary><b>🧘 ZenPulse (Flask Wellness Companion)</b></summary>

*   A mental well-being dashboard built using Flask, containing a session-isolated LLM chatbot for emotional support and a virtual chatbot pet that responds dynamically to user text input.
</details>

<details>
<summary><b>📊 Applied Machine Learning & Data Science</b></summary>

*   **Animal Species Classification**: CV model employing deep transfer learning to categorize animal classes.
*   **Age & Gender Detection**: Computer vision model wrapped in a Streamlit GUI to perform live/image-based face classification.
*   **Car Price Prediction**: Regression analysis model evaluating pre-owned vehicle valuations.
*   **Email Spam Classifier**: NLP text classification model identifying and filtering spam emails.
*   **Movie Recommendation System**: Similarity-search-based recommendation engine utilizing collaborative vector filtering.
</details>

---

## 📊 Developer Metrics

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=zafar-TechWizard&show_icons=true&theme=midnight-purple&hide_border=true&bg_color=0D1117&title_color=9745F5&icon_color=9745F5&text_color=c9d1d9&ring_color=9745F5" alt="GitHub Stats" />
  &nbsp;&nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=zafar-TechWizard&layout=compact&theme=midnight-purple&hide_border=true&bg_color=0D1117&title_color=9745F5&text_color=c9d1d9&langs_count=8" alt="Top Languages" />
  
  <br/>
  
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=zafar-TechWizard&theme=midnight-purple&hide_border=true&background=0D1117&stroke=9745F5&ring=9745F5&fire=9745F5&currStreakLabel=9745F5&sideLabels=c9d1d9&currStreakNum=c9d1d9&sideNums=c9d1d9&dates=6e7681" alt="GitHub Streak" />

  <br/>
  
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=zafar-TechWizard&bg_color=0D1117&color=9745F5&line=9745F5&point=FFFFFF&area=true&area_color=9745F5&hide_border=true" alt="Contribution Graph" />
</div>

---

## 🚀 Currently & Connecting

```yaml
learning:
  - Advanced distributed system design & concurrency
  - Custom LLM fine-tuning & domain-specific embeddings
  - Cloud-native architecture (AWS certification track)
building:
  - Local-first knowledge systems and custom agent integrations
  - Production SaaS models with isolation-first constraints
open_to:
  - Contract & freelance system builds (FastAPI backend architectures, RAG, Web Automation)
  - Collaborative engineering in agentic and developer tooling projects
```

<div align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=midnight-purple" alt="Dev Quote" />
  
  <br/>
  
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer" width="100%" alt="Footer Wave" />
</div>
