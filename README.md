# Minimum Example of Eggjs, TypeScript, Jest

## How to reproduce error


```bash
npm install
npm run jest
```



```
> egg-ts-jest@1.0.0 jest
> EGG_TYPESCRIPT=true jest

Debugger listening on ws://127.0.0.1:42401/0c1a1397-de71-4c34-8800-573895206328
For help, see: https://nodejs.org/en/docs/inspector
Debugger attached.
2022-02-16 22:26:30,674 ERROR 1308535 nodejs.TypeError: Cannot use 'in' operator to search for 'enable' in 105
    at AgentWorkerLoader.normalizePluginConfig (~/workspace/egg-ts-jest/node_modules/egg-core/lib/loader/mixin/plugin.js:207:20)
    at AgentWorkerLoader.readPluginConfigs (~/workspace/egg-ts-jest/node_modules/egg-core/lib/loader/mixin/plugin.js:182:14)
    at AgentWorkerLoader.loadPlugin (~/workspace/egg-ts-jest/node_modules/egg-core/lib/loader/mixin/plugin.js:62:29)
    at AgentWorkerLoader.loadConfig (~/workspace/egg-ts-jest/node_modules/egg/lib/loader/agent_worker_loader.js:15:10)
    at new EggApplication (~/workspace/egg-ts-jest/node_modules/egg/lib/egg.js:55:17)
    at new Agent (~/workspace/egg-ts-jest/node_modules/egg/lib/agent.js:22:5)
    at MockApplication.[init] (~/workspace/egg-ts-jest/node_modules/egg-mock/lib/app.js:84:33)
    at Object.<anonymous>.next (<anonymous>)
    at onFulfilled (~/workspace/egg-ts-jest/node_modules/co/index.js:65:19)
    at processTicksAndRejections (node:internal/process/task_queues:94:5)

pid: 1308535
hostname: bj-dl-048.autox.sz

 FAIL  test/app/controller/home.test.ts
  ● test/app/controller/home.test.ts › should GET /

    TypeError: Cannot use 'in' operator to search for 'enable' in 105

      at AgentWorkerLoader.normalizePluginConfig (node_modules/egg-core/lib/loader/mixin/plugin.js:207:20)
          at Object.<anonymous>.next (<anonymous>)

  ● test/app/controller/home.test.ts › should GET /

    can't get backgroundTasksFinished before ready

      at Object.get (node_modules/egg-mock/lib/app.js:197:36)

2022-02-16 22:26:30,750 ERROR 1308528 nodejs.TypeError: Cannot use 'in' operator to search for 'enable' in 105
    at AgentWorkerLoader.normalizePluginConfig (~/workspace/egg-ts-jest/node_modules/egg-core/lib/loader/mixin/plugin.js:207:20)
    at AgentWorkerLoader.readPluginConfigs (~/workspace/egg-ts-jest/node_modules/egg-core/lib/loader/mixin/plugin.js:182:14)
    at AgentWorkerLoader.loadPlugin (~/workspace/egg-ts-jest/node_modules/egg-core/lib/loader/mixin/plugin.js:62:29)
    at AgentWorkerLoader.loadConfig (~/workspace/egg-ts-jest/node_modules/egg/lib/loader/agent_worker_loader.js:15:10)
    at new EggApplication (~/workspace/egg-ts-jest/node_modules/egg/lib/egg.js:55:17)
    at new Agent (~/workspace/egg-ts-jest/node_modules/egg/lib/agent.js:22:5)
    at MockApplication.[init] (~/workspace/egg-ts-jest/node_modules/egg-mock/lib/app.js:84:33)
    at Object.<anonymous>.next (<anonymous>)
    at onFulfilled (~/workspace/egg-ts-jest/node_modules/co/index.js:65:19)
    at processTicksAndRejections (node:internal/process/task_queues:94:5)

pid: 1308528
hostname: bj-dl-048.autox.sz

 FAIL  test/app/service/Test.test.ts
  ● test/app/service/Test.test.js › sayHi

    TypeError: Cannot use 'in' operator to search for 'enable' in 105

      at AgentWorkerLoader.normalizePluginConfig (node_modules/egg-core/lib/loader/mixin/plugin.js:207:20)
          at Object.<anonymous>.next (<anonymous>)

  ● test/app/service/Test.test.js › sayHi

    can't get mockContext before ready

       7 |
       8 |   beforeAll(async () => {
    >  9 |     ctx = app.mockContext();
         |               ^
      10 |   });
      11 |
      12 |   it('sayHi', async () => {

      at Object.get (node_modules/egg-mock/lib/app.js:197:36)
      at test/app/service/Test.test.ts:9:15

  ● test/app/service/Test.test.js › sayHi

    can't get backgroundTasksFinished before ready

      at Object.get (node_modules/egg-mock/lib/app.js:197:36)

Test Suites: 2 failed, 2 total
Tests:       2 failed, 2 total
Snapshots:   0 total
Time:        2.168 s
Ran all test suites.
```

