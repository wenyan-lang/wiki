Thanks for being interested in contributing to this project! Here are some steps and notes for you before you go.


## Ways to contribute
- [Publish Your Wenyan Scripts](#share-your-wenyan-scripts)
- [Share Your Works Related to Wenyan](#share-your-works-related-to-wenyan)
- [Contribute to Code](#contribute-to-code)
- [Contribute to Documentation](#contribute-to-documentation)
- [Contribute to Online IDE](#contribute-to-online-ide)
- [Contribute to Standard Library](contribute-to-standard-library)
- [Contribute to Testing](contribute-to-testing)

### Share Your Wenyan Scripts

To share your scripts, you can:

- Share your code snippets on the [Snippets Site](https://wenyan-snippets.glitch.me/)
- Add [examples](https://github.com/wenyan-lang/wenyan/tree/master/examples) to the main repo
- Create and publish your own packages on [wyg](/guide/wyg)

### Share Your Works Related to Wenyan

> WIP

### Contribute to Code

> WIP

### Contribute to Documentation

> WIP

### Contribute to Online IDE

> WIP

### Contribute to Standard Library

> WIP

### Contribute to Testing

Check out the [Testing Section](/contribute/test).

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

## Code Style

Don't worry about the code style as long as you install the dev dependencies. Git hooks will format and fix them for you on committing.

## Code of Conduct
Our [Code of Conduct](https://github.com/wenyan-lang/wenyan/blob/master/CODE_OF_CONDUCT.md) is a guide to make it easier to enrich all of us and the technical communities in which we participate.