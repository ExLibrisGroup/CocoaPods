# Installation instructions

These are instructions to install this custom version of cocoapods.

## Prerequisites

You need `Ruby` installed in your Mac. Usually it comes along with the system, but it's recommended you install [rbenv](https://github.com/rbenv/rbenv#how-rbenv-hooks-into-your-shell) in order to use a more recent version of ruby. Also this will help you overcome all the problems with permissions. Follow the [installation instructions](https://github.com/rbenv/rbenv#installation) to install it. Once you have ran rbenv-doctor as mentioned in step 4 of installation paragraph you're good to go.

## Steps

1. Clone this project in a local folder.
2. Open a terminal.
3. Verify that you don't have cocoapods already installed. Run `pod --version`. If the terminal replies with an error it means that is not installed. If instead it replies with a version you need to uninstall cocoapods using `gem uninstall cocoapods`.
4. Run `sudo gem install bundler` to install bundler.
5. Run `bundle exec rake bootstrap` to install all the dependencies of the project.
6. Run `bundle exec rake build` to build the project. A file named `cocoapods-1.10.0.gem` will be created in the just created folder called `pkg`
7. Run `gem install <PATH-TO-GEM>`. Replace `<PATH-TO-GEM>` with the path of the gem created in the previous step. In my case was `gem install /Users/paolo/Projects/CocoaPods/pkg/cocoapods-1.10.0.gem`
8. Run `pod --version` to verify that you have this version installed.