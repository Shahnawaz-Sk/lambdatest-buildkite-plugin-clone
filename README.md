# LambdaTest Buildkite Plugin

A [Buildkite plugin](https://buildkite.com/docs/agent/v3/plugins) that opens a [LambdaTest tunnel](https://www.lambdatest.com/support/docs/testing-locally-hosted-pages/).

It contains a [pre-command hook](hooks/pre-command), [pre-exit hook](hooks/pre-exit), and [tests](tests/command.bats) using [plugin-tester](https://github.com/buildkite-plugins/plugin-tester).

## Configuration

### `tunnelName` (optional)

The tunnel name to use, by default it will use the Buildkite Job ID (`BUILDKITE_JOB_ID`)

```yml
steps:
  - command: 'yarn && yarn LT test'
    plugins:
      - lambdatest/lambdatest:
          tunnelName: "custom-tunnel-id"
```
## Tests
To run the tests, run `.ci/test.sh`

## Lint

* Plugin: `.ci/lint-plugin.sh`
* Shell files `.ci/lint-shell.sh`
