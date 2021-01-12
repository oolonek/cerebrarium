---
id: 739ad898-dfbf-403f-8cc6-073cfcca103e
title: Dendron
desc: ''
updated: 1610408341783
created: 1609631769094
---

# Dendron

[Website](dendron.so)


## Useful links
[Your First Extension](https://code.visualstudio.com/api/get-started/your-first-extension)

## Notes
**2021-01-06 8:04 AM**
- Grabbed my first issue a few days ago.
- Seems I need a bit of ts/js + VSCode extension development primer so I've been on that for the last few days
- First going through [the typescript handbook](https://www.typescriptlang.org/docs/handbook/) to get myself familiar with typescript.
- [Kevin](https://www.kevinslin.com/) has kindly offered help to get me started with contributing. The community is very welcoming to newcomers.

**2021-01-11 11:17 PM**

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
