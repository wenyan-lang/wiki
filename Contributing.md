Thanks for being interested in contributing to this project! Here are some steps and notes for you before you go.

## Ways to contribute
- [Share Your Wenyan Scripts](#share-your-wenyan-scripts)
- [Share Your Works Related to Wenyan](#share-your-works-related-to-wenyan)
- [Financial Contribute](#financial-contribute)
- [Contribute to Code](#contribute-to-code)
- [Contribute to Documentation](#contribute-to-documentation)
- [Contribute to Online IDE](#contribute-to-online-ide)
- [Contribute to Standard Library](contribute-to-standard-library)
- [Contribute to Testing](contribute-to-testing)

### Share Your Wenyan Scripts

To share your scripts, you can:

- Publish your code snippets on the [Snippets Site](https://wenyan-snippets.glitch.me/)
- Add [examples](https://github.com/wenyan-lang/wenyan/tree/master/examples) to the main repo
- Create and publish your own packages on [wyg](/guide/wyg)

### Share Your Works Related to Wenyan

Made a tool/work for wenyan? Cool!

Open an issue and share your work. We would love to add it to our wiki page!

### Financial Contribute

Become a financial contributor and help us sustain our community. [[Contribute](https://opencollective.com/wenyan-lang/contribute)]

### Contribute to Code

You can check out [Development Setup](#development-setup) and [Project Structure](#project-structure) to get familiar with the project.

Before you make changes to code, it's always better to open an issue first and get some discussion.

### Contribute to Documentation

Please go to the [wiki repo](https://github.com/wenyan-lang/wiki), you can found the instructions there.

### Contribute to Online IDE

The code of Online IDE is under the `static` folder. Check out [Project Structure](#project-structure) for more details.

### Contribute to Standard Library

> WIP

### Contribute to Testing

Check out the [Testing Section](https://github.com/wenyan-lang/wenyan/wiki/Testing).

## Development Setup

You will need [Node.js](https://nodejs.org/) version 10+

After cloning the repo, run:

```bash
# install all the dependencies
npm i
```

### Commonly used NPM scripts
```bash
# watch and auto re-build code into dist
$ npm run dev

# watch and auto re-build code for online ide
$ npm run dev:site

# directly run and test cli without building
$ npm run cli

# build all dist files, including npm packages
$ npm run build

# run the full test suite, including linting/type checking
$ npm test
```

There are some other scripts available in the scripts section of the `package.json` file.

**Please make sure to have this pass successfully before submitting a PR**. Although the same tests will be run against your PR on the CI server, it is better to have it working locally.

## Project Structure

- **`tools`**: contains build-related scripts and configuration files. Usually, you don't need to touch them.

- **`dist`**: contains built files for distribution.

- **`typings`**: contains type declarations for [Typescript](https://www.typescriptlang.org/). These declarations are generated alongside with building. Usually, you don't need to worry about them either.

- **`test`**: contains all tests. The unit tests are written with [Jest](https://jestjs.io/). Refer to [this Section](https://github.com/wenyan-lang/wenyan/wiki/Testing) for more details.

- **`static`**: contains files of the Online IDE and website.

- **`examples`**: contains examples contributed by the community. They will also be bundled into the Online IDE.

- **`site`**: the legacy website files. Using to redirect to the new one.

- **`lib`**: contains the Standard Libraries. The subfolders are for language-specified codes.

- **`documentation`**: the legacy documentation files. Please use wiki now.

- **`src`**: contains the source code. The codebase is written in [Typescript](https://www.typescriptlang.org/) with ES2015 syntax.

  - **`transpilers`**: contains code for the transpiling to different target languages.

  - **`parser.ts`**: contains code for the compiler core.

  - **`runtime.ts`**: contains code for [[Browser Runtime]].

  - **`cli.ts`**: contains code for [Command Line Interface](https://www.npmjs.com/package/@wenyanlang/cli).


## Code Style

Don't worry about the code style as long as you install the dev dependencies. Git hooks will format and fix them for you on committing.

## Code of Conduct
Our [Code of Conduct](https://github.com/wenyan-lang/wenyan/blob/master/CODE_OF_CONDUCT.md) is a guide to make it easier to enrich all of us and the technical communities in which we participate.

## Contributors

### Code Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
<a href="https://github.com/wenyan-lang/wenyan/graphs/contributors"><img src="https://opencollective.com/wenyan-lang/contributors.svg?width=890&button=false" /></a>

### Financial Contributors

Become a financial contributor and help us sustain our community. [[Contribute](https://opencollective.com/wenyan-lang/contribute)]

#### Individuals

<a href="https://opencollective.com/wenyan-lang"><img src="https://opencollective.com/wenyan-lang/individuals.svg?width=890"></a>

#### Organizations

Support this project with your organization. Your logo will show up here with a link to your website. [[Contribute](https://opencollective.com/wenyan-lang/contribute)]

<a href="https://opencollective.com/wenyan-lang/organization/0/website"><img src="https://opencollective.com/wenyan-lang/organization/0/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/1/website"><img src="https://opencollective.com/wenyan-lang/organization/1/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/2/website"><img src="https://opencollective.com/wenyan-lang/organization/2/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/3/website"><img src="https://opencollective.com/wenyan-lang/organization/3/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/4/website"><img src="https://opencollective.com/wenyan-lang/organization/4/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/5/website"><img src="https://opencollective.com/wenyan-lang/organization/5/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/6/website"><img src="https://opencollective.com/wenyan-lang/organization/6/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/7/website"><img src="https://opencollective.com/wenyan-lang/organization/7/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/8/website"><img src="https://opencollective.com/wenyan-lang/organization/8/avatar.svg"></a>
<a href="https://opencollective.com/wenyan-lang/organization/9/website"><img src="https://opencollective.com/wenyan-lang/organization/9/avatar.svg"></a>