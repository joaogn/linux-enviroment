# Enviroment Linux Configuration

## Steps

- Install git
  - `sudo apt-get install git`
- Configure git
  - `git config --global user.name "Your name here"`
  - `git config --global user.email "your_email@example.com"`
  - `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
  - `vi ~/.ssh/id_rsa.pub` (copy ssh Key)
  - Add ssh key on github
    - https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account
- Install vscode
  - https://code.visualstudio.com/
- Install Dracula Theme vscode
- Install Font FiraCode
  - https://github.com/tonsky/FiraCode
- Install Core Extesions
  - vscode-icons
  - Color Highlight
  - EditorConfig
  - ESLint
  - Prettier
  - Rocketseat ReactJS
  - Rocketseat React Native
- Configure vscode settings.json (ctrl+shift+p)

```json
{
  "workbench.colorTheme": "Dracula",
  "editor.fontFamily": "Fira Code",
  "editor.fontLigatures": true,
  "editor.fontSize": 16,
  "editor.lineHeight": 24,
  "workbench.iconTheme": "vscode-icons",
  "editor.formatOnSave": true,
  "[typescript]": {
    "editor.formatOnSave": false
  },
  "[typescriptreact]": {
    "editor.formatOnSave": false
  },
  "editor.rulers": [80, 120],
  "editor.tabSize": 2,
  "editor.renderLineHighlight": "gutter",
  "terminal.integrated.fontSize": 14,
  "emmet.syntaxProfiles": {
    "javascript": "jsx",
    "typescript": "tsx"
  },
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "typescript": "typescriptreact"
  },
  "javascript.updateImportsOnFileMove.enabled": "never",
  "breadcrumbs.enabled": true,
  "editor.parameterHints.enabled": false,
  "prettier.eslintIntegration": true,
  "eslint.autoFixOnSave": true,
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    {
      "language": "typescript",
      "autoFix": true
    },
    {
      "language": "typescriptreact",
      "autoFix": true
    }
  ]
}
```

- Configure Font FiraCode Retina on Terminal
- Configure Theme Dracula on Terminal
  - https://github.com/dracula/gnome-terminal
- Install Oh My Zsh
  - `sudo apt-get update`
  - `sudo apt-get install zsh`
  - `sudo apt-get install curl`
  - https://ohmyz.sh/ (install via curl)
- Making Zsh Default Shell
  - `whereis zsh`
  - `sudo usermod -s /usr/bin/zsh $(whoami)`
  - `sudo reboot`
- Install Oh My Zsh SpaceShip

  - https://github.com/denysdovhan/spaceship-prompt
  - install via oh-my-zsh
  - code ~/.zshrc

    - change ZSH_THEME to `"spaceship"`
    - add endfile

      ```
      SPACESHIP_PROMPT_ORDER=(
      user          # Username section
      dir           # Current directory section
      host          # Hostname section
      git           # Git section (git_branch + git_status)
      hg            # Mercurial section (hg_branch  + hg_status)
      exec_time     # Execution time
      line_sep      # Line break
      vi_mode       # Vi-mode indicator
      jobs          # Background jobs indicator
      exit_code     # Exit code section
      char          # Prompt character
      )

      SPACESHIP_PROMPT_ADD_NEWLINE=false
      SPACESHIP_CHAR_SYMBOL="❯"
      SPACESHIP_CHAR_SUFFIX=" "
      ```

  - reload terminal

- Install Plugins Terminal
  - https://github.com/zdharma/zplugi (install from automatic option)
  - code ~/.zshrc
    - add endfile
      ```
      zplugin light zsh-users/zsh-autosuggestions
      zplugin light zsh-users/zsh-completions
      zplugin light zdharma/fast-syntax-highlighting
      ```
  - reload terminal
- Install Chrome Extensions
  - React Developer Tools
  - Dracula DevTools Theme
    - see how to install
- Install Postman
  - `wget https://dl.pstmn.io/download/latest/linux64 -O postman.tar.gz`
  - `sudo tar -xzf postman.tar.gz -C /opt`
  - `rm postman.tar.gz`
  - `sudo ln -s /opt/Postman/Postman /usr/bin/postman`
  - ```
    cat > ~/.local/share/applications/postman.desktop <<EOL
    [Desktop Entry]
    Encoding=UTF-8
    Name=Postman
    Exec=postman
    Icon=/opt/Postman/app/resources/app/assets/icon.png
    Terminal=false
    Type=Application
    Categories=Development;
    EOL
    ```
- Install DevDocs
  - https://devdocs.egoist.moe/
- Install NodeJs
  - Install nvm
    - https://github.com/nvm-sh/nvm
    - Reload terminal
  - `nvm install 10.15.3`
  - `nvm alias default 10.15.3`
- Install Yarn
  - https://yarnpkg.com/pt-BR/docs/install#debian-stable
- Install Docker
  - https://docs.docker.com/install/linux/docker-ce/ubuntu/
  - https://docs.docker.com/install/linux/linux-postinstall/
- Install Postgres
  - docker run --name database -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres
  - https://electronjs.org/apps/postbird
