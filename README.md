# zsh-ollama-command

An [`oh-my-zsh`](https://ohmyz.sh) plugin that integrates the OLLAMA AI model 
with [fzf](https://github.com/junegunn/fzf) to provide intelligent command 
suggestions based on user input requirements.

## Features

* **Intelligent Command Suggestions**: Use OLLAMA to generate relevant
  terminal commands based on your query or input requirement.
* **FZF Integration**: Interactively select suggested commands using FZF's fuzzy
  finder, ensuring you find the right command for your task.
* **Customizable**: Configure default shortcut, OLLAMA model, and response number
  to suit your workflow.

## Requirements

* `jq` for parsing JSON responses
* `fzf` for interactive selection of commands
* `curl` for making API requests
* `OLLAMA` server running

## Configuration Variables

| Variable Name                | Default Value            | Description                                    |
|------------------------------|--------------------------|------------------------------------------------|
| `ZSH_OLLAMA_MODEL`           | `llama3`                 | OLLAMA model to use (e.g., `llama3`)           |
| `ZSH_OLLAMA_COMMANDS_HOTKEY` | `Ctrl-o`                 | Default shortcut key for triggering the plugin |
| `ZSH_OLLAMA_COMMANDS`        | 5                        | Number of command suggestions displayed        |
| `ZSH_OLLAMA_URL`             | `http://localhost:11434` | The URL of OLLAMA server host                  |
| `ZSH_OLLAMA_OS_FLAVOUR`      | `Linux (Fedora 42)`      | OS/Flavour for terminal commands               |

## Usage

1. Clone the repository to `oh-my-zsh` custom plugin folder
    ```bash
    git clone https://github.com/plutowang/zsh-ollama-command.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-ollama-command
    ```

2. Enable the plugin in ~/.zshrc:
    ```bash
    plugins=(
      [plugins...]
      zsh-ollama-command
    )
    ```
3. Input what you want to do then trigger the plugin. Press the custom shortcut (default is Ctrl-o) to start
   the command suggestion process.
4. Interact with FZF: Type a query or input requirement, and FZF will display
   suggested terminal commands. Select one to execute.

**Get Started**

Experience the power of AI-driven command suggestions in your terminal! This
plugin is perfect for developers, system administrators, and anyone looking to
streamline their workflow.

Let me know if you have any specific requests or changes!
