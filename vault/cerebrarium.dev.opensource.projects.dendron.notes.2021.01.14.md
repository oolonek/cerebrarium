---
id: 77d6a034-60cb-4894-bd0d-5e41c2a75797
title: '14'
desc: ''
updated: 1610668964946
created: 1610579065274
---

# Notes on pairing session

## Session goal
- Add a test for MarkdownPublishPod
- Show how tests are set up for Dendron

## watch

```bash
cd bootstrap/scripts
./watch.sh
```
- Dendron is made up of a multiple typescript projects
- This script will watch all of them and compile them when you make change to the code.

---

## Testing in Dendron

- All tests are managed with jest.
    - Except the plugin itself, which uses mocha
        - mocha is very well integrated into VSCode's [test harness](https://en.wikipedia.org/wiki/Test_harness)
- Any test code that are not testing plugin functionality are
    - located in the `__tests__` directory
    - in the file name formatted `TestName.spec.ts`
- To run a test, use VSCode tasks
    - `cmd` + `shift` + `p`, -> `Task: Run Task` in the command palette
    - Select the appropriate task to run.
        - These are vscode wrappers around bash scripts.
    - In our case, we want to test `MarkdownPod.spec.ts`
    - Type `npm:test:watch` in the task comman palette
    - There will be a number of selections, marked with which project's test it will be running.
        - Select the one marked with `pods-core`, as we are testing pods today.
    - This will open a terminal and run `jest --watch` on the specific test we are interested in.
        - Now jest will run all the tests for you every time you change your test code
- Writing new tests
    - Start a new [describe block](https://jestjs.io/docs/en/api#describename-fn), and give it an appropriate name.
    - Write a new test case.
        - 
