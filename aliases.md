##############################
# Git Aliases
##############################
# Adding and committing changes
alias ga='git add .'                     # Stage all changes
alias gaa='git add -A'                   # Stage all changes including deleted files
alias gc='git commit -m'                 # Commit with a message
alias gca='git commit -am'               # Add and commit in one command
alias gcm='git commit --amend'           # Amend last commit

# Branch management
alias gch='git checkout'                 # Switch to a branch
alias gchb='git checkout -b'             # Create and switch to a new branch
alias gb='git branch -a'                 # List all branches
alias gbd='git branch -d'                # Delete branch
alias gbD='git branch -D'                # Force delete branch
alias gm='git merge'                     # Merge branch

# Status and logs
alias gs='git status'                    # Show status
alias gss='git status -s'                # Short status
alias gl='git log --oneline --graph --decorate'  # Pretty log
alias gll='git log --oneline --graph --decorate --all -10'  # Last 10 commits all branches
alias glp='git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short'

# Pulling and pushing
alias gpl='git pull'                     # Pull from current branch
alias gps='git push'                     # Push to current branch
alias pull='git pull origin main'       # Pull from main
alias push='git push origin main'       # Push to main
alias gpsu='git push -u origin $(git branch --show-current)'  # Push and set upstream

# Diffs and resets
alias gd='git diff'                      # Show diff
alias gdc='git diff --cached'           # Show staged diff
alias grh='git reset HEAD'              # Unstage files
alias grm='git reset --mixed'           # Mixed reset
alias grs='git reset --soft'            # Soft reset
alias grhard='git reset --hard'         # Hard reset (careful!)

# Stashing and miscellaneous
alias gsta='git stash'                   # Stash changes
alias gstap='git stash pop'             # Pop latest stash
alias gstaa='git stash apply'           # Apply stash without removing
alias gstal='git stash list'            # List stashes
alias gra='git remote -v'               # Show remotes
alias gf='git fetch'                    # Fetch from remote
alias gco='git checkout'                # Shorter checkout
alias gcl='git clone'                   # Clone repository

##############################
# VS Code & Editors
##############################
alias cw='code -n'                      # Open new window
alias v='vim'                           # Vim editor
alias nv='nvim'                         # Neovim (if installed)

##############################
# Laravel Aliases
##############################
# Artisan commands
alias pa='php artisan'                  # Base artisan command
alias pas='php artisan serve'           # Start development server
alias pat='php artisan tinker'          # Laravel REPL
alias pal='php artisan list'            # List all commands

# Migrations and database
alias pam='php artisan migrate'         # Run migrations
alias pamf='php artisan migrate:fresh --seed'  # Fresh migration with seeds
alias parm='php artisan migrate:rollback'      # Rollback migration
alias pams='php artisan migrate:status' # Migration status
alias seed='php artisan db:seed'        # Run seeders

# Cache and optimization
alias pao='php artisan optimize'        # Optimize for production

##############################
# Navigation and File Management
##############################
# Navigation shortcuts
alias ..='cd ..'                        # Go up one directory
alias ...='cd ../..'                    # Go up two directories
alias ....='cd ../../..'                # Go up three directories
alias ~='cd ~'                          # Go to home directory
alias cdr='cd $(git rev-parse --show-toplevel)'  # Go to git root
alias cdp='cd -'                        # Go to previous directory

##############################
# Terminal and System
##############################
alias cls='clear'                       # Clear screen
alias c='clear && printf "\e[3J"'       # Clear screen and scrollback
alias h='history'                       # Show command history
alias hg='history | grep'               # Search command history
alias reload='source ~/.bashrc'         # Reload bash configuration
alias bashrc='vim ~/.bashrc'            # Edit bash configuration
alias aliases='vim ~/.bash_aliases'     # Edit aliases file

# Process management
alias allprocess='ps aux'               # Show all processes

##############################
# Database Aliases
##############################
alias sql='mysql -u root -p'           # MySQL root login
alias psql='sudo -u postgres psql'     # PostgreSQL login

##############################
# Docker Aliases
##############################
alias dc='docker compose'              # Docker Compose
alias dcu='docker compose up -d'       # Start containers in background
alias dcd='docker compose down'        # Stop containers
alias dcr='docker compose restart'     # Restart containers
alias dcl='docker compose logs -f'     # Follow logs
alias dps='docker ps'                  # List running containers
alias dpsa='docker ps -a'              # List all containers
alias di='docker images'               # List images
alias dexec='docker exec -it'          # Execute command in container
alias dlogs='docker logs -f'           # Follow container logs
