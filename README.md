# crossexam
A simple notebook to do RAG based interrogation of congressional bills. I threw this together in an afternoon. It's just a simple homebrew RAG setup that seems to work well for my specific use case.
It is very rudimentary and will likely require tweaking for other use cases. This one breaks the bill down into sections, subsections, and further divisions and chunks by the smallest unit it finds. Then during retrieval,
it pulls the relevant sections and provides them to the LLM for answering the question. 

# Requirements
- A running chromadb instance
- A running Ollama instance (Notebook is currently configured for a local instance)
- The ability to perform inference on a model in Ollama

# Usage
1) Edit Cell #2 to reflect your environment and preferred model
2) Click Run All
3) Scroll to the bottom, edit the question variable
4) Run the remaining cells

In addition to the answer to your question, the notebook will also provide citations to the body of the text that was RAG'd as long as it was formatted correctly.