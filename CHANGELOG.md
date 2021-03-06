## Change Log

### v1.0.0

  **New** Language agnostic bridge for hooks in Python and Ruby

- [#230](https://github.com/apiaryio/dredd/pull/230) Language agnostic hooks bridge & transaction compiler extraction (@netmilk, @w-vi, @kuba-kubula)

### v0.6.1

  **New** Added `beforeValidation` and `beforeEachValidation` hooks

  **New** Added `general` property under results object for each `testStep` and `transaction` for adding other then Gavel errors

  **New** Connection errors are handled in scope of each step, emmited to reporter as `test error` and added as a general error `general`

  **New** Apiary reporter failure is gracefully handled and will not brake build



- [#229](https://github.com/apiaryio/dredd/pull/229) Clean beforeResults for every gavelResult iteration (@netmilk)
- [#222](https://github.com/apiaryio/dredd/pull/222) Report skipped and programatically failed transactions (@netmilk)
- [#228](https://github.com/apiaryio/dredd/pull/228) Updated the MkDocs config from the deprecated format (@d0ugal)
- [#224](https://github.com/apiaryio/dredd/pull/224) Support for before validation hooks (@netmilk, @nevir)
- [#219](https://github.com/apiaryio/dredd/pull/219) Connection errors in gavel error interface (@netmilk)
- [#218](https://github.com/apiaryio/dredd/pull/218) Public:true/false Apiary reporter, based on token and api-name (suite) existence (@kuba-kubula)
- [#216](https://github.com/apiaryio/dredd/pull/216) Update documentation, fix a few typos/leftovers, line wrapping, how-to changelog (@kuba-kubula)
- [#212](https://github.com/apiaryio/dredd/pull/212) Gracefully handle connection errors to server under test (@netmilk)
- [#214](https://github.com/apiaryio/dredd/pull/214) Fixed example with modifying request URI, closes #186 (@netmilk)
- [#213](https://github.com/apiaryio/dredd/pull/213) Example for session handling in hooks (@netmilk)


### v0.6.0

- [#202](https://github.com/apiaryio/dredd/pull/202) Hooks logging, sending logs to apiary-reporter, transaction.startedAt (@kuba-kubula)

  **Breaking**: Removed support for `console` (e.g. `console.log`) in sandboxed hooks.

  **New**: Hooks logging via `hooks.log` function

  **New**: If using Apiary reporter and `hooks.log` in hooks, send the output of `hooks.log` to Apiary together with `transaction.startedAt` timestamp

- [#203](https://github.com/apiaryio/dredd/pull/203) **Fix**: Typo in variable name `newTransactionName` (@kuba-kubula)
- [#207](https://github.com/apiaryio/dredd/pull/207) **Docs**: Start writing [Changelog](CHANGELOG.md), with little help from `github-changes` npm package (@kuba-kubula)

### v0.5.5

- [#200](https://github.com/apiaryio/dredd/pull/200) **Fix**: Typo `bleuprint -> blueprint` in interactive config and elsewhere (@abtris)

### v0.5.4

- [#199](https://github.com/apiaryio/dredd/pull/199) **New**: Completed support for API Blueprint 1A8 (Dredd now supports arbitrary actions) (@netmilk)

### v0.5.3

- [#198](https://github.com/apiaryio/dredd/pull/198) **Fix**: Trying to fix build by adding delay to prevent race condition (@netmilk)
- [#197](https://github.com/apiaryio/dredd/pull/197) **Update**: Dependencies update (@netmilk)
- [#195](https://github.com/apiaryio/dredd/pull/195) **Fix**: Freeze proxyquire to 1.4.x, 1.5.x broke the build (@kuba-kubula)
- [#185](https://github.com/apiaryio/dredd/pull/185) **Docs**: Typos in README.md (@bootstraponline)

### v0.5.2

- [#184](https://github.com/apiaryio/dredd/pull/184) **Fix**: Dredd init fix (@netmilk)

### v0.5.1

- [#179](https://github.com/apiaryio/dredd/pull/179) **New/Fix**: Add __support for io.js, node.js 0.12 and MSON__ (@kuba-kubula)
- [#178](https://github.com/apiaryio/dredd/pull/178) **Update/Fix**: Use pitboss-ng npm instead of pitboss fork-git-url (@kuba-kubula)
- [#176](https://github.com/apiaryio/dredd/pull/176) **Docs**: Use Read the Docs (@netmilk, @smizell)

### v0.5.0

- [#167](https://github.com/apiaryio/dredd/pull/167) Loading and running hooks in isolated sandboxed context (@kuba-kubula, @netmilk)

  **Breaking**: Run hooks functions as a separate functions without access to environment around

  **New**: `--sandboxed` hooks do not share whole code, they are evaluated and executed in separate contexts

  **New**: Dredd JavaScript instance can be configured to use hooks provided from an object with strings (`configuration.hooksData`)

- [#174](https://github.com/apiaryio/dredd/pull/174) **Update**: Enhance apiary reported json (@kuba-kubula)
- [#165](https://github.com/apiaryio/dredd/pull/165) **Change**: One Hooks instance per one Dredd instance - avoid sharing of hooks object through all instances of Dredd class (@netmilk, @kuba-kubula)
- [#164](https://github.com/apiaryio/dredd/pull/164) **Docs**: Fix small typos in documentation (@kuba-kubula)

### v0.4.8

- [#161](https://github.com/apiaryio/dredd/pull/161) **Update**: Show line numbers in warnings from parser (@netmilk, @kuba-kubula)
- [#163](https://github.com/apiaryio/dredd/pull/163) **Docs**: Hooks documentation and examples (@netmilk, @kuba-kubula)

### v0.4.7

- [#160](https://github.com/apiaryio/dredd/pull/160) Hooks loosing context / reference to transaction (@kuba-kubula)

### v0.4.6

- [#159](https://github.com/apiaryio/dredd/pull/159) Release 0.4.6 (@kuba-kubula)
- [#154](https://github.com/apiaryio/dredd/pull/154) Passing custom parameters to Reporters via JS API, logic from bin script to CoffeeScript (@kuba-kubula)
- [#156](https://github.com/apiaryio/dredd/pull/156) Feature: Custom user assertions in hooks to fail a transaction (@netmilk)
- [#158](https://github.com/apiaryio/dredd/pull/158) Add tests to test prettify-response method (@kuba-kubula)
- [#157](https://github.com/apiaryio/dredd/pull/157) Various small fixes (@netmilk, @kuba-kubula)
- [#150](https://github.com/apiaryio/dredd/pull/150) Update dependencies to latest (@kuba-kubula)
- [#149](https://github.com/apiaryio/dredd/pull/149) Coffeelint Dredd source files (@kuba-kubula)
- [#148](https://github.com/apiaryio/dredd/pull/148) Adding CR to multipart requests based on multipart content-type header, ... (@netmilk)
- [#146](https://github.com/apiaryio/dredd/pull/146) Add a Gitter chat badge to README.md (@gitter-badger)
- [#147](https://github.com/apiaryio/dredd/pull/147) Add unit tests when path is a URL to blueprint file (@kuba-kubula)

### v0.4.5

- [#145](https://github.com/apiaryio/dredd/pull/145) Load blueprint-file from provided URL from http/https (@netmilk, @kuba-kubula)
- [#144](https://github.com/apiaryio/dredd/pull/144) Ability to use String with Blueprint data in JS API without using files on filesystem. (@kuba-kubula)


### v0.4.4

- [#142](https://github.com/apiaryio/dredd/pull/142) Bump version to 0.4.4 (@kuba-kubula)
- [#141](https://github.com/apiaryio/dredd/pull/141) Fix cli-test by freezing devDependency clone@0.x (@kuba-kubula)
- [#140](https://github.com/apiaryio/dredd/pull/140) Removed insecure `marked` dependency and updated all others (@netmilk)
- [#139](https://github.com/apiaryio/dredd/pull/139) Transaction runner fills all properties for test(step) (@kuba-kubula)

### v0.4.3

- [#138](https://github.com/apiaryio/dredd/pull/138) Gavel with support for JSON schema v4 (@netmilk)

### v0.4.1

- [#137](https://github.com/apiaryio/dredd/pull/137) Bump versions of some dependencies (@kuba-kubula)

### v0.4.0

- [#136](https://github.com/apiaryio/dredd/pull/136) Anonymous Apiary Reporter (@kuba-kubula, @netmilk)
- [#135](https://github.com/apiaryio/dredd/pull/135) Fix JS API backward compatibility (@netmilk)
- [#131](https://github.com/apiaryio/dredd/pull/131) Add oneline Hipchat notification from travisci (@abtris)
- [#128](https://github.com/apiaryio/dredd/pull/128) Merge pull request #128 from apiaryio/netmilk/fix-124, fixing #124 (@netmilk)
- [#125](https://github.com/apiaryio/dredd/pull/125) Multi blueprint processing (@netmilk)
- [#130](https://github.com/apiaryio/dredd/pull/130) Suppressing color output with --color false, closes #105 (@netmilk)
- [#120](https://github.com/apiaryio/dredd/pull/120) New copy-pasteable example (@netmilk)
- [#121](https://github.com/apiaryio/dredd/pull/121) Dry-run option added to CLI help. Fixing #119 (@netmilk)

### v0.3.14

- [#115](https://github.com/apiaryio/dredd/pull/115) Updated dependencies to latest, version bump (@netmilk)
- [#114](https://github.com/apiaryio/dredd/pull/114) Removed URI parameter string validation for number values, Fixing #111, Merging conflicting #113 (@netmilk)
- [#112](https://github.com/apiaryio/dredd/pull/112) Fixes #98 header parsing issue (@ecordell)
- [#110](https://github.com/apiaryio/dredd/pull/110) Fix for boolean example validation. (@jonathanbp)

### v0.3.13

- [#107](https://github.com/apiaryio/dredd/pull/107) Fixing #106 (@apiaryio)

### v0.3.12

- [#104](https://github.com/apiaryio/dredd/pull/104) Netmilk/new features (@netmilk)

### v0.3.11

- [#103](https://github.com/apiaryio/dredd/pull/103) Updated all deps to latest, fixed travis build for node 0.8.x - all badges back in green (@netmilk)

### v0.3.10

- [#102](https://github.com/apiaryio/dredd/pull/102) Adding beforeAll and afterAll (@CodeFred)
- [#95](https://github.com/apiaryio/dredd/pull/95) Reintroduces "silent" flag (@frio)
- [#92](https://github.com/apiaryio/dredd/pull/92) Added '-L' parameter to curl command (@eddieroger)
- [#2](https://github.com/apiaryio/dredd/pull/2) Adding documentation to README (@CodeFred)
- [#1](https://github.com/apiaryio/dredd/pull/1) Adding beforeAll and afterAll hooks, allowing setup and teardown common to all tests (@CodeFred)

### v0.3.9

- [#86](https://github.com/apiaryio/dredd/pull/86) Catches errors in hooks, allows skipping tests, fixes small bug (@ecordell)
- [#82](https://github.com/apiaryio/dredd/pull/82) Netmilk/documentation (@netmilk)

### v0.3.8

- [#81](https://github.com/apiaryio/dredd/pull/81) Protagonist 0.12.0, showing blueprint parsing warnings (@netmilk)
- [#80](https://github.com/apiaryio/dredd/pull/80) Updated LICENCE (@netmilk)

### v0.3.7

- [#76](https://github.com/apiaryio/dredd/pull/76) Update npm before build (@netmilk)

### v0.3.4

- [#72](https://github.com/apiaryio/dredd/pull/72) Updated nonconflicting libraries (@netmilk)
- [#71](https://github.com/apiaryio/dredd/pull/71) Updated protagonist to v0.11.0 (@netmilk)

### v0.3.3

- [#70](https://github.com/apiaryio/dredd/pull/70) Updated gavel and bumped version (@netmilk)

### v0.3.2

- [#69](https://github.com/apiaryio/dredd/pull/69) Netmilk/new rest reporter (@netmilk)
- [#68](https://github.com/apiaryio/dredd/pull/68) Apiary reporter (@netmilk)
- [#60](https://github.com/apiaryio/dredd/pull/60) Adds protocol information to individual transactions (@ecordell)

### v0.3.1

- [#59](https://github.com/apiaryio/dredd/pull/59) Better file handling for reporters (fixes #48 and #57) (@ecordell)

### v0.3.0

- [#56](https://github.com/apiaryio/dredd/pull/56) Update to protagonist v0.8.0 (@zdne)
- [#44](https://github.com/apiaryio/dredd/pull/44) Adds before/after hooks to Dredd (@ecordell)
- [#49](https://github.com/apiaryio/dredd/pull/49) Fix Dredd / Gavel.js interface. Closes #46 (@zdne)
- [#45](https://github.com/apiaryio/dredd/pull/45) Add support for path in API endpoint. Fixes #43 (@abtris)
- [#41](https://github.com/apiaryio/dredd/pull/41) Fixes sequencing bug in junit reporter (@ecordell)
- [#37](https://github.com/apiaryio/dredd/pull/37) Dredd exited without an interesting error message (@albertjan)
- [#36](https://github.com/apiaryio/dredd/pull/36) Fix sorting to use the order used in the apiary file as well. Close #32 and #36. (@ksarna)

### v0.2.1

- [#21](https://github.com/apiaryio/dredd/pull/21) Tests and fixes passing Dredd class pre-runtime errors to the CLI (@netmilk)
- [#19](https://github.com/apiaryio/dredd/pull/19) Content-Length header in reqeusts for Rails support (@netmilk, @theodorton)

### v0.1.6

- [#14](https://github.com/apiaryio/dredd/pull/14) Fixing exit status and adding CLI tests (@netmilk)

### v0.1.4

- [#8](https://github.com/apiaryio/dredd/pull/8) Added Vagrant virtual development environment (@netmilk)
- [#5](https://github.com/apiaryio/dredd/pull/5) HTTPS support, global header injection, improved reporter output (@ecordell)

### v0.1.1

- [#1](https://github.com/apiaryio/dredd/pull/1) V0.1 (@netmilk)
