# HR AI Agent

A conversational HR management system built with LangChain and Mistral AI that demonstrates the power of AI agents over traditional automation.

## 🌟 Features

### Core Capabilities
- **Natural Language Processing** - Talk to your HR system like a human colleague
- **Contextual Intelligence** - Understands complex, multi-intent requests
- **Document Retrieval (RAG)** - Answers policy questions from your HR documents
- **Conversational Memory** - Maintains context throughout the conversation

### HR Tools Available
1. **Employee Lookup** - Find employees with natural queries ("Who's the Python developer in Team A?")
2. **Leave Management** - Process vacation requests with intelligent validation
3. **Email Automation** - Send personalized onboarding emails with role-specific content
4. **IT Equipment Requests** - Handle hardware/software requests with smart recommendations
5. **Performance Reviews** - Schedule and manage reviews with contextual templates
6. **HR Policy Q&A** - Answer complex policy questions using RAG from documents
7. **Welcome Email System** - Automated onboarding email workflows
8. **General Communication** - Other HR communications and notifications

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Mistral API key
- Jupyter Notebook

### Installation
```bash
git clone https://github.com/yourusername/hr-ai-agent-demo.git
cd hr-ai-agent-demo
pip install -r requirements.txt
```

### Setup
1. Create a `.env` file in the root directory:
```env
MISTRAL_API_KEY=your_mistral_api_key_here
```

2. (Optional) Add your HR documents to the `hr_docs/` or `docs/` folders for enhanced RAG capabilities

3. Open the Jupyter notebook:
```bash
jupyter notebook hr_management_agent_demo.ipynb
```

4. Run all cells to initialize the agent

## 💬 Example Conversations

### Natural Language Employee Lookup
```
User: "Who is the senior React developer working on the mobile project?"
Agent: "I found Sarah Johnson, Senior Frontend Developer in the Engineering team. 
        She's currently working on the Mobile App Redesign project..."
```

### Intelligent Leave Processing
```
User: "I need time off for the holidays, maybe Dec 20th through Jan 2nd"
Agent: "I've processed your vacation request for Dec 20, 2024 - Jan 2, 2025 (10 business days). 
        Your remaining balance will be 8 days. Note: This overlaps with company closure Dec 25-26..."
```

### Multi-Intent Handling
```
User: "I'm starting Monday, need a laptop for ML work, and want to know about remote work policy"
Agent: "Welcome! I've noted you need ML equipment - I recommend the MacBook Pro M3 Max with 64GB RAM. 
        For remote work, our policy allows up to 3 days per week. Let me send you the welcome email 
        and IT setup instructions..."
```

## 🏗️ Architecture

### Tech Stack
- **LangChain** - Agent framework and tool orchestration
- **Mistral AI** - Large language model for natural language understanding
- **FAISS** - Vector database for document retrieval
- **HuggingFace Embeddings** - Text embeddings for semantic search

### Why AI Agent vs. Traditional Automation?

| Traditional HR Portal | AI Agent |
|----------------------|----------|
| Fill out 10-field equipment form | "I need a powerful machine for ML work" |
| Navigate 5 different systems | One conversational interface |
| Rigid dropdown selections | Natural language understanding |
| No context between requests | Maintains conversation memory |
| Generic responses | Personalized, role-aware assistance |

## 📁 Project Structure
```
hr-ai-agent-demo/
├── hr_management_agent_demo.ipynb    # Main notebook
├── requirements.txt                   # Python dependencies
├── .env.example                      # Environment variables template
├── hr_docs/                          # HR documents for RAG (optional)
├── docs/                             # Additional documents (optional)
└── README.md                         # This file
```

## 🔧 Customization

### Adding New Tools
The agent architecture makes it easy to add new HR capabilities:

```python
def new_hr_function(input_str: str) -> str:
    # Your custom HR logic here
    return "Response"

new_tool = Tool(
    name='NewHRTool',
    func=new_hr_function,
    description="Description for when to use this tool"
)
```

### Adding Documents
Simply place PDF, CSV, JSON, or TXT files in the `hr_docs/` or `docs/` folders. The RAG system will automatically index them for policy questions.

## 🎯 Use Cases

### For IT Companies
- Developer onboarding with role-specific setup
- Equipment requests with technical specifications
- Performance reviews tailored to engineering roles
- Policy questions about remote work, PTO, etc.

### For HR Teams
- Automate repetitive tasks with intelligence
- Provide 24/7 employee self-service
- Maintain consistency in HR communications
- Scale HR support without adding headcount

### For Demonstrations
- Show AI agent capabilities vs. traditional automation
- Illustrate natural language processing in enterprise
- Demonstrate RAG and document retrieval
- Exhibit conversational AI in business contexts

## 📈 Performance

- **Response Time**: < 2 seconds for most queries
- **Accuracy**: High accuracy on policy questions with proper documents
- **Scalability**: Handles multiple concurrent conversations
- **Memory**: Maintains context for full conversation sessions

## 🤝 Contributing

This is a demonstration project, but contributions are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [LangChain](https://python.langchain.com/) for the agent framework
- [Mistral AI](https://mistral.ai/) for the language model
- [HuggingFace](https://huggingface.co/) for embeddings and transformers
- [FAISS](https://github.com/facebookresearch/faiss) for efficient similarity search

## 📞 Support

If you have questions or need help with the demo:
- Open an issue in this repository
- Check the [LangChain documentation](https://python.langchain.com/docs/get_started/introduction.html)
- Review the [Mistral API documentation](https://docs.mistral.ai/)
