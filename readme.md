```

> jest-repro@1.0.0 test
> jest

 FAIL  src/test.ts
  ● Test suite failed to run

    TypeError: Cannot read properties of undefined (reading 'bind')

      at Runtime._createJestObjectFor (node_modules/jest-runtime/build/index.js:2193:46)
```

Adding a direct dependency on jest-environment-node "fixes" the issue.

The dependency in `@types/jest-environment-puppeteer` on `jest-environment-node` should be fixed.

`npm i -D jest-environment-node`
