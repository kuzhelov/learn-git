# Setting Up Repository

## git init

### git init - initializes repository for current working directory
### git init <directory> - initializes repository in the specified working directory
### git init --bare <directory> - initializes repository without working directory

### Notes

Centralized remote repository should be always created with the 'bare' flag being specified


## git clone

Clones an existing repository

### git clone <repository> - clones the repository located at 'repository' onto a local machine.
### git clone <repo> <dir> - clones the repository to 'dir'

### Notes 

This is a most common command for obtaining local development comment. It is important to understand that Git's idea is the fact that all interaction are basedon repository-to-repository collaboration. It is possible to introduce an idea of Centralized Repository that will comply with this model - though it is not the mandatory thing that Git user is obligated to follow.


## git config

### git config --global --edit - will open config file for editing

### git config --global user.name <name>
### git config --global user.email <email>
### git config --global alias <alias-name> <git-command>
### git config --system core.editor <editor>

### Notes 

Settings are placed in the following places: 

### <repo>/.git/config - Repository-specific settings
### ~/.gitconfig - User-specific settings. Settings with the --global tag are stored here
### <prefix>/etc/gitconfig - System-wide settings
