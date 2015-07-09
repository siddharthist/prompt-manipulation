# prompt-manipulation
Manipulate bash/zsh prompts in your shell scripts!

### Installation
```bash
wget TODO
```

### Usage
```bash
source prompt_manipulation.sh
```
or
```bash
. prompt_manipulation.sh
```
and then just call one of the functions!

### Provided functions
```bash
# Description: Echos the prompt prefix as a string
# Arguments: none
function current_prompt() {
    ...
}

# Description: Prefixes the user's shell prompt with a given string.
# Arguments: string to put in front of the prompt.
function prefix_prompt() {
    ...
}

# Description: Suffixes the user's shell prompt with a given string.
# Arguments: string to put behind the prompt.
function suffix_prompt() {
    ...
}

# Description: Replaces the user's shell prompt with a given string.
# Arguments: string to replace the prompt.
function replace_prompt() {
    ...
}

# Description: Reset the prompt to whatever it was before your script ran.
# Should be called every time you use one of the above functions.
# Arguments: none
function reset_prompt() {
    ...
}
```

### Examples

Prompt: `$ `
Code: `prompt_prefix "prompt"`
Prompt: `prompt$ `
Code: `reset_prompt`
Prompt: `$ `

Prompt: `user@hostname `
Code: `prompt_suffix "DB>"`
Prompt: `user@hostname DB>`
Code: `reset_prompt`
Prompt: `user@hostname `

Prompt: `user [11:09:56]>`
Code: `prompt_replace ">>>"`
Prompt: `>>>`
Code: `reset_prompt`
Prompt: `user [11:09:56]>`
