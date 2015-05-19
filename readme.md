Registering Asnyc Helpers

Luke Melias answer here : http://stackoverflow.com/questions/26498845/using-ember-cli-how-do-i-get-an-acceptance-test-to-wait-for-a-promise

Overview

@bantic's [slideshow (not too detailed)](http://www.slideshare.net/bantic/ember-testing-internals-with-ember-cli)


@jqwhite's long screencast (includes setting up testing and stubbing a method using firebase...)
https://skillsmatter.com/skillscasts/6362-an-introduction-to-ember-js

To Keep an eye on progress

https://github.com/switchfly/ember-test-helpers/issues/50
- Using the new asnyc wait format... as per
https://github.com/ember-cli/ember-cli/issues/3529

##Blog Posts
- [Robert Jackson on QUnit 2.0 with new format (by bye setup/teardown hello beforeEach/afterEach)](http://reefpoints.dockyard.com/2015/02/06/ember-qunit-0-2.html)
- [Bantic - Demystifying Asncy testing](http://coryforsyth.com/2014/07/10/demystifing-ember-async-testing/)
- [Acceptance testing in Ember-CLI, an introduction.](http://mariogintili.svbtle.com/acceptance-testing-ember-cli)
	- 2nd May 2015 • Beginner • [Mario Gintili][MarioGintili]
	- Basic acceptance test use case run through
	- stubbing requests with [Pretender][pretender] & [Ember-CLI-Mirage][ember-cli-mirage]

##Forum Posts
- [Proper way to handler timers w/ Ember Testing](http://discuss.emberjs.com/t/proper-way-to-handler-timers-w-ember-testing/4693)
	- some options for Ember.run.later issue but no real conclusion
	- [proposed solution on Stack Overflow](http://stackoverflow.com/questions/27851517/ember-integration-testing-hangs-after-visiting-route#answer-27887807) by [Teddy Zeenny][teddyzeenny]

##Project Github Repos

###[LG Front-End](https://github.com/201-created/LG)
- stubbing authentication with [torii][torii]
- general patterns

Specific files
- https://github.com/201-created/LG/blob/master/tests/helpers/sign-in.js

https://github.com/stefanpenner/ember-jobs
Stubbing resolver, Pretender
https://github.com/stefanpenner/ember-jobs/blob/master/tests/acceptance/searching-test.js
https://github.com/stefanpenner/ember-jobs/blob/master/tests/acceptance/admin-test.js

[MarioGintili]: https://twitter.com/mariogintili
[teddyzeenny]: https://twitter.com/teddyzeenny

[ember-cli-mirage]: http://www.ember-cli-mirage.com/
[pretender]: https://github.com/trek/pretender
[torii]: http://vestorly.github.io/torii/
