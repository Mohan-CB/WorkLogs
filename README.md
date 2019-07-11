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

7/4/2019

- [Code][CW-2674][CW-2383][Code Review] event search, exponential backoff strategy done
- [Code][CW-2674][CW-2382][In Progress] event webhook processing, rejected by QA since spam_complaint event needs more dependency from siteops on the bounce domain
- [Code][CW-2675][In Progress] compress proxy email address, TS version done, however, found an error with the implementation about the special character support in the original payload, the algorithm design is fragil since the algorithm relies on the special character '_\' as the delimiter, need to talk to XXX about it and fix.

7/5/2019

- [Code Refactor][Code Review] working with XXX on logging service and related. PR made
- [Code][CW-2674][CW-2383][Code Review] event search, exponential backoff strategy done, fix conflicts with new Logging service.

7/6/2019

- [Code][In Progress] add test coverage tool
- [Code][CW-2674][CW-2383][Code Review][Code Refactor] event search, exponential backoff strategy done, fix conflicts with new Logging service.
- [Test] new logging service and related. PR made

7/8/2019

- [Code][In Progress] add test coverage tool
- [Code][CW-2674][CW-2383][Code Review][Code Refactor] event search, exponential backoff strategy done, fix conflicts with new Logging service.
- [Code][CW-3267]rules service, undeliverable rule

7/9/2019

- [Code][In Progress] add test coverage tool
- [Code][CW-2674][CW-2383][Merged][QA Test] event search, exponential backoff strategy done, fix conflicts with new Logging service.
- [Setup][CW-2383]setup CloudWatch to trigger the route daily
  - CloudWatch definition
  - Lambda / ECS task definition 
- [Code][CW-3267][Code Review]rules service, undeliverable rule
- [Code][Code Review][Refactor] insertOptFooter PR, fix subanchoIndex logic


7/10/2019

- [Code][Code Review] add test coverage tool
- [Setup][CW-2383]setup CloudWatch to trigger the route daily
  - CloudWatch definition
  - Lambda / ECS task definition
- [Code][In Progress]add testcases for models
- [Demo] record demos for CW-2674 event webhook feature and CW-2605 unsubscribe feature

7/11/2019

- [Code][Code Review] add testcases for models
- [Bugfix][In Progress] CW-3311 
- [Setup][CW-2383]setup CloudWatch in staging to trigger the route daily
  - CloudWatch definition
  - Lambda / ECS task definition
- [Code][Code Review] add test coverage tool
- [Code][Code Review Feedback] compress email length 
