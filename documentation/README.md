# REI-Cedar Roadmap to V2

# Distribution 
- **NPM Compositions**(v2)
  [x] Compositions are available from npm @alltayl@rei.com
  [x]  Compositions successfully abstracts it dependencies @alltayl@rei.com
  [ ] The documentation for compositions is shared on npm and github. @alltayl@rei.com @Lance H
  [x] The version of a dependency remains  intact when the non dependency of the same type is at a separate version @alltayl@rei.com
  [ ]  The documentation maps to correct version of a dependency @alltayl@rei.com @Lance H
[ ] Debug merging NPM packages back into mainline (v2)
- test environment (v2)
  - investigate using this as a sample project for component usage how too’s
  [ ] spike on test environment @alltayl@rei.com @Lance H
    [ ] outline what problems this will solve [here](/doc/REI-Cedar-Quality-bcwHtHy3u5DH2O7m8VUNe) @alltayl@rei.com @Michael H
    [ ] identify potential solutions and needs 
  [ ] Take results from spike and build out test environment @alltayl@rei.com @Lance H
  [ ] Identify and integrate sanity testing for dependency requirements: @alltayl@rei.com @Lance H
    - (potential option) investigate  [**don’t break**](https://github.com/bahmutov/dont-break) ****-Checks if the node module in the current folder breaks unit tests for specified dependent projects.
      [ ]  spike on if this provides additional stability to our deliverables 
      [ ]  is appropriate within the module testing environment
  - [india](https://github.com/bcherny/india) -INDIA looks at your file's exports, and parses the jsdoc for each exported method. It then diffs the jsdocs at the given git commits, and runs the resultant diff through its validation rules. Based on the result, INDIA suggests an appropriate next version for your file.
      [ ]  spike on if this provides additional stability to our deliverables 
      [ ]  is appropriate within the module testing environment
- Updating multiple packages within a bundle 
  - when one is a breaking change
- tool to track/report on usage of cedar components from NPM
  - https://www.npmjs.com/package/module-usage
- **Documentation**(v2)
  [ ] Create a new package @alltayl@rei.com
  [ ] Update a package @alltayl@rei.com
  [ ] Consume a module @Lance H
  [ ] Contribute @Michael H @alltayl@rei.com @Lance H
  [ ] Log an issue @Michael H
  [ ] Request a feature enhancement @Michael H
[ ] kitchen sink / various bundling (post v2)
- Distribution of Utility css onto REI.com
  [ ] investigate Renderman @Michael H @alltayl@rei.com
  [ ] investigate Satchel
- Distribution of Global css files 
  [ ] requirements @Lance H @Michael H
  [ ] investigate Renderman @Michael H @alltayl@rei.com
  [ ] investigate Satchel
# Server-side rendering (post v2)
[ ] Investigate options @alltayl@rei.com @Lance H
  [ ] nashhorn: https://medium.com/@jimmy_shen/use-nashorn-engine-to-do-server-side-rendering-with-react-eba835e33d77 |  https://github.com/vuejs/vue/issues/5415 
  [ ]  [nuxt](https://nuxtjs.org/guide)
  [ ] custom
[ ] provide sample implementations @alltayl@rei.com
  [ ] Node
  [ ] Java
  [ ] .net?
[ ] Work with platform to provided access to preferred solution for REI.com @Michael H


----------
# Architecture
- **Monorepo with multiple projects**
[x] [**Lerna**](https://github.com/lerna/lerna) **-** Splitting up large codebases into separate independently versioned packages is extremely useful for code sharing. However, making changes across many repositories is *messy* and difficult to track, and testing across repositories gets complicated really fast. @alltayl@rei.com
- **Testing** (v2)
  [x] Unit testing
    [x] Migrate to  [Jest](https://facebook.github.io/jest/) @Lance H
    [x] Unit test updates @Lance H
    [x] Snapshot tests(V2) @Lance H
    [x] Increased unit test code coverage(V2) @Lance H
[ ] Cross Browser testing ( post v2 )
  [ ] Assess and document available solutions
    [ ] https://github.com/gemini-testing/gemini
    [ ] others
  [ ] Prototype chosen solution
  [ ] Integrate prototype into mainline
  
- **Reports and Tracking**
  [ ] Analytics
    [ ] Component analytic hooks: for tracking usage of components/ allowing easy tagging for teams
  [ ] Accessibility


- G**lobal css concerns and dependencies** (post v2)
  [ ] reduce global reset and refactor into pattern parts
  [ ] Utility css
  
- **Theming** (post v2)
  [ ] Site themes
    [ ] multiple brand.ai files to switch between
  [ ] Component themes
    [ ] [css modules](https://github.com/css-modules/css-modules)
    
- **Vue.js component a/b testing** 
  [ ] ([example](https://github.com/fromAtoB/vue-a2b)) - *vue-a2b* uses [named slots](https://vuejs.org/v2/guide/components.html#Named-Slots) for defining test variations. Any amount of variations is supported (A/B/n). The the variation identifier should be used as slot name and can be any valid string. Selection chances are given as ratio. In the first example, **test A** has twice the chance to be selected over **test B**:
- **Standardizing communication** (v2)
  - [**commitizen**](https://github.com/commitizen/cz-cli) - When you commit with Commitizen, you'll be prompted to fill out any required commit fields at commit time. No more waiting until later for a git commit hook to run and reject your commit (though [that](https://github.com/kentcdodds/validate-commit-msg) can still be helpful). No more digging through [CONTRIBUTING.md](https://github.com/commitizen/cz-cli/blob/master/CONTRIBUTING.md) to find what the preferred format is. Get instant feedback on your commit message formatting and be prompted for required fields.
  - [**Conventional changelog**](https://github.com/conventional-changelog/standard-version) - Automatic versioning and CHANGELOG generation, using GitHub's squash button and [conventional commit messages](https://conventionalcommits.org/).
  - [**Semantic release**](https://github.com/semantic-release/semantic-release) ****(spike)
  - [**Git release notes**](https://github.com/ariatemplates/git-release-notes) (spike)
  - CSS Table of Contents 
- **Commit hardening** 
  [ ] Backstop on travis (v2) @Lance H
  - [**cracks**](https://github.com/semantic-release/cracks) (spike This module can automatically detect breaking changes by running the test suite of your last-release against the current codebase. That shouldn't fail.)
  - [**don’t break**](https://github.com/bahmutov/dont-break) (spike Checks if the current version of your package would break dependent projects)
  [x]  [**istanbul**](https://github.com/gotwarlost/istanbul) (used by Jest) @Lance H
  - [**codecov**](https://codecov.io/) reports on test coverage of feature updates and will auto fail build if degritory
- **Documentation**(v2)
  [ ] Create a component
  [ ] Create a composition
  [ ] Update a component or composition
  [ ] Silver Task ForceAdd or update a modifier
  [ ] Create a new pattern
  [ ] Log an issue
  [ ] Request a feature enhancement
- **Maintenance** (v2)
  - Vue updates
  - Version management 
- Automate updating of gh-pages/patterns docs site with new versions


----------
# Docs 
[ ] Assess where this documentation should live
  1. Separate git project 
  2. Cedar
  3. Shared DDS Google drive
[ ] Diagrams
    [ ] Ecosystem of Cedar2
    [ ] Component anatomy 
    [ ] Composition anatomy 
    [ ] Organism scaffold 
    [ ] Page scaffold
  [ ] Support matrix
[ ] How to Use guides
  [ ] Component and Composition API docs (v2)
  - [tips on how to write a “how to”](https://medium.com/@rachel.sobel/how-to-write-technical-how-tos-4279d2534786)
    [ ] Build a component
    [ ] Request an enhancement or feature 
    [ ] Build a composition
    [ ] Build a template
    [ ] Using Cedar on my page
  [ ] Setup guides (v2)
    [ ] Webpack set-up docs
    [ ] Migration documentation
  [ ] Style-guide (v2)
    [ ] first pass @Michael H
- What features do our documentation solutions require?
  [ ] Search
  [ ] Markdown
  [ ] Versioning
  [ ] Navigation
  [ ] Branding
  [ ] Connected Design and Development documentation
  [ ] Able to contribute to without development 
  [ ] Able to be designed to spec
- Vet potential documentation solutions
  [ ] [styleguidest](https://github.com/vue-styleguidist/vue-styleguidist)
  [ ] https://github.com/PharkMillups/beautiful-docs
  [ ] https://docsify.js.org/


----------


# UI Bugs
[ ] Move from 10px base rem to browser default to correct a11y/usability
- button missing 


# Features
[ ] [V2.0 list of components available](https://docs.google.com/spreadsheets/d/1LDGIt42ulrlWcJXajD6rscHaRDA6R64iTE2IR_m1jps/edit#gid=0) 
- Components (post v2)

 

# WYSIWYG

theme of Cedar for content team applications 


# Education
[ ] biweekly meetings with PO’s / open to interested parties on updates and roadmap
# Governence


