# MacOS HighSierra web development setup

## 1. Xcode

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
