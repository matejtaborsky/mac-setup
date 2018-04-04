# MacOS HighSierra web development setup

## 1. Xcode
Install Xcode from app store

## 2. Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

add App Store integration to Homebrew
```
brew install mas
```

## 3. Brewfile
```
touch Brewfile
```

```
tap 'caskroom/cask'

brew 'git'
brew 'npm'
brew 'python'
brew 'postgresql'
brew 'mongo'
brew 'redis'
brew 'heroku'

cask '1password'
cask 'sublime-text'
cask 'slack'
cask 'harvest'
cask 'google-chrome'
cask 'firefox'
cask 'google-backup-and-sync'
cask 'dropbox'
cask 'jeromelebel-mongohub'
cask 'postico'
cask 'sourcetree'
cask 'iterm2'
cask 'caffeine'
cask 'spectacle'
cask 'sip'
cask 'vlc'
cask 'spotify'
```

```
brew bundle install
```
## 3. Setup git & GitHub

https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

## 3. Node.js

We’re going to use Node Version Manager (nvm) to install Node.js.
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.1/install.sh | bash
```
Install the latest version.
```
nvm install node
```
Restart terminal and run the final command.
```
nvm use node
```
Confirm that you are using the latest version.
```
node -v
```
You can also test with `which node`, which will output your Node path and version number.

## 4. Gulp

Install Gulp globally.
```
npm install --global gulp-cli
```
