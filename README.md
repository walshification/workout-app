# workout-app

## Dependencies

### Xcode

The easiest way to install Xcode is through the [Mac App Store](https://itunes.apple.com/us/app/xcode/id497799835). If you have already installed Xcode on your system, make sure it is version 10 or newer.

### Node

I'm not going to tell you how to manage your Node installation, but I use nodenv. If you also use nodenv and want to install the version of Node I used, just run:

```zsh
% nodenv install $(cat .node-version)
```

### iOS Simulator of the Appropriate Version

The version you install might differ based on your phone/needs. This must be installed within Xcode within the `Xcode > Preferences > Components` tab.

### Ruby and Bundler

Ruby is needed for CocoaPods, a dependency manager for Swift and Objective-C Cocoa projects. As with Node and nodenv, I use rbenv to manage Ruby installations. Then you'll want Bundler to manage the Ruby dependency. The easiest way from this project is:

```zsh
% rbenv install $(cat .ruby-version)
% gem install bundler
```

### Local Dependencies

Having taken care of the above, run the following command to install the remaining dev dependencies:

```zsh
% make deps
```

This will:

* Install [watchman](https://facebook.github.io/watchman) via [Homebrew](https://brew.sh/)
* Install [CocoaPods](https://cocoapods.org/) via [Bundler](https://bundler.io/)
* Install [React Native](https://reactnative.dev/) and its dependencies via [npm](https://www.npmjs.com/)

## Running the Development Environment

1. Start Metro by moving into the react-native project directory (`WorkoutApp`).

```sh
$ cd WorkoutApp
$ npx react-native start
```

1. Start the iOS simulator in another terminal session.

```sh
$ npx react-native run-ios
```

3. Start coding!
