## Repro

```
yarn
yarn build
yarn test
```

You will get something like:

```
Counter
    count up
      1) "before each" hook for "should count up"


  0 passing (9ms)
  1 failing

  1) Counter
       "before each" hook for "should count up":
     Error: HERE
      at ...typescript-solidity-dev-starter-kit/test/counter.ts:54:31
      at step (test/counter.ts:33:23)
      at Object.next (test/counter.ts:14:53)
      at ...typescript-solidity-dev-starter-kit/test/counter.ts:8:71
      at new Promise (<anonymous>)
      at __awaiter (test/counter.ts:4:12)
      at Context.<anonymous> (test/counter.ts:50:37)
      at processImmediate (internal/timers.js:456:21)
      at process.topLevelDomainCallback (domain.js:137:15)
```

The real line should be `14`.
