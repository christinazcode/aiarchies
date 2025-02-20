# Functional Requirements

The **Augmenting Human Intelligence solution** makes it more efficient for both full-time and part-time expert software architects to collaborate.

The agent, named **Ema**, enables authorized users to have certifiable, context-aware conversations to assist with their tasks.

The five designated experts can use the solution to **brainstorm** ideas to modify certification tests and change/add case studies. They can continue the conversation with Ema to further fine-tune those ideas.

Ungraded aptitude tests and architecture submissions will be scanned automatically to check for **plagiarism**, including internet searches, previous aptitude tests and submissions, and AI-generated content.

The solution will **summarize** any test answers longer than 50 words and generate feedback so the expert software architects can spend two hours or less grading each candidate.

The solution will provide **references** to previous submissions and feedback for the same or similar questions to help maintain consistency and fairness in the grading process.

Users can **rank** LLM responses to improve the LLM's response generation, including Ema's.

# Added By som
Software Architecture shall have a data pipeline to have continous update of  test questions and answers database for RAG systems. 

Software Architecture shall need to have prompt geneartion tightly coupled to vector database for up to date and relevant prompt generation

software architecture shall ensure that Architecture is designed in such a way not to load LLM for repeated queries to control costs.

software architecure shall need to have a monitoring system for costs incurred with LLM usage(Token usage etc.)

Software architecture shall need to have a guideline for prompt responses back from LLM.

Software architecture shall need to have a process of filtering/guradrailing  user responses to LLM.

Software architecture shall have a way  of structured response generation from LLM as per user need.

Software Architecture shall have a way of automtically quering the vector database without any human assistance like an agentic AI system.

Software Architecture shall have a way of evaluating the models used in AI assisted grading system.