# WorkLogs

6/29/2019

- [BUGFIX] reply can't be received due to defect logic in unsub rule, fixed, PR made, in staging, code review

6/30/2019

- [CW-2675] research about the options to compress the payload, lzw, lz4, smaz, one time padding(XOR)

7/1/2019

- [Code][CW-3283] initiate the event search on SparkPost
  - routes and function
  - exponential backoff
  - miscellaneous
  - create index on db for status column
- [Code] POC for email compression using one time padding algo
- [Code review and fix][CW-2674] event webhook PR
- [Code review and fix][CW-2605] unsubscribe PR

7/2/2019

- [Code][CW-2674][CW-2383] event search, in progress.
- [Code][CW-2675] compress proxy email address, xxx from xxx team has shared some code snippets in C# with me, but I need to confirm with him about the engineering details, mean while, I am working on recreating the code snippets in JS/TS
- [Follow up][CW-2674][CW-2383] webhook PR merged, deployed, in staging, ready for test

7/3/2019

- [Code][CW-2674][CW-2383] event search, in progress.
- [Code][CW-2675] compress proxy email address, TS version done, basic working prototype done, optimizing now.
- [Follow up][CW-2674][CW-2383] webhook updated test instructions on spam_complaint event
- [Code Review] xxx's PR about refactor, feedback given
