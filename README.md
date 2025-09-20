# Expert Role Prompt MCP v2.0 🎯

Enhanced Model Context Protocol server with 50 expert roles, advanced reasoning frameworks, and REST API.

## ✨ What's New in v2.0

### 🎭 50 Expert Roles (Expanded from 7)
- Engineering: Backend, Frontend, DevOps, Security, Mobile, Data, QA
- Product & Design: Product Manager, UX Designer, UI Designer
- Business: Business Analyst, Project Manager, Marketing Manager
- AI/ML: ML Engineer, Data Scientist, AI Researcher, Prompt Engineer
- And many more specialized roles!

### 🧠 Advanced Reasoning Frameworks
- **Chain-of-Thought (CoT)**: Step-by-step problem solving
- **Tree-of-Thoughts (ToT)**: Branching exploration of solutions
- **Custom Workflows**: Create your own reasoning patterns

### 📊 Enhanced Confidence Scoring
- Keyword matching with weights
- Domain-specific confidence calculations
- Multi-factor scoring algorithm

### 🔌 REST API Server
- Port 3456 for external integrations
- JSON-based request/response
- WebSocket support (coming in v2.1)

## 🚀 Installation

### As Part of MCP Federation Core
See [MCP Federation Core](https://github.com/justmy2satoshis/mcp-federation-core) for complete installation.

### Standalone Installation

1. Clone the repository:
```bash
git clone https://github.com/justmy2satoshis/expert-role-prompt.git
cd expert-role-prompt
```

2. Install dependencies:
```bash
npm install
```

3. Add to Claude Desktop config:
```json
{
  "mcpServers": {
    "expert-role-prompt": {
      "command": "node",
      "args": ["C:/path/to/expert-role-prompt/server.js"],
      "type": "stdio"
    }
  }
}
```

4. Restart Claude Desktop

## 📖 Usage

### Nominate an Expert
```javascript
expert-role-prompt:nominate_expert
  task_description: "Design a scalable microservices architecture"
  
// Returns best expert match with confidence score
```

### Enhance a Prompt
```javascript
expert-role-prompt:enhance_prompt
  expert_id: "backend_engineer"
  task_description: "Implement user authentication"
  reasoning_type: "technical"
```

### Execute Workflow
```javascript
expert-role-prompt:execute_workflow
  template_name: "api_design"
  context: { "requirements": "RESTful API for e-commerce" }
```

### Apply Reasoning
```javascript
expert-role-prompt:apply_reasoning
  framework: "chainOfThought"
  template: "problem_solving"
  variables: { "problem": "Database performance issues" }
```

## 🎭 Available Expert Roles

### Engineering (15 roles)
- `backend_engineer`: Server-side architecture, APIs, databases
- `frontend_engineer`: UI/UX implementation, React/Vue/Angular
- `devops_engineer`: CI/CD, containerization, cloud infrastructure
- `security_engineer`: Security audits, penetration testing
- `mobile_engineer`: iOS/Android development
- And 10 more...

### Product & Design (8 roles)
- `product_manager`: Product strategy, roadmaps
- `ux_designer`: User experience, wireframes
- `ui_designer`: Visual design, design systems
- And 5 more...

### Business (10 roles)
- `business_analyst`: Requirements, process optimization
- `project_manager`: Agile/Scrum, timeline management
- `marketing_manager`: Go-to-market, campaigns
- And 7 more...

### AI/ML (7 roles)
- `ml_engineer`: Model deployment, MLOps
- `data_scientist`: Statistical analysis, experiments
- `prompt_engineer`: Prompt optimization, LLM fine-tuning
- And 4 more...

### Other Specialists (10 roles)
- `technical_writer`: Documentation, tutorials
- `qa_engineer`: Testing strategies, automation
- `solutions_architect`: System design, integration
- And 7 more...

## 🔧 REST API

Start the REST API server:
```bash
node rest-api-server.js
```

### Endpoints

#### POST /nominate
```json
{
  "task_description": "Build a recommendation system",
  "context": "E-commerce platform with 1M users"
}
```

#### POST /enhance
```json
{
  "expert_id": "ml_engineer",
  "task_description": "Implement collaborative filtering",
  "reasoning_type": "technical"
}
```

#### GET /experts
Returns list of all available experts

#### GET /expert/:id
Get details for specific expert

## 🧪 Testing

Run the test suite:
```bash
npm test
```

Test confidence scoring:
```bash
node test-confidence.js
```

## 📊 Performance

- Response time: <100ms for expert nomination
- Confidence scoring: <50ms
- REST API: Handles 1000+ requests/second
- Memory usage: ~50MB idle, ~100MB active

## 🤝 Contributing

We welcome contributions! Areas of focus:
- Adding more expert roles
- Improving confidence algorithms
- New reasoning frameworks
- Performance optimizations

## 📄 License

MIT License

## 🔗 Links

- [MCP Federation Core](https://github.com/justmy2satoshis/mcp-federation-core)
- [Documentation](https://github.com/justmy2satoshis/expert-role-prompt/wiki)
- [Issues](https://github.com/justmy2satoshis/expert-role-prompt/issues)

---

Part of the MCP Federation ecosystem.