# Pareidolia - Detecting patterns? A prototype Use Case for LLM, GPT, langchain and vector databases

 Generative AI and Large Language Models (LLM) are opening up far-reaching possibilities beyond "smart search" and "generating pretty pictures". And this without having to train or fine-tune the models (although that is definitely possible).

Langchain allows you to connect a Large Language Model like GPT4 to your own sources of data like an entire database filled with your own data like customer data or a collection of documents (reports, images) etc. which then becomes visible to the LLM, can search it and provide answers to questions about the data. And langchain allows to perform actions based on the questions and their answers, like agents interacting with external API's.

This project is a prototype Use Case: connect a LLM to a collection of CV's and resource planning & allocation system and it is possible to have the AI, as a response to particular resource request, propose team compositions at a particular date, which would be very handy in the outsourcing industry.

[LangChain Explained in 13 Minutes | QuickStart Tutorial for Beginners](https://youtu.be/aywZrzNaKjs)
## Installation

Clone the repository. Use the dependency and package manager [Poetry](https://python-poetry.org/) to install all the dependencies of vein.

```bash
poetry install
```
## Configuration for usage with OpenAI (Visual Studio Code)

Create a text file _"dev.env"_ in the root of the project. This will contain the "OPENAI_API_KEY" environment variable used by the application to obtain the token associated to a valid OpenAI account when calling the API.

```bash
OPENAI_API_KEY=sk-A_seCR_et_key_GENERATED_foryou_by_OPENAI
```

The environment variable is loaded into the execution context of the application when run in the debugger if as such specified in the file _"launch.json"_. An example launch configuration shows how:

```json
{   //example launch configuration
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File",
            "type": "python",
            "request": "launch",
            "program": "app.py",
            "console": "integratedTerminal",
            "justMyCode": true,
            "envFile": "${workspaceFolder}/dev.env"
        }
    ]
}
```

## Configuration for usage with OpenAI (JupyterLab)

The OPENAI_API_KEY should be loaded in an Environment Variable before starting jupyter-lab. This can be by setting the OPENAI_API_KEY environment variable before starting the JupyterLab executable. For example, in Powershell on Windows you can create a file "devenv.ps1" with the following content:

```powershell
$Env:OPENAI_API_KEY="sk-A_seCR_et_key_GENERATED_foryou_by_OPENAI"
. jupyter-lab.exI
```

And on Mac and Linux you can create a file "devenv.sh" with the following content:

```bash
#!/bin/bash
export OPENAI_API_KEY=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
jupyter-lab
```

## Usage
[Activate the Python virtual environment](https://python-poetry.org/docs/basic-usage/#activating-the-virtual-environment) with

```bash
poetry shell
```

Running the Jupyter environment with the aformentioned scripts. On Linux:

```bash
./devenv.sh
```

and on Windows:

```powershell
./devenv.ps1
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Copyright and license

Copyright © 2023 Iwan van der Kleijn

Licensed under the MIT License 
[MIT](https://choosealicense.com/licenses/mit/)