# Case Study of Heroku

This document if for the case study/research of how we may use Heroku for Continuous Integration in each of the testing environments.

## Types of Testing Environments

-Development Environment

-QA Environment

-Staging/Pilot Environment

-Production Environment

### Using Heroku for CI

First, what is continuous integration? During the dev process of a game, developers must test their work regularly to catch any bugs in their new features, functions, updates, etc. While the idea sounds greats, in reality, if done manually and directly to the main branch, these tests may stall work for an extended period of time. Continuous Integration is having the build and testing of new bits of code from developers done completely automated, multiple times a day, and on a machine dedicated to doing this process. This is crucial to the development lifecycle in a game because is saves countless hours that could be used to further the quality of the game being creating.

Heroku allows developers in the Dev Environment to divide or branch work being done to separate new code from the master branch of code. This prevents and conflict between code(s) being tested by only permitting *working* code in the master branch. If the code doesn't work when you try to test it with the master branch, which should theoretically be working, then its an issue in your new code. Once the build has passed, unit testing is a breeze and it will be added to the next build automatically.

In the QA Environment, Heroku may be useful with continuous integration as the build and testing can be automated. Smoke/Regression tests that come back right away with no new issues can be committed straight to the build automtically if they pass. If they do not pass, Heroku will notify you and you may revert back to the previopusly working product.

The Staging/Pilot Environment is only for working code that has been through QA and is ready for user validation and training. Heroku has the ability to separate each of the Testing environments, so staging/pre-production is simple. The main branch is always deployable, so staging can always be done on the main branch. Heroku gives you a unique url if needed to test the functionality of the game or software, and offers review apps for multiple developer insight and decision making.

Once in the Production Environment, developers may test the software with real data. The product is ready to go by this time and Heroku can publish your work for you. Concluding, any and all changes by you or your team are tracked and displayed, there is complete clearity and confidence in the creation of a large project knowing that everything is accounted for and everyone is in the loop on these changes.
