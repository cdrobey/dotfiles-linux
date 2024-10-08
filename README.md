# Linux Bare Minimum Dotfiles

This repository contains my personal configuration files (dotfiles) for setting up a minimal shell environment. The configurations are tailored for a clean and efficient shell experience, with Zsh leveraging the `powerlevel9k` theme for a visually appealing and informative prompt.

## Overview

This repository includes:

- **Bash Configuration**:
  - `.bashrc`: Custom Bash configurations including aliases, prompt customization, and basic environment settings.
- **Zsh Configuration**:
  - `.zshrc`: Minimal Zsh configuration using the `powerlevel9k` theme for prompt customization.
  - `.p10k.zsh`: Configuration file for `powerlevel9k` (or `powerlevel10k`).
- **Vim Configuration**:
  - `.vimrc`: Basic Vim configuration for a streamlined editing experience.
- **Git Configuration**:
  - `.gitconfig`: Global Git configuration for aliases, user information, and other settings.

## Directory Structure

```plaintext
dotfiles/
├── .bashrc         # Minimal Bash configuration
├── .zshrc          # Minimal Zsh configuration with powerlevel9k
├── .p10k.zsh       # powerlevel9k/powerlevel10k theme configuration
├── .vimrc          # Basic Vim configuration
├── .gitconfig      # Global Git configuration
└── README.md       # This file
```

## Features

### Bash Configuration (`.bashrc`)

- **Aliases**: Commonly used command shortcuts for convenience.
- **Prompt Customization**: A simple and informative prompt displaying the current directory and user.
- **Environment Settings**: Basic environment variable settings for a clean shell experience.

### Zsh Configuration (`.zshrc`)

- **Powerlevel9k Theme**: Leverages the `powerlevel9k` theme for a powerful and customizable prompt.
- **Minimal Plugins**: Only essential plugins are loaded to keep the shell lightweight.
- **Prompt Customization**: A visually appealing prompt with useful information, including git status, current directory, and user info.
- **Path Setup**: Ensures the correct paths are added to `$PATH` for easy command execution.

### Vim Configuration (`.vimrc`)

- **Syntax Highlighting**: Enables syntax highlighting for a better coding experience.
- **Line Numbers**: Shows line numbers for easy navigation.
- **Basic Mappings**: Includes basic mappings for convenience (e.g., easier window navigation).

### Git Configuration (`.gitconfig`)

- **User Information**: Set up your global user name and email for commits.
- **Aliases**: Handy Git command shortcuts (e.g., `git st` for `git status`).
- **Color Customization**: Enables color output for Git commands for better readability.

## Installation

To set up these dotfiles on your system, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/dotfiles.git ~/dotfiles
```

### 2. Symlink the Dotfiles

Symlink the relevant dotfiles to your home directory:

```bash
# For Bash
ln -sf ~/dotfiles/.bashrc ~/.bashrc

# For Zsh
ln -sf ~/dotfiles/.zshrc ~/.zshrc
ln -sf ~/dotfiles/.p10k.zsh ~/.p10k.zsh

# For Vim
ln -sf ~/dotfiles/.vimrc ~/.vimrc

# For Git
ln -sf ~/dotfiles/.gitconfig ~/.gitconfig
```

### 3. Install Powerlevel9k or Powerlevel10k

To use the `powerlevel9k` theme, you need to install it (or `powerlevel10k`, which is a faster and more feature-rich version):

```bash
# If using Oh My Zsh:
git clone https://github.com/bhilburn/powerlevel9k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel9k

# For powerlevel10k (recommended):
git clone https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

### 4. Reload the Shell

After symlinking, reload your shell and Vim configuration:

```bash
# For Bash
source ~/.bashrc

# For Zsh
source ~/.zshrc

# Vim configuration will be applied automatically when you start Vim
```

## Customization

Feel free to customize the configurations to fit your needs. The provided configurations are designed to be minimal, making it easy to add your own aliases, functions, or environment settings.

### Customizing Powerlevel9k/Powerlevel10k

If you're using `powerlevel10k`, run the configuration wizard to customize your prompt:

```bash
p10k configure
```

You can edit the `.p10k.zsh` file directly to customize the prompt further.

### Adding Aliases

To add your own aliases, simply edit the `.bashrc`, `.zshrc`, or `.gitconfig` file:

```bash
# Example alias in .bashrc or .zshrc
alias gs='git status'

# Example alias in .gitconfig
[alias]
    co = checkout
    br = branch
    ci = commit
    st = status
```

## Contributing

If you have suggestions or improvements, feel free to open an issue or submit a pull request. Contributions are welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```

This `README.md` now includes `.gitconfig` and `.vimrc` in the list of dotfiles managed by your repository, and provides instructions on how to set them up.
