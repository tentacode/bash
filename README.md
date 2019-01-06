# bash
My current `.bash_profile`, shell scripts and aliases. I hope to complete it later.

Feel free to fork it and customize it (please send me a message on [@tentacode](https://twitter.com/tentacode) if you liked it! 🙏).

![🙀(1) dotfiles (master*)$](./img/prompt.png)

## Setup

```bash
git clone git@github.com:tentacode/bash.git
cd bash
make install
source ~/.bash_profile
```

Once setup your `~/.bash_profile` has been symlinked to this repository's `dotfiles/.bash_profile`.

Also the `~/.bash_bin` symlink to this repository's `bin` folder has been created and added to your `$PATH`, making the shell scripts in the folder available from anywhere.

## [~/.bash_profile](./dotfiles/.bash_profile)

What's in my `~/.bash_profile` :

* Various aliases.
* History configuration.
* `$PATH` to add this repository's `bin` folder.
* `$CDPATH` to add my workspace directory to cd.
* Custom prompt.

## [prompt](./bin/refresh_prompt)

* Prompt display current directory (without the full path).
* Prompt displays last error code in red with a cat emoji.
* Prompt display current git branch if in a git directory.
* Prompt display a `*` if the git repository state is dirty (something to be commited)

## aliases

`histogrep` : search history for a pattern, `histogrep git` :

```bash
   90  git st
   93  git config
   94  git config --get-regexp alias
  109  gityolomend
  110  histogrep git
```

## shell scripts

[relou](./bin/relou) : finds biggest files / directory in a given directory, `relou ~` :

```bash
 35G	/Users/gabriel
 24G	/Users/gabriel/Library
6,0G	/Users/gabriel/VirtualBox VMs
1,5G	/Users/gabriel/Workspace
177M	/Users/gabriel/Dropbox
105M	/Users/gabriel/Downloads
 81M	/Users/gabriel/Movies
 75M	/Users/gabriel/Documents
 71M	/Users/gabriel/Music
 46M	/Users/gabriel/Screenshots
 46M	/Users/gabriel/Desktop
 22M	/Users/gabriel/Applications
 12M	/Users/gabriel/.gem
 ```

 (other scripts are used for `make install` or running `~/.bash_profile`).