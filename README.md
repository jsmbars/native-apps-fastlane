# native-apps-fastlane

** Installation **

To implement fastlane to your project, you need to make these steps below:

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

** Versioning **

List of releases can be found here https://github.com/jsmbars/native-apps-fastlane/releases

Tags naming convention:
* `v<manjor>.<minor>.<dic> eg. v3.4.3` - Using semvar Major is for breaking changes, minor number for new features (no breaking changes) fixes is for fixes with no breaking changes

Checking tags from local repo:
1) `git ls-remote --tags` - will show list of remote tags
2) `git tag` - will show list of local tags
3) `git describe --abbrev=0 --tags` - will show current local tag

Creating tags:
1) Merge feature-branch PR into master
2) In your local repo checkout master branch and pull the last changes (with merge commit)
3) Add local tag `git tag tagname`
4) Push tag to remote repo `git push origin tagname`

