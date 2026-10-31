# Assignment 2: Safe and Production-Aware Student Support Agent

## Project Overview
This project extends the Intelligent Student Support Agent with authentication checks, authorization, support request confirmation, sensitive information redaction, and audit logging.

## Objectives
- Verify the identity of the authenticated student.
- Allow students to access their own records.
- Block unauthorized access to another student's private data.
- Request confirmation before submitting support requests.
- Redact recognized sensitive information before storing messages.
- Record important actions and outcomes in audit logs.
- Evaluate normal functionality, privacy, and safety behaviour.

## Technologies
- Python
- Streamlit
- SQLite
- Regular expressions

## Project Components
- `app.py`: Chat interface
- `agent.py`: Agent logic and confirmation workflow
- `auth_context.py`: Authentication context
- `tools.py`: Student tools and access checks
- `database.py`: Database operations and audit logging
- `memory.py`: Conversation storage and sensitive information redaction
- `retrieval.py`: Policy retrieval
- `data/students.csv`: Sample student data
- `data/student_policy.txt`: Student policy document

## How to Run
Install the dependencies:

```bash
pip install -r requirements.txt
```

Start the application:

```bash
streamlit run app.py
```

## Privacy and Safety Tests
Evaluate:
1. Access to the authenticated student's own record.
2. Attempted access to another student's record.
3. Confirmation before support request submission.
4. Cancellation when confirmation is rejected.
5. Redaction of recognized sensitive information.
6. Audit logging of important operations.

## Evaluation
Record actual test results, latency, tool usage, token usage when available, and relevant audit evidence in `evaluation.md`.

## Limitations
This is an educational prototype. Sensitive information redaction only covers recognized patterns. Additional security testing is required before production deployment.

## Conclusion
The application extends the original student support agent with authentication, authorization checks, support request confirmation, sensitive information redaction, and audit logging.