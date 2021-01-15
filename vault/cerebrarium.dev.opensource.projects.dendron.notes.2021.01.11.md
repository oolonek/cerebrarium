---
id: 4b6788bb-f6c2-4d5f-abdb-8b597ea69e41
title: '11'
desc: ''
updated: 1610706925648
created: 1610661289528
---

- Scheduled a pairing sessions on 2021-01-13 7:30AM. 

[Writing Tests](https://dendron.so/notes/c84aa95c-83b9-4d52-90a1-eeec8f0ca84f.html)
- consider both single vault and multi-vault scenario.
    - `runLegacySingleWorkspaceTest`
    - `runLegacyMultiWorkspaceTest`
    - These set up mocks for single/multi vault testing.
        - example : [RenameNoteV2.test.ts](https://github.com/dendronhq/dendron/blob/master/packages/plugin-core/src/test/suite-integ/RenameNoteV2.test.ts#L131:L131)
    - [arguments](https://github.com/dendronhq/dendron/blob/master/packages/plugin-core/src/test/testUtilsV3.ts#L70:L70)
        - `ctx`
            - [vscode extension context](https://code.visualstudio.com/api/references/vscode-api#ExtensionContext)
            - collection of utilities private to an extension
        - `preSetupHook`
            - runs before init
        - `postSetupHook`
            - runs after init
        - `preActivateHook`
            - runs befor workspace activation
        - `postActivateHook`
            -
- [runJestHarnessV2](https://github.com/dendronhq/dendron/blob/58b3587f1e44f54635f77f7395f7b756f18e0c84/packages/common-test-utils/src/utils.ts#L119)
    - use shimmed jest methods to assert equality of actual and expected test outcome.

- engine test setup
    1. initialize engine
    2. seed it with fixtures for testing
    - may require testing in multiple environments (plugin, CLI, server, engine)
    - may require multiple test runners (jest / mocha)
