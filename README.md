# To implement fastlane to your project, you need to make these steps below:

1. Add submodule to project at ./fastlane
```
$> git submodule add git@github.com:jsmbars/native-apps-fastlane.git fastlane
```
2. Copy `.env.fastlane.example` to the project root
3. Change `.env.fastlane.example` file name suffix to one of (.production or .development) and fill in the variables.
3. Run `bundle install` from the project root
4. Add `code-push-cli` to your project (if you don't have it yet) `yarn add code-push-cli`