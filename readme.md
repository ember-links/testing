#Resources for Writing Tests in Ember.JS

##Screencasts
- [An Introduction to Ember.js](https://skillsmatter.com/skillscasts/6362-an-introduction-to-ember-js)
    - 12th May 2015 • Beginner • [Jamie White][jgwhite]
    - setting up testing on new Ember CLI project
    - using [Phantom JS][PhantomJS]
    - mocking services and using [Firebase][Emberfire] with [MockFirebase][MockFirebase]

##Slideshows
- [Testing Ember Apps: Managing Dependency](http://www.slideshare.net/mixonic/testing-ember-apps-managing-dependency)
    - 29th August 2015 • Advanced • [Mixonic][mixonic]
    - isolating implementation & normalize behaviour
    - extract as service and use promise for consistent sync/async behaviour
    - has [an accompanying blogpost with more details](http://madhatted.com/2014/8/29/testing-ember-js-apps-managing-dependencies)
- [slideshow (not too detailed)](http://www.slideshare.net/bantic/ember-testing-internals-with-ember-cli)
    - [Cory Forsyth][Bantic]

##Blog Posts
- [Ember QUnit 0.2.x](http://reefpoints.dockyard.com/2015/02/06/ember-qunit-0-2.html)
    - 6th February 2015 • Beginner • [Robert Jackson][rwjblue]
    - simple examples
    - this.append() is now this.subject()
    - setup/teardown is now beforeEach/afterEach
- [Acceptance testing in Ember-CLI, an introduction.](http://mariogintili.svbtle.com/acceptance-testing-ember-cli)
    - 2nd May 2015 • Beginner • [Mario Gintili][MarioGintili]
    - basic acceptance test use case run through
    - stubbing requests with [Pretender][Pretender] & [Ember-CLI-Mirage][ember-cli-mirage]
- [Improving Ember-CLI Testing with Sinon.js](http://spin.atomicobject.com/2015/05/18/sinon-js-ember-cli-testing/)
    - 18th May 2015 • Intermediate • John Fisher @ [Atomic Object][AtomicObject]
    - how to use [Sinon][Sinon] library with [Ember-sinon][Ember-sinon]
    - example demonstrating stubbing and checking actions
- [Demystifying Asncy testing](http://coryforsyth.com/2014/07/10/demystifing-ember-async-testing/)
    - [Cory Forsyth][Bantic]
- [Mocking Ember Services for Unit Testing](http://blog.stevenedouard.com/mocking-ember-services-for-unit-testing/)
    - 17th April 2015 • Intermediate • [Steven Edouard][stevenedouard]
    - mocking Azure storage
    - custom adapters
    - unit testing mocked services
- [Ember component integration tests](http://alisdair.mcdiarmid.org/2015/06/20/ember-component-integration-tests.html)
	- 20th June 2015 • Intermediate • 

http://alisdair.mcdiarmid.org/2015/06/20/ember-component-integration-tests.html
http://matteodepalo.github.io/blog/2014/01/03/ember-integration-testing-with-konacha/
http://emberup.co/integration-tests-for-components/



##Forum Posts
- [Proper way to handler timers w/ Ember Testing](http://discuss.emberjs.com/t/proper-way-to-handler-timers-w-ember-testing/4693)
    - some options for Ember.run.later issue but no real conclusion
    - [proposed solution on Stack Overflow](http://stackoverflow.com/questions/27851517/ember-integration-testing-hangs-after-visiting-route#answer-27887807) by [Teddy Zeenny][teddyzeenny]
- [Manually overriding the testing run loop to wait for something](http://stackoverflow.com/questions/25512168/async-call-in-ember-testing#answer-25513886)
    - a very basic way of pausing the test for a fixed time to allow for a non-promise event to occur
- [Registering Asnyc Helpers](http://stackoverflow.com/questions/26498845/using-ember-cli-how-do-i-get-an-acceptance-test-to-wait-for-a-promise#answer-27085279)
    -  create an Async Helper to wait for a specified promise to resolve [Luke Melia][LukeMelia]

##Libraries
- [ember-cli-htmlbars-inline-precompile](https://github.com/pangratz/ember-cli-htmlbars-inline-precompile)
    - by [Clemens Müller][pangratz]
    - precompile inline HTMLBars templates via ES6 tagged template strings
    - addon to help make component integration tests readable see
        - [Stefan Penner's precompile suggestions](https://gist.github.com/stefanpenner/38a36298d04b29bbce5f)
        - [Support component integration tests](https://github.com/switchfly/ember-test-helpers/pull/38)
        - [Robert Jackson's Example Gist](https://gist.github.com/rwjblue/a178377293380ed537ce)
- [ember-qunit](https://github.com/rwjblue/ember-qunit)
    - by [Robert Jackson][rwjblue]
    - unit test helpers for Ember
- [ember-simple-auth-testing](https://github.com/simplabs/ember-simple-auth/tree/master/packages/ember-simple-auth-testing)
    - by [marcoow][marcoow]
    - 3 test helpers for authenticating / setting the current session / invalidating when using Ember Simple Auth

##Forthcoming Features

> Keep an eye on these for newer techniques when wrtiting tests

###Using new wait format for async testing
- [Using the new asnyc wait format](https://github.com/switchfly/ember-test-helpers/issues/50) as per
    - https://github.com/ember-cli/ember-cli/issues/3529

##Github repos with good testing examples
- [LG Front-End](https://github.com/201-created/LG)
    - general patterns & using registerAsyncHelpers
    - stubbing requests using [Pretender][Pretender]
        - https://github.com/201-created/LG/blob/master/tests/helpers/fake-server.js
        - https://github.com/201-created/LG/blob/master/tests/helpers/fake-requests.js
    - stubbing authentication with [torii][torii]
        - https://github.com/201-created/LG/blob/master/tests/helpers/sign-in.js
- [Ember Jobs](https://github.com/stefanpenner/ember-jobs)
    - stubbing resolver
        - https://github.com/stefanpenner/ember-jobs/blob/master/tests/helpers/container.js
        - https://github.com/stefanpenner/ember-jobs/blob/master/tests/acceptance/admin-test.js
    - simple stubbing of requests using [Pretender][Pretender]
        - https://github.com/stefanpenner/ember-jobs/blob/master/tests/acceptance/searching-test.js
- [Ember Inspector](https://github.com/emberjs/ember-inspector)
    - container lookups
        - https://github.com/emberjs/ember-inspector/blob/master/tests/integration/view_tree_test.js
- [Ember Crumbly](https://github.com/poteto/ember-crumbly)
    - acceptance testing formatting
        - https://github.com/poteto/ember-crumbly/blob/develop/tests/acceptance/integration-test.js
- [Ember Front End Blog](https://github.com/Robdel12/front-end-blog)
    - acceptance testing with [Pretender][Pretender]
        - https://github.com/Robdel12/front-end-blog/blob/master/tests/acceptance/adding-post-test.js
- [Liquid Fire](https://github.com/ef4/liquid-fire)
    - working with view registry (last resort, better to test visible interfaces)
        - https://github.com/ef4/liquid-fire/blob/fa2a79964763a5290c32f09ed209f443259a3139/tests/integration/helpers/liquid-spacer-test.js#L18-L40


https://github.com/alphasights/ember-calendar/blob/develop/tests/unit/components/as-calendar-test.js

Updating to new component integration tests from unit
https://github.com/rwjblue/dashboard.aptible.com/commit/43995b61ff9ceea3b937ebd69de03637584f25e4?diff=split



[MarioGintili]: https://twitter.com/mariogintili
[teddyzeenny]: https://twitter.com/teddyzeenny
[AtomicObject]: https://twitter.com/atomicobject
[mixonic]: https://twitter.com/mixonic
[rwjblue]: https://twitter.com/rwjblue
[LukeMelia]: https://twitter.com/lukemelia
[Bantic]: https://twitter.com/bantic
[jgwhite]: https://twitter.com/jgwhite
[stevenedouard]: http://blog.stevenedouard.com/
[pangratz]: https://twitter.com/pangratz
[marcoow]: https://twitter.com/marcoow

[ember-cli-mirage]: http://www.ember-cli-mirage.com/
[Pretender]: https://github.com/trek/pretender
[torii]: http://vestorly.github.io/torii/
[Sinon]: http://sinonjs.org/
[Ember-sinon]: https://github.com/csantero/ember-sinon
[Emberfire]: https://github.com/firebase/emberfire
[MockFirebase]: https://github.com/katowulf/mockfirebase
[PhantomJS]: phantomjs.org