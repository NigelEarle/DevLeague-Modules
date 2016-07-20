# Install Fest
If you have already installed any of these programs before, then you may skip it.

## [iTerm2](http://iterm2.com/)(osx)
* [Linux flavors](https://images.duckduckgo.com/iu/?u=http%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DJN.IPzyIkPmvjKusFebtPtiBQ%26pid%3D15.1&f=1) can use instead use the Terminal application that comes installed.

## [Oh-My-ZSH Shell](http://ohmyz.sh/)
**Scroll to the bottom of the page and find the install code for your operating system**:

- **OSX:** follow the instructions in the via curl tab
- **Linux:** follow the instructions in the via curl tab
  - **additional:** install the `git-core` package though `apt-get`: `sudo apt-get install git-core`

### Change your theme
- **OSX:** run the command: `vi ~/.zshrc`
- **Ubuntu:** run the command: `nano ~/.zshrc`

Move your cursor down with the `J` key and `L` to move right. (also, `H` is left, and `K` is Up). **YOUR MOUSE WILL NOT WORK**

In your `.zshrc` file, using the movement keys the line with the code `ZSH_THEME` and change it to `ZSH_THEME="pygmalion"`

Press `i` to go into insert mode to make changes.
When ready to save and exit, press `ESC` to leave Insert Mode and go back to Command Mode. Now you can move around again with the movement keys.

### Useful plugins
With the `.zshrc` file still open in `vi`, find the line with the code `plugins` and change it to look like the line below, order doesn't matter:

`plugins=(osx git npm brew github node sublime)`

### Enabling some helpful aliases
find the code near the bottom of the `.zshrc` file:

  # Example aliases
  # alias zshconfig="subl ~/.zshrc"
  # alias ohmyzsh="subl ~/.oh-my-zsh"

change to:

  # Example aliases
  alias zshconfig="subl ~/.zshrc"
  alias ohmyzsh="subl ~/.oh-my-zsh"

### Save and reload your configuration
While in Command Mode (press `ESC` key a few times to make sure you are in Command Mode), press the `:` key then type `x` and hit enter. You have now saved and exited  the `vi` program.

Type the command: `source ~/.zshrc` into your terminal to reload the configuration file.

## [Homebrew](http://brew.sh/#install)

### Install Node through Homebrew
run the command `brew install nodejs` (this will give us the NPM command which we will use later in this doc)

## [Sublime Text 3](http://www.sublimetext.com/3)
If you have Sublime Text 2 installed, then remove it and install 3. Version 3 is still free and has many helpful packages that Version 2 does not.

### [Package Control for Sublime Text](https://packagecontrol.io/installation)
Package control is a Package Manager to manage Sublime Text Plugins.

### [Installing a Javascript Linter](https://gist.github.com/sgnl/04fa7063183e7777e079)

### [Install suggested configuration for Sublime Text](https://gist.github.com/sgnl/0b0c5db79b16105c5fb5)


## UBUNTU/DEBIAN INSTALLING NODEJS
1. Fixing "node: no command found"-like errors
2. using n package to avoid having to symlink /usr/local/bin/nodejs to /usr/local/bin/node` on day one:

```
sudo apt-get install nodejs npm
sudo npm i -g n
sudo n stable
sudo npm i -g npm
```

### Notes
if you get errors like this:

```
/Users/lyonm028/.zshrc:3: command not found: ^M
/Users/lyonm028/.zshrc:9: command not found: ^M
/Users/lyonm028/.zshrc:12: command not found: ^M
/Users/lyonm028/.zshrc:15: command not found: ^M
/Users/lyonm028/.zshrc:18: command not found: ^M
/Users/lyonm028/.zshrc:21: command not found: ^M
/Users/lyonm028/.zshrc:24: command not found: ^M
/Users/lyonm028/.zshrc:27: command not found: ^M
/Users/lyonm028/.zshrc:30: command not found: ^M
/Users/lyonm028/.zshrc:35: command not found: ^M
/Users/lyonm028/.zshrc:40: command not found: ^M
/Users/lyonm028/.zshrc:43: command not found: ^M
/Users/lyonm028/.zshrc:48: command not found: ^M
/Users/lyonm028/.zshrc:49: command not found: ^M
/Users/lyonm028/.zshrc:51: command not found: ^M
/Users/lyonm028/.zshrc:54: command not found: ^M
/Users/lyonm028/.zshrc:source:55: no such file or directory: /Users/lyonm028/.oh-my-zsh/oh-my-zsh.sh^M
/Users/lyonm028/.zshrc:56: command not found: ^M
/Users/lyonm028/.zshrc:59: command not found: ^M
/Users/lyonm028/.zshrc:66: command not found: ^M
/Users/lyonm028/.zshrc:69: command not found: ^M
/Users/lyonm028/.zshrc:72: command not found: ^M
```

[The solution is here](https://github.com/robbyrussell/oh-my-zsh/issues/1363#issuecomment-11144048)
