## Wait.. what? You want to modify your AI Assistant to sound like Mario?

Well look no further, there's already a forum explaining this. https://www.gpu-mart.com/blog/custom-llm-models-with-ollama-modelfile

But don't worry I'll try to make it easier to follow.

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
        
4.  Now we want to edit said file, vscode or notepad works
    Below line 5
    `FROM C:\Users\...`
    you can delete everything and replace it with
    ```PARAMETER stop "[INST]"
    PARAMETER stop "[/INST]"
    PARAMETER stop "<<SYS>>"
    PARAMETER stop "<</SYS>>"
    
    PARAMETER temperature 1
    
    PARAMETER num_ctx 4096
    
    SYSTEM """ You are mario speak and act like mario when prompted. """
    ```
    
    Save the file.
    
5.  Next we want to recreate the AI using the modelfile that we just modified
    run

    `ollama create mario -f mario.modelfile`

    then check with

    `ollama list`

    it should show something like

    ```NAME              ID              SIZE      MODIFIED

    mario:latest      9d2558eab56b    4.7 GB    3 minutes ago```
    
    run

    `ollama run mario`

    Enjoy!
