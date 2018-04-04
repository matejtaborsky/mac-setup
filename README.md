# MacOS HighSierra web development setup

## 1. Xcode
Install Xcode from app store.

## 2. Homebrew
Install Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Add App Store integration to Homebrew
```
brew install mas
```

## 3. Brewfile
Install all libraries and apps in one step via script
```
touch Brewfile
```
Edit `Brewfile` and paste/modify the list
```
tap 'caskroom/cask'

brew 'git'
brew 'npm'
brew 'python'
brew 'rbenv'
brew 'rbenv-gemset'
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
Install the libraries and apps
```
brew bundle install
```

After you `brew install postgresql` you can initialize or stop the postgresql daemon with these commands: `brew services start postgresql` or `brew services stop postgresql`. This also stnad for all other deamons - mongo,redis. See `brew services list` for installed services. 

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

## 5. Ruby
Use rbenv to install Ruby versions out of the box. Run `rbenv init` and add to the `~/.bash_profile`.
```
eval "$(rbenv init -)"
```
Close terminal, and check if rbenv is configured properly via rbenv-doctor script
```
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash
```
```
# List of Ruby versions: 
rbenv install -l

# Install Ruby version:
rbenv install 2.5.1

# Use local Ruby
rbenv local 2.5.1
```
Install Bundler
```
gem install bundler
```
Rehash the ruby env
```
rbenv rehash
```
