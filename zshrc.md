# Path to your Oh My Zsh installation
export ZSH="$HOME/.oh-my-zsh"

# Theme
ZSH_THEME="robbyrussell"

# Plugins
plugins=(git zsh-autosuggestions zsh-completions)

# Load completions
autoload -Uz compinit
compinit

# Load Oh My Zsh
source $ZSH/oh-my-zsh.sh

# Add custom PATH
export PATH="$HOME/.local/bin:$PATH"

# Oh My Posh prompt theme
eval "$(oh-my-posh init zsh --config ~/.poshthemes/json.omp.json)"

# Enable bash aliases if they exist
if [ -f ~/.bash_aliases ]; then
  source ~/.bash_aliases
fi

# Load NVM (Node Version Manager)
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"

# FZF keybindings (optional: if copied to home directory)
[ -f ~/.fzf-key-bindings.zsh ] && source ~/.fzf-key-bindings.zsh

# Fuzzy search command history with Ctrl+R using FZF
__fzf_history_search() {
  BUFFER=$(history | fzf --tac +s --reverse | sed 's/ *[0-9]* *//')
  CURSOR=${#BUFFER}
  zle redisplay
}
zle -N __fzf_history_search
bindkey '^R' __fzf_history_search


export PATH="$PATH:$HOME/.config/composer/vendor/bin"
