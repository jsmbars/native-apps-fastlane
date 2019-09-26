# To implement fastlane to your project, you need to make these steps below:

1. Add submodule to project at ./fastlane
```
$> git submodule add git@github.com:jsmbars/native-apps-fastlane.git fastlane
```
2. Create Gemfile in the project root with lines below or add these lines if the file already exist
```
fastlane_gemfile_path = File.join(File.dirname(__FILE__), 'fastlane', 'Gemfile')
eval_gemfile(fastlane_gemfile_path) if File.exist?(fastlane_gemfile_path)
```
3. Run `bundle install` from the project root
4. Copy `.env.fastlane.example` to the project root
5. Change `.env.fastlane.example` file name suffix to one of (.production or .development) and fill in the variables.

6. Add `code-push-cli` to your project `yarn add code-push-cli`