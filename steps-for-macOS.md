# `.zshrc` file for mac

```
# path to oh-my-zsh installation
export ZSH="/Users/nicolasemkis/.oh-my-zsh"

# theme setting
# more themes here: https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
ZSH_THEME="spaceship"

# just cool plugins
plugins=(
  git
  node
  yarn
  zsh-syntax-highlighting
  zsh-autosuggestions
  zsh-completions
)

# permission to zsh use root
ZSH_DISABLE_COMPFIX=true

# i've no idea, just leave this line here
source $ZSH/oh-my-zsh.sh

# spaceship theme customizations
SPACESHIP_PROMPT_ORDER=(
  user          # Username section
  dir           # Current directory section
  host          # Hostname section
  git           # Git section (git_branch + git_status)
  hg            # Mercurial section (hg_branch  + hg_status)
  node          # Node.js section
  exec_time     # Execution time
  line_sep      # Line break
  vi_mode       # Vi-mode indicator
  jobs          # Background jobs indicator
  exit_code     # Exit code section
  char          # Prompt character
)

SPACESHIP_PROMPT_ADD_NEWLINE=true     # add a new line after executing a command
SPACESHIP_CHAR_SYMBOL="⤷"             # custom symbol
SPACESHIP_CHAR_SUFFIX=" "             # character after the arrow
SPACESHIP_NODE_PREFIX=""              # removes prefix before node version

# definig path for yarn global packages
export PATH="$(yarn global bin):$PATH"

# defining path for nvm
export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && . "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion

# custom aliases
# for a full list of active aliases, run `alias`.
alias zshConfig="code ~/.zshrc"
alias zshHistory="code ~/.zsh_history"
```