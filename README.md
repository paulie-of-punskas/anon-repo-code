# Info
This is a CLI tool, that is used for "anonymizing" and pushing code to:
- privacy oriented repositories (e.g. [Codeberg](https://codeberg.org)) 
- non privacy oriented (e.g. [GitHub](https://github.com))
- self-hosted instance of code forge

App removes the source code, slims down "README.md", and pushes changes to the repos found in ".git/config".
Why was it built? I do not wish my code to be used for training the "AI".

__No data is transmitted outside of URLs defined by user.__

__No telemetry is collected.__

## Requirements
- [git](https://github.com/git/git) to be installed

## CLI options
`verbose` can be combined with others, e.g. `anon-repo-code -verbose -check_dir`

__about__ - print app about content  
__check-dir__ - check if current directory contains ".git/config"  
__push-to-all__ - push content to all remote repositories  
__push-to-github__ - push redacted content to GitHub  
__push-to-non_github__ - push content to non GitHub  
__update-readme__ - print updated README (for GitHub)  
__urls__ - print remote URLs, if ".git/config" is available  
__verbose__ - enable verbosity. By default, only the most important messages will be printed.  
__version__ - print current version of the app  

## How it works
User wants to push folder content to GitHub and non github (`-push_to_all` flag).
Program reads ".git/config". If there are multiple remotes:

- send everything to non-github repository
- update README.md and remove file content, except for 
".gitignore", "NEWS.md", "README.md", "TODO.md", ".DS_Store". Push to GitHub.  

## Tests
Succesfully tested with SSH on:

- macOS Sequoia 15.7.4
- Linux Manjaro ("rolling")

## Examples
![](/examples/about.png "Result of about description")

![](/examples/flag-push-to-all.png "Example of running push-to-all flag")

# Where can I see the full source code?
  - https://codeberg.org/paulie-aus-punskas/anon-repo-code
