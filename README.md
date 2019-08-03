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


7/12/2019
- [Bugfix][In Progress] CW-3311
- [Code Review] 3080
- [Code][In Progress] add tests for services
- [Code][Code Review] add testcases for models
- [Code][Code Review] add test coverage tool

7/15/2019
- [Bugfix][Code Review] DecryptionService has a bug which blockes the whole workflow, fixed
- [Bugfix][In Progress] CW-3311
- [Code][In Progress] add tests for services
- [Code][Code Review] add testcases for models
- [Code][Code Review] add test coverage tool


7/16/2019
- [Bugfix][Code Review] DecryptionService has a bug which blockes the whole workflow, fixed
  - related Bugs [Code Review] CW-2257 CW-3358
- [Bugfix][In Progress] CW-3311
- [Code][In Progress] add tests for services
- [Code][Code Review] add testcases for models
- [Code][Code Review] add test coverage tool

7/17/2019
- [Bugfix][Code review] CW-3311
- redis high concurrency problem
  - 1. use atomic operations with buffer (done)
  - 2. use redis-lock [in progress]
  - 3. compare performance, load testing
- part of the rules engine code is lost in the refactor stage because of force push, revised, pr made

7/18/2019
- [Bugfix][Code review] CW-3311
- [Code review] redis high concurrency problem
  - 1. use atomic operations with buffer [done]
  - 2. use redis-lock [done]
  - 3. compare performance, load testing [done]
- [Code review]part of the rules engine code is lost in the refactor stage because of force push, revised, pr made
- [Miscellenous]attend cab meeting for GCM-6091


7/19/2019
- [Bugfix][Code review] CW-3311
- [Code review] redis high concurrency problem
- [Code review]part of the rules engine code is lost in the refactor stage because of force push, revised, pr made
- [Miscellenous] configuration work for staging env
    -  [done]replace `xxxxx` with `xxxxxx` for receiving and sending emails
    -  [done] new-relic alert slack integration setup for channel  #oppsstagingalerts
      - error rate high
      - apdex low
      - request take too long
    - [In progress] bounce domain setup

7/22/2019
- [Code Review] mysql query results cache in redis
- [Miscellenous] configure new-relic apdex benchmark index to be 0.8. the original one was 0.1
- [Documentation][In Progress] api documentation
- [Testcases][In Progress] services tests
- [Bug] investigate potential node vm memory leak

7/23/2019
- [Bug] investigate potential node vm memory leak, aws related
  - [ ] add pm2 to restart at memory usage at 600mb
  - [ ] investigate the root cause
- [In Progress] integrate the send message functionality into the new UI

7/24/2019
- [Bug] investigate potential node vm memory leak, aws related
  - [x] add pm2 to restart at memory usage at 600mb, will monitor performance over the time 
  - [ ] investigate the root cause
- [In Progress] integrate the send message functionality into the new UI, share observations and questions

7/25/2019
- setup the local dev env for cbdash-ui and services. spinned up 90% functionalities
- investigate the root cause for opps vm mem leak

7/26/2019
- [CW-3383] hook up message modal on the cbdash ui, compoennts added,working on the styles
- confirm the pm2 restart mechanism works, PR merged

7/27/2019
- investigate the root cause for the offplatform node vm mem leak bug
  - [ ] poc, isolate the memssage poller package out and monitor the memory usage

7/29/2019
- CW-3383 integrate the old send message modal to new TDP HP
  - [x] solve conflicts with differnet angular versions and dependency problems with submodules
- work with QA team on the tests, shared the postman collection of opps
- work with Rui on the nodejs vm leak bug, located the root cause, working on a solution

7/30/2019
- CW-3383 give up on integrating the old send message modal, switch to new modal, working with HP to get the sending functionality done, provided the mc api postman collection
- working on the opps nodejs vm mem leak bug

7/31/2019
- CW-3383 working with Malar on the template api
- investigate the root cause of yesterday incident

8/1/2019
- CW-3383 provide tests material to Malar
- design and brain storm with team for strategies for fixing the firebase outage incident, proposed two layer new relic alerts

8/2/2019
- working on the testcases for opps 50% , covered all services

8/3/2019
- working on the testcases for opps 50%^, covering controllers  
