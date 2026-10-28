# AwanSolveAi | HR Policy & SOP Knowledge Intelligence

### Helping businesses turn complex HR documents into accessible, reliable knowledge

**A practical AI-powered knowledge assistant for HR teams, employees, managers, and business operations.**

Developed by **AwanSolveAi — Intelligent Business Software Solutions**.

---

## The Business Problem

Many organizations maintain extensive HR policies, employee handbooks, standard operating procedures (SOPs), and administrative guidelines.

Finding the right information can be time-consuming, particularly when documents cover multiple departments, policies, or jurisdictions.

Employees may repeatedly ask similar questions, while HR teams must locate and verify the relevant policy language.

## Our Solution

The **AwanSolveAi HR Knowledge Intelligence Platform** helps users search approved policy documents through natural-language questions.

Rather than manually searching numerous documents, users can ask questions and retrieve relevant policy information with supporting source references.

### Key Capabilities

- **Intelligent Policy Search:** Find relevant information from HR policies, handbooks, and SOPs.
- **Evidence-Based Responses:** Associate answers with supporting policy references.
- **Source Traceability:** Help users verify information against original documents.
- **Hybrid Document Retrieval:** Combine semantic search and keyword-based matching.
- **Document Context Awareness:** Preserve relevant policy and jurisdiction information.
- **Unsupported-Answer Protection:** Withhold unsupported answers when sufficient evidence is unavailable.
- **Customizable Knowledge Base:** Adapt the architecture to an organization's approved documents.

## Business Benefits

The platform is designed to help organizations:

- Reduce time spent searching internal documents.
- Improve access to consistent policy information.
- Support faster responses to routine HR questions.
- Reduce repetitive document-search tasks.
- Make better use of existing organizational knowledge.
- Support employees and managers with traceable information.

Actual time savings depend on the organization's documents, workflows, and deployment.

## Who Can Benefit?

Potential users include:

- Small and medium-sized businesses
- Human Resources departments
- Business operations teams
- Employee support departments
- Administrative service providers
- HR consultants
- Organizations managing extensive policies and SOPs

## Example Questions

Users could ask:

- What is the employee offboarding procedure?
- Where can I find the leave-of-absence policy?
- Which document explains anti-harassment reporting?
- What does the policy say about remote working?
- What information is available about employee benefits?

Answers depend entirely on the approved documents available in the knowledge base.

## Technology

This implementation uses:

| Component | Technology |
|---|---|
| Primary language | Python |
| Document intelligence | Retrieval-Augmented Generation (RAG) architecture |
| Semantic retrieval | Sentence Transformers |
| Vector search | FAISS |
| Keyword retrieval | BM25 |
| Hybrid ranking | Reciprocal Rank Fusion |
| Optional reranking | MiniLM CrossEncoder |
| User interface | Streamlit |
| Evaluation | Automated Python tests and retrieval benchmarks |

The architecture can operate with local components. Answer generation requires a separately configured compatible backend.

## Internal Validation

The project's frozen V1 evaluation report records:

| Evaluation | Recorded result |
|---|---|
| Golden evaluation set | 75 cases |
| Golden Top-1 retrieval accuracy | 98.48% |
| Golden Recall@3 | 100% |
| Adversarial evaluation set | 41 cases |
| Adversarial Top-1 retrieval accuracy | 97.14% |
| Regression tests | 28/28 passed |

**Important:** These figures are internal evaluation results for the tested corpus and configurations. They do not guarantee the same performance on new organizations, documents, or production workloads.

See [FREEZE_V1.md](FREEZE_V1.md) and [AUDIT.md](AUDIT.md) for the evaluation record, technical findings, and limitations.

## Running the Project Locally

Install dependencies:

```powershell
python -m pip install -r requirements.txt
```

Example policy retrieval:

```powershell
python main.py "What happens when an employee leaves GitLab?"
```

Run the retrieval evaluation:

```powershell
python -m evaluation.evaluate --no-reranker
```

Run automated tests:

```powershell
python -m pytest -q
```

### Streamlit Interface

Configure a compatible answer-generation backend, then launch the application.

Example using the existing Ollama backend:

```powershell
$env:POLICY_GENERATOR_BACKEND="src.generation.ollama_backend:generate"
python -m streamlit run app/streamlit_app.py
```

The selected backend must be installed, configured, and operational.

Without a configured generation backend, the application intentionally restricts answer generation.

## Demonstration and Deployment Scope

This repository is a reference implementation and portfolio demonstration.

It is not an independently certified HR compliance system or a verified production deployment for a customer.

For a business implementation, the platform must be configured and evaluated using that organization's authorized documents, access requirements, privacy rules, and relevant jurisdictions.

**Human review remains necessary for consequential employment and compliance decisions.**

## Source Attribution

The demonstration corpus includes material derived from publicly available GitLab handbook content.

GitLab's public handbook is licensed under **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.

Official source: https://handbook.gitlab.com/

Handbook licensing information: https://handbook.gitlab.com/handbook/about/handbook-usage/

GitLab retains its applicable rights to its original content. Any reused or adapted material remains subject to the corresponding license requirements, including attribution and applicable share-alike conditions.

AwanSolveAi is an independent software-development initiative and is not affiliated with or endorsed by GitLab.

The licensing of third-party handbook content is separate from the licensing of AwanSolveAi's original application code.

## Custom Business Solutions

AwanSolveAi develops customized AI-powered knowledge and document-intelligence applications for organizations seeking practical, cost-conscious software solutions.

Potential implementations include:

- HR Policy Intelligence
- Internal SOP Knowledge Assistants
- Employee Handbook Search Systems
- Document Retrieval and Comparison
- Administrative Knowledge Systems
- Evidence-Based Business Document Assistants

## Contact

**Malik Usman Haider**  
Founder & AI Solutions Developer  
**AwanSolveAi**

Email: awansolveai2025@gmail.com

GitHub: https://github.com/AwanSolveAi

https://www.linkedin.com/in/malik-usman-438424446/

**AwanSolveAi — Turning Business Knowledge into Practical AI Solutions.**
