 
## System Architecture __ Overview
Scribe is built as a multi layer architecture that connects communication tools (like Slack or Notion) to an AI processing backend.  
It extracts key decisions, summaries, and insights from conversations, storing them as structured knowledge that can be queried later.


## Frontend Stack
Framework: React (Next.js)  
Styling: TailwindCSS + ShadCN components  
Key Modules:
- Conversation Feed: Displays real-time captured discussions.
- Knowledge Dashboard: Shows summarized insights and linked threads.
- AI Coworker Panel: Interface for interacting with the AI assistant.
- Analytics View: Provides engagement and recall metrics.


### Communication
Frontend communicates with backend REST APIs and WebSocket channels for real time updates.


#### Backend Stack

Framework: (Node.js + Express)
 Core Services:
1. AI Processing Service
   - Handles summarization, context filtering, and memory embeddings.
   - Uses OpenAI / Anthropic APIs for natural language understanding.
2. Data Pipeline Service
   - Ingests messages from external integrations (Slack, Notion, email).
   - Filters noise, extracts entities, and routes clean data to storage.
3.  API Gateway
   - Authenticates requests and routes data between frontend and backend.
   - Implements rate limiting and caching for performance.


##### Data Base Stack
| Layer           |   Technology           |                 Purpose |
|-----------------|------------------------|--------------------------------------|

| Primary DB     |    PostgreSQL           | Stores summaries, metadata, and user profiles. |

| Cache Layer    |      Redis              |      Speeds up query and retrieval operations. |

| Vector DB     |      Pinecone / Weaviate | Enables semantic memory and contextual recall. |



######  Technical Feasibility
Scribe’s architecture leverages proven, scalable technologies — React, Node.js, and PostgreSQL — ensuring:
- Fast MVP Development
- AI Integration Ready
- Scalable Knowledge Indexing
- Cloud Deployment Support (AWS/Vercel)

This makes the system both feasible and sustainable for production-scale teams.




Design Mockup
https://www.figma.com/design/ZDt9yf76NGkc5oLSEGIg99/AI-Web-driven-Architecture?node-id=0-1&t=uGKqq52yqFZCs7hZ-1