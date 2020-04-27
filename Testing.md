This project uses [Jest](https://jestjs.io/) for unit and snapshot testing.

You can run all the tests by

```bash
npm test
```

All test cases can be found under the `test` folder.

## Watch and Rerun

If you are working on a feature using [TDD](https://technologyconversations.com/2013/12/20/test-driven-development-tdd-example-walkthrough/), you can run and watch a particular test by

```bash
npm test ./test/stdlib.math.test.ts -- --watch
```

## Snapshot Testing

We use Snapshot Testing for `examples` to make sure most of the code works as expected.

There are some articles about snapshot testing:

 - https://jest-bot.github.io/jest/docs/snapshot-testing.html
 - https://scotch.io/tutorials/writing-snapshot-tests-for-react-components-with-jest

**If you made some changes by purpose and it breaks the snapshot testing, you may need to update the snapshot by**

```bash
npm run test:update
```