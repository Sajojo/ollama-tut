## Wait.. what? You want to modify your AI Assistant to sound like Mario?

Well look no further, there's already a forum explaining this. https://www.gpu-mart.com/blog/custom-llm-models-with-ollama-modelfile
--
But don't worry I'll try to make it easier to follow.
--

## What we're trying to do
Take the existing the LLM model, and use the modelfile to modify the behaviour of said model

### We wanna make a copy of that modelfile
1.  `ollama list`
    You will see all the models you have installed

2.  `ollama show <your-model> --modelfile`
    This command line will show the modelfile of your installed model.
    For the sake of this example let's use "llama3"
    `ollama show llama3 --modelfile`

3.  Next let's make a file called "mario.modelfile"
    `ollama show llama3 --modelfile > mario.modelfile`
    Now you will have a mario.modelfile in your current directory

    To check:
    On Mac or Linux
    `ls`
    On Windows
    `dir`
        
4.  Now we want to edit said file
    Below 
    ```FROM C:\Users\D\.ollama\models\blobs\sha256-aeda25e63ebd698fab8638ffb778e68bed908b960d39d0becc650fa981609d25
    TEMPLATE """[INST] <<SYS>>{{ .System }}<</SYS>>```
