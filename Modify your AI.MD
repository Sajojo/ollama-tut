## Wait.. what? You want to modify your AI Assistant to sound like Mario?

Well look no further, there's already a forum explaining this. https://www.gpu-mart.com/blog/custom-llm-models-with-ollama-modelfile
--
But don't worry I'll try to make it easier to follow.
--

## What we're trying to do
Take the existing the LLM model, for the sake of this example let's take llama3

### We wanna make a copy of that modelfile
ollama show llama2:latest --modelfile
