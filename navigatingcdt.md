<h1>Navigating the World as a Context-Driven Tester</h1>

<h2 id="contents">Contents</h2>

[Introduction](#introduction)

[Responding to questions or statements around testing](#content)\
    &nbsp;&nbsp; [Testing](#testing)\
    &nbsp;&nbsp; [Automation](#automation)\
    &nbsp;&nbsp; [Context-driven Testing](#context-driven-testing)\
    &nbsp;&nbsp; [Scripts/test cases](#scripts)\
    &nbsp;&nbsp; [Testers](#testers)\
    &nbsp;&nbsp; [Testing Status](#testing-status)\
    &nbsp;&nbsp; [Project Scheduling](#project-scheduling)\
    &nbsp;&nbsp; [Career](#career)

[Acknowledgements](#acknowledgements)\
    &nbsp;&nbsp; [The Association for Software Testing](#the-association-for-software-testing)\
    &nbsp;&nbsp; [Contributors](#contributors)\
    &nbsp;&nbsp; [Licensing](#licensing)
        
<h2 id="introduction">Introduction</h2>

_Navigating the World as a Context-Driven Tester_ provides responses to common questions and statements about testing from a context-driven perspective.

The e-book was designed to act as an FAQ for the day-to-day situations a tester may find themselves in and how to approach them from a context-driven perspective.

The book was coordinated and collated by testing practitioner and long-standing AST member [Dr Lee Hawkins](https://www.linkedin.com/in/lee-hawkins-3574148). The content was crowdsourced, starting early in 2021 and the final edit was made in August 2024 after some 28 requests for contributions. These requests were made across multiple platforms, including Twitter (X), LinkedIn, Slack (viz. in the AST and Rapid Software Testing channels), Mastodon and the AST mailing list. All contributions are [attributed](#contributors).

<h2 id="content">Responding to questions or statements around testing</h2>

<h3 id="testing">Testing</h3>
<h4>How can I possibly test "all the stuff" every iteration?</h4>

It's never possible to test "all the stuff" because there are so many variables involved in running any piece of software anywhere that there's always another test that could be performed. What is possible, though, is to decide what is the important stuff to test given what we know about stakeholder concerns, risks to business value, time available, the software, and other relevant factors.

Firstly, does every single feature or area of the software really get changed every single iteration? The whole point of iterating over software during the development is to introduce small, but valuable changes and deliver them to users. Since the changes are small, most of the software is the same as it was in the last iteration and therefore does not need to undergo comprehensive testing again.

Secondly, you need to determine the level of risk introduced by these changes. What is being done to the software that introduces so much risk every iteration that someone believes it needs to be tested in its entirety? If something is being done that introduces that much risk, why is that being done and why is it being done every iteration? Thinking about risk helps you to work out what is an appropriate amount of time and effort to spend reviewing the changes. Sometimes that will include not looking at them at all. Maybe changes have broader scope than anticipated, or they introduce unintended consequences in other parts of the software. While these are fair concerns, most changes made to the software don't impact the entire system and you should not assume by default that they might.

Next, even if you're the only tester in your team, it doesn't mean you're the only person who can take on testing tasks. Perhaps you can suggest that someone else should pick up the task of checking that bug fix, or that you'd like to pair with someone to review the coverage of this test suite and see whether it can be extended to remove a day's manual effort at the end of each sprint, or that you think it would be a good idea to get together as a team to think about edge cases before coding the next feature so that more robust testing can be done during development. Similarly, some development tasks might not need to be tested or verified by a dedicated tester, but by anyone who did not write the code. 

In the same vein, wise use of automation might take some of the work off your plate. If there's some time-consuming repetitive testing tasks that are mechanical and boring to do, then they're likely to be done badly or not at all. Look for ways to subcontract that work to automation and free a human up to do something they're better suited to. While automation has limits and can’t check everything (see [Let's just automate the testing](#lets-just-automate-the-testing)), it can be very helpful. You need to understand what automation can and can’t do in your project, so you can make informed decisions about which features and paths you don’t need to spend much time on. When someone asks you to repeatedly perform specific tests, you might use that as opportunity to discuss spending some time on improving automation instead.

Attempting to test "all the stuff", whether every iteration or otherwise, is a fool's errand. Instead, you need to understand the scope of what's changed, analyze the risks created by those changes and then design tests accordingly. Remember that other members of your team can probably assist with some testing tasks and automation used wisely will likely help you to reduce the amount of testing you need to do whenever the software changes.

<h4>Developers can't find bugs in their own code</h4>

Developers can and do find bugs when coding. They not only find them in the code they are writing now, but also in code they wrote earlier, in their colleagues' code, and in the code of third-party libraries and applications they are using. 

Some people think developers can't find bugs because they don't realise that the developer is likely testing at layers lower than the tester. The developer might test something impossible to know about at any higher level. Something obvious from white box analysis could be a hidden, random guessing game from the perspective of a black box tester.

Developers - with their intimate knowledge of their own code - have hunches and concerns that can help testers find rich areas of concern to investigate. This presents an awesome opportunity for testers to broaden their understanding of risk by collaborating with developers .

The developer's detailed knowledge of their code has a downside, though, in that they lack critical distance. Critical distance may be defined as the totality of differences between any two ways of relating to or thinking about the same thing. Software testing in general benefits from critical distance and testers can identify problems that the developer themself was unlikely to spot.

Another way that the developer might have trouble is when the bug arises from a misunderstandings or mistaken assumptions. These represent blind spots that impacted the developer's choices while coding and are also likely to impact decisions they make crafting a test strategy. There are ways to get around these blind spots, but they are a difficult hurdle, particularly when we don't realize they are there. This is an instance where someone not as closely tied to the implementation choices, e.g. a tester, can often do better with testing.

Testing optimized toward exposing deep, complex problems takes uninterrupted effort and time. The typical time demands on a developer mean they either spend it designing a solution, coding a solution, searching for a fix to a problem, or coding that solution. These demands compete with the time for testing.

Developers find - and fix - bugs all the time during their coding work. They don't typically find all of the bugs in their code and are less likely to identify some kinds of bugs, but the same can be said of testers too. The combination of developer testing where it makes sense and testing performed by expert testers is likely to increase the chances of finding the bugs that matter.
    
<h4>We test to make sure it works</h4>

We test to learn and make sure we understand how it works, and for whom; and how it doesn't work, and for whom.

To get to an understanding of what "works" means for a particular piece of software, we start with testing to explore and mentally model it. As we learn more and come to an agreement with stakeholders about what it means for the software to be working, we must still be mindful that any certainty we’ve gained is limited to the types and variety of testing and experimenting we've performed. We can still be fooled – there may be dependency on variables that we might not even be aware of, it might appear to work for us but might not to the customer (and vice versa), or we may have failed to consider particular types of user.

So, when we test the software, we might explore who is likely to be using it, the things they might use it for, and what they would hope to get from it. It’s also worth finding out why we built this particular solution, what else we tried, and why the others were rejected. Through collaboration we are uncovering what "it works" means for different users (and stakeholders), situations, in relation to the purpose and intent of the product. All of these different components of the context of the software help us to test whether it gives the required value to the people who matter and also what risks it poses to these people.

With context in mind, we strive to understand what the software does well enough to tell the team making it enough that they can determine what could be changed to align with the intent. Our understanding also should enable us to tell the stakeholders enough that they can determine if what it does is sufficient to be deliverable.

We also need to be interested in whether the product does things that we don't intend it to, or that users expressly do not want, and what the effects of those things might be. In this sense, we also consciously test to find out how it might _not_ work.

No level of testing can provide certainty that the software works, so our understanding of perceived risks and threats to the value of the software drive our prioritization of what to test and to what degree. As we explore, our assessment of risk may well change in light of new information too.

<h4>Testing is just to make sure the requirements are met</h4>

Requirements come in many different shapes and sizes. While checking (explicit) requirements can be important, testing has much more to offer than just demonstrating that the software fulfils such requirements.

Many companies consider written requirements as their only requirements. This is a very narrow view of requirements. The majority of requirements are implicit and fuzzy. Requirements are fallible because the people who write them are fallible - they are often incomplete, ambiguous and contain internal contradictions.

Testing is a way of discovering unstated requirements and can often only come from a really thorough evaluation of the software. Testing can (and should) question if the requirements would actually solve the problem that the software is meant to solve, or if there is a different way it can be solved which is more appealing to the client. Testing can tease out ambiguities and clarify uncertainty, as well as discover and expose constraints.

There's also often an assumption that the requirements satisfy the needs of the stakeholders, and that the relevant set of stakeholders has been consulted and had their needs taken into account. Testing should ask whether we've met the requirement that the requirements make sense to the right set of people.

It's important to note that testing cannot ensure that requirements are met. Testing is sympathetically sceptical about the project. It seeks to help the stakeholders to build the best version of the thing they want within their constraints. 

Moving away from viewing testing as just a way to verify that the software meets the explicit requirements allows for more space for testing to add value to the project. Testing is a way of evaluating the software and its requirements, as well as identifying additional requirements, discovering ambiguities and exposing constraints.

<h4>Why didn't you find those issues before we shipped?</h4>

There are many reasons why issues find their way into released software - and we expect this to happen.

We should first note that we have a collective responsibility - from management down - for what we deliver. A healthy organization will be able to use this question as a means to analyze and reflect on their methods, procedures and practices.

We may have missed issues before we shipped because:

* We didn't look, or
* We didn't look in the right places, or
* We looked in the right places but didn't provoke the issue, or
* We looked in the right places and provoked the issue, but didn't realise
* We looked in the right places, and provoked the issue, and realised, but didn't understand the impact

There are many possible reasons for the above:

* Our ideas of what to review didn't cover this
* Our risk assessment prioritised other areas
* Our budget didn't permit us to test all of the places we thought of
* Our ability to control the product behaviour is limited
* Our visibility of the product behaviour is limited
* Our access to environments in which to test is limited

And we could explain some of these reasons:

* We didn't understand the domain implications
* We didn't understand something important about how our customers would use the product
* We didn't understand the code to a relevant depth or breadth
* We didn't understand the requirements, implicit or explicit
* We made some assumptions that were invalid
* We didn't spend enough time with enough perspectives to think of this possibility
* We didn't place a high value on checking our work relative to building it
* We didn't place a high value on checking our work relative to shipping it

Mistakes happen because humans are fallible. However, we can learn with the aim of improving when we all share responsibility and avoid the blame game. So a better version of this question might be "Could we examine as a group why these issues were missed before we shipped the product, so that we in future can ship a better quality product to our customers? I would like you to be honest with me, and not hold anything back."

<h4>When is the best time to test?</h4>

The best time to test is, usually, now. You still need to think about what to test, how to test it, and why it might make sense to test it now.

Consider whether there's a good chance the effort will be worth the expense. Is there enough of something to be tested now? Is the information you get from the testing most useful right now? Is there actually an opportunity to test now?

Deciding what you could or should be testing now depends on many factors, including where the software is in its development lifecycle and how involved you can be as a tester in these various stages. Each phase of developing a product - from ideation to release - has some hypothesis that could benefit from being challenged, though.

Tasks like these could all be productive and cost-effective testing at different times:

* Test a new market for opportunities
* Suggest pros and cons of potential projects
* Build models of potential features
* Look for evidence that the suggested needs are worth addressing
* Synthesise previous discussion to provide a set of constraints on any solution
* Ask questions of the designers, architects, programmers, customers and stakeholders (practising "prospective testing", a term coined by James Bach and Jeff Nadelman)
* Prototype solutions to discover likely issues
* Research similar solutions to identify missing features, failure modes, test ideas, etc.
* Critically analyze specifications or mockups, looking for assumptions and gaps, and asking questions
* Explore the emerging solution, as it emerges
* Explore the implemented solution in context 
* Compare the capabilities of the implementation to the original needs
* Try to find new risks introduced by the solution
* Explore the new feature in production
* Monitor the behaviour and performance of the new feature
* Look for evidence that the solution is satisfying the identified needs
* Explore user data to look for patterns
* Analyse telemetry data for potential bottlenecks

If you're unsure about what risks to investigate, the scale of a potential problem, the cost of a range of solutions, or have any important unknown at all, then the best time to test (all other things being equal) is now. If software is being developed and you are involved in that process as a tester, you can almost always find some way to be testing and providing valuable information to your stakeholders.

<h4>Are observability and monitoring part of testing?</h4>

To the extent that observability and monitoring influence testability, they are part of testing.

Observability is an attribute of a system which refers to the ability to make observations of its behavior and state. Observability is *not* a kind of testing. Observability affects our ability to test, since we utilize and exploit a system's observability when we test.

Observability can help to answer questions after a product is released and so can serve multiple needs including testing, customer support and business intelligence. Observability exposes how our systems actually work, by making it easier to learn how our users actually use the systems that we built and shipped. 

Turning to monitoring, most tooling that you'll integrate for logging, monitoring and telemetry will have a facility for interrogating the data it produces. This can help to answer questions, and so be part of testing, but can also be used productively to explore that data looking for questions to ask. Armed with this new understanding we can enhance our telemetry, craft better dashboards and alerts, tweak the infrastructure, or change the product - this can be considered part of testing too. 

When combined with capabilities such as partial deployment and quick rollback, monitoring can provide risk reduction in a post-hoc way instead of as an expensive pre-emptive effort.

A system that has better observability has better testability, and we can use monitoring to suggest usage patterns that could inform future testing and also to run experiments we can't replicate in our labs. The fact that it *can* be used for testing, however, does not make it a *part* of it.

Information about how software is actually used, what parts are most visited, for how long, when, on what environments and by how many users is invaluable to a development team - this information, and potentially more, is provided by observability and monitoring. For testers, it can be extremely useful, helping to design better tests and to design testing environments that better model actual production environments.

The **TOAD** acronym, introduced by Noah Sussman and built on by Chris McMahon, can be helpful in understanding the tight connections between **T**esting, **O**bservability **A**nd **D**evOps.

The idea behind TOAD is that there is a common thread between all three concepts and, when you focus on them, you are able to better understand your application. DevOps facilitates the development process from desktop to production. Observability tells us what has happened on the system in great detail. Testing helps us to understand what the system actually does. (Taken from [Chris McMahon's blog](https://chrismcmahonsblog.blogspot.com/))

The interplay of testing, observability and DevOps make sense. Let's use an example:

* We create well designed automated tests to help us show our application works.
* We add them to a pipeline to detect changes throughout development.
* We observe if the changes in the behaviour of the application caused by the tests are acceptable or if they create new problems.

If monitoring is robust and thorough enough, it can reveal information about the system’s functionality, reliability, and other characteristics that are traditionally assessed during testing. Observability takes us further by understanding what is happening to our application(s) under test during our testing. This blurring of the lines is captured well by TOAD.

Observability and monitoring can both provide capabilities that help testing. There is value to and overlap with testing in expressive logging and tracing capabilities. Taking observability seriously (and thinking of it as a requirement of the software) allows you to understand and learn about the software you're testing, at a depth beyond UI "correctness" against modeled expectations. The ability to capture evidence of failure can help us move software engineering and the discipline of testing past shallow, binary "functioning to spec" checking to continuous learning and exploration.

<h3 id="automation">Automation</h3>

<h4 id="letsjustautomate">Let's just automate the testing</h4>

While automation can be a valuable tool in testing, it can't replace the human.

A context-driven tester believes that good software testing is a challenging intellectual process. While there's often a great deal of scope for automating a path after it's been trodden, it takes intent and agency to find the paths worth following and the things to look for while walking along them. 

When people speak of "[automating the testing](https://www.developsense.com/blog/2017/04/deeper-testing-2-automating-the-testing/)", they're often talking about automating the typing, or the mouse clicks, or the looking up of results in a table, and comparing it to output from the product we're testing. But testing is far more than mashing keys and moving mice and looking stuff up. Tools can assist us with our testing in powerful ways, but testing cannot be automated.

A computer can check whether or not certain conditions are met, when programmed to do so, but only a human can make the judgment call on what checks are necessary, and when. Also, only a human can interpret the (meaning and significance of the) results, or the lack thereof, and decide whether or not we have a problem. Sometimes, a failing check, or a missing result, is the desired outcome even if, some other time, that exact same outcome would be a problem. A computer cannot make this distinction.

We need to be deliberate in our thinking about how automation can help us to test and also what makes sense to automate. Perhaps there is some repetitive confirmatory work that humans currently do that is time-consuming and boring and is amenable to being implemented in code - this seems plausible as a target for automation. We'd probably want to consider effort and value factors such as the costs associated with developing and maintaining the automation, the risks it would mitigate, and the potential multipliers that it could bring (such as documenting behaviour, and being runnable in different environments).

The diminutive "just" in the statement ("Let's just automate the testing") makes it seem like such a quick and easy thing to do, a casual activity that we can engage in that takes minimal effort. Implementing automated checks requires significant human effort and should be considered as software development work in its own right.

<h4>If testers can't code, they're of no use to us</h4>

There are many non-coders that are a part of software development, including product managers, technical writers and designers. People in all of these roles might benefit from being able to code, but generally bring value to the table without it. So, what about testers? 

Testers are sometimes worried that they won't be taken seriously on their project unless they have a coding background. But software projects typically include people who are expected to write code. We call them developers. If coding is so important to the project, what additional value does a tester who can code give over a developer? If there's none, why look for a tester? If there's some, why couldn't a tester provide it and be supported by developers? 

If a tester has coding skills, they may be able to write tools, automated checks, contribute to repos (such as to make minor bug fixes), provide feedback in design and code reviews, participate in unit testing or build a test framework. Their level of coding skill and experience will determine the degree to which they can contribute to all of these possibilities. So think about whether it's enough that the tester can hack together a temporary test rig out of Python and bash or whether you really need a tester who can architect and build a company-wide, end-to-end, full-stack, test framework.

If developers and testers work closely together, developers can support and enable testers (e.g. by building test tools) without threatening the testers' ability to test deeply and maintain their critical distance from the code.

Testers in many ways are advocates for the user and sometimes fill in as a proxy. Evaluating software by testing from the viewpoint of the code risks missing important dimensions such as usability and user experience (though, on the flip side, the ability to read the code might help to expose potential sources of bad UX because known antipatterns can be searched for easily instead of being discovered by exhaustive exploration).

Clearly, testers with coding skills can contribute to projects in ways that testers without those skills can't. Non-coding testers still bring value to their projects, though, so consider whether coding is better left to developers who can support testers in their work.

<h4>What percentage of our test cases are automated?</h4>

The number of test cases and the percentage of those that are automated doesn't really provide any useful information about quality. 

A question like this could be a relatively harmless example of [availability biases](https://thinkinsights.net/strategy/availability-heuristic/) influencing people's perception of what testing is. For some people automated tests will be the first (and perhaps only) thing that comes to mind when they hear the word "testing" (see also <a href="#letsjustautomate">"Let's just automate the testing"</a>).
    
The term "test case" is vague and so, when being asked for a percentage such as this, it's reasonable to assume that the questioner thinks a test case is a consistent or meaningful unit by some measure. Unfortunately, a percentage is problematic in the real world where test cases are quite different from each other in important ways. One test case may have 20 steps while another may have two, automating one but not the other gives you a 50% rate either way. Maybe only 50% are automated, but perhaps those were the 50% that provide 95% of the coverage of regression risk, or maybe those were the 50% that comprised 75% of the execution cost.

The question is less meaningful when there is no set of scripted test cases, or the baseline is compared against tests engineers perform regularly. The behavior and outcome of an automated, scripted check of a piece of code or system is very dissimilar to what happens when a human tests a piece of code or system.

Faced with a question like this, it's perhaps better to reframe the conversation by asking some more critical questions about the state of test automation for the software. Questions such as:

* What risks are mitigated by our automated tests?
* What should we definitely *not* be automating?
* What signals are we missing by relying on this automated test?
* Are these tests genuinely useful and do they actually detect problems?
* Are these tests the most efficient and helpful way of obtaining the information we want to learn about the software? 
* Can the information we want even be reduced to a pass or fail, or does it require more nuanced evaluation and assessment?
* Are the tests actually worth the cost of executing and maintaining them?
* What value do they provide to us, our team, our stakeholders and our customers?

Instead of concerning ourselves with calculating percentages of tests that are automated, we should be looking more holistically at our test strategy and where automation fits into it, makes the most sense and delivers useful information. Providing a single numeric answer to this question is a missed opportunity to explore more deeply the role that automation does - and should - play in your testing approach as you look to deliver value to the business from your testing efforts.

<h4>When the build is green, the product is of sufficient quality to release</h4>

The common risk of every single software release is that there might be important problems that you don’t know about and that you underestimated problems that you do know about which turn out to be more serious than you thought. 

Relying on a "green build" for a release decision is really making a bet - is this one-time measurement of this particular build going to be enough to mitigate this risk? Whether or not the checks run during the build are sufficient to safely make that bet depends, as always, on context; in some situations, it's a horrible bet, while in others it may work well.

Firstly, what do we understand by a "green build"? Probably it's something like one of these: all of the unit tests ran locally and none showed a failure; unit, integration, and other tests ran in some continuous integration pipeline and all passed; or the product was built and deployed then end-to-end tests were run across it and other services without obvious error. The common aspect of what we generally understand by green builds is that some kinds of tests or steps ran and none were reported as unsuccessful as far as we can see.

Secondly, what exactly is being checked? What are we trying to test, how broadly, how deeply, to what level of accuracy, covering which parts of the product, according to whose expectations, in what combinations, in what environments, for what purpose? We need to consider whether there's a difference between what was intended to be tested and what is actually being tested. What do "pass" and "fail" even mean? The kinds of tests we're discussing here are more change detectors and less error detectors. While many people are concerned about false negatives, they overlook that there might be false positives as well, so consider the possibility that the build is "false green".

Thirdly, the meaning of "sufficient quality" is highly context-dependent and will often include intangibles that are hard to test for in a pipeline, such as usability. If you can define metrics that represent sufficient quality for you, and they can be evaluated programmatically, then they could certainly be added to a build pipeline. But this does not mean that the tests assess all of what makes a product sufficient quality for our users.

Finally, we need to understand our release process and risk tolerance. If we have great monitoring for all important business KPIs and easy rollback, and if the risk of fudging a release is low enough and our tests provide us with enough confidence then there's a good chance that we can safely release once "the build is green". In any other situations, though, we need to factor in the risks and rewards to make this decision. Some people mitigate the "sufficient quality to release" concern with feature/service capabilities that allow for exposure control and isolation so that testing may continue post release, and then a feature is activated only if no further issues are discovered.

To be confident enough that "green" indicates a build of sufficient quality to release, ensure that your context allows for this choice to be viable. If not, human involvement in analyzing test results and making risk-informed release decisions is probably still a good idea.

<h3 id="context-driven-testing">Context-driven Testing</h3>

<h4>Isn't all testing context-driven?</h4>

Existing in a context is not the same as consciously choosing how to take account of it, watching for changes, and adapting accordingly; that is, being *driven* by that context. In this sense, not all testing is context-driven.

Many testers have had the experiences of not knowing why they're doing the testing they're being asked to do, not knowing who cares about the testing they're doing, and not knowing why the testing they think they should do is the right testing to do right now. These are all potential indicators that the tester and their testing is not being actively driven by the context.

On a project, a context-driven tester might seek to understand what the project aims are, who needs to benefit, in what ways, and why the approach proposed is thought to be appropriate. They could wonder whether the personnel, timeframe, and tooling are likely to deliver the desired outcome, and if not why not. They will look for ways that they can contribute to the project's success under whatever constraints it has and with whatever skills they have.

Testers who are taking a context-driven approach will recognise that every participant's perspective will differ to some extent, not least because we are each an integral part of our own contexts. They will try account for that by, for instance, repeated observation, applying heuristics, finding similar examples from their experience, calling on their expertise, looking for collaboration, making regular attempts to synchronise with the people who matter on the project, and aligning work with current goals and restrictions.

Being context-driven helps to minimise "best practice" and "one size fits all" thinking. Context can change regularly, rapidly, and often in unpredictable ways so being mindful of it encourages us to eagerly adapt, reducing the risks of status quo bias and the complacency that can follow. Context-driven is sometimes constrasted with "context-oblivious", where testing is performed using using a well-worn process and without considering the business needs and other important contextual factors.

<h4>There are no best practices, really?</h4>

One of the context-driven testing principles reminds us that:

*There are good practices in context, but there are no best practices.*

Context is crucial. An approach that works for you, for this problem, today might not work for me, or for an apparently identical problem, or on another day. 

"Best" is often intended subjectively (as in "in my opinion"), or in some implied context (as in "in some specific situation"), or as hyperbole (as in "it is really good"). But there are real, practical, benefits to taking the perspective that there are no best practices. The primary gain is that it can help you to make an informed choice, balanced across competing needs and constraints, given what you know at the time.

"No best practices" doesn't mean that no practice can ever be reused. We shouldn't assume that we are smarter than everyone else - ignoring widely used practices is not something to be done lightly. What is important is that we understand the prerequisites, benefits and drawbacks of each approach we consider employing and adjust it to meet our specific situation.

Although it might sound like "considering the context" is itself a best practice, there are clearly situations in which stopping to take account of the context might be the wrong thing to do; for example, in life-or-death situations where you must simply act.

So, while we could choose a charitable interpretation when we hear the term "best practice" being used - rather than the speaker really meaning "the most excellent, effective, or desirable, always, everywhere" - we benefit from thinking instead of good practices in context, reminding us to make a more considered choice in the unique situation we find ourselves in.

<h4>What's the difference between context-driven testing and exploratory testing?</h4>

Context-driven testing is a paradigm that focuses on how good testing can fit into software projects, while exploratory testing is an approach to performing the testing.

By way of reminder, the seven principles of the [Context-Driven School](https://context-driven-testing.com/) are: 

* The value of any practice depends on its context.
* There are good practices in context, but there are no best practices.
* People, working together, are the most important part of any project's context.
* Projects unfold over time in ways that are often not predictable.
* The product is a solution. If the problem isn't solved, the product doesn't work.
* Good software testing is a challenging intellectual process.
* Only through judgment and skill, exercised cooperatively throughout the entire project, are we able to do the right things at the right times to effectively test our products.

The "context-driven" part of context-driven testing is about where you're situated in the project community. It is the recognition that the surrounding circumstances in which we're testing affect the way we need to approach that testing. It is premised on an aspiration to deal with and respond to the context first.  (This is not the same as being context-aware; the difference is that context-aware testers would acknowledge and respond to the context, but *not* do so first.)

While there are many definitions of "exploratory testing" and they continue to evolve, they generally highlight the importance of learning and the need for the tester to have agency.  For example, Maaret Pyhäjärvi has coined the term "[contemporary exploratory testing](https://visible-quality.blogspot.com/2021/01/contemporary-exploratory-testing.html)", while James Bach and Michael Bolton have now dropped the "exploratory" label because to them [all testing is exploratory](https://www.satisfice.com/blog/archives/1509) (though they still might explicitly use "exploratory" to highlight when they are referring to the more informal end of their [Testing Formality Continuum](https://www.developsense.com/blog/2019/01/breaking-the-test-case-addiction-part-3/). Elisabeth Hendrickson presents a useful introduction to exploratory testing in her ["Explore It? Explore It!" YouTube video](https://www.youtube.com/watch?v=9FKY1Is0lgs).

Exploratory testing does not dictate a context-driven approach and it is certainly possible to test in an exploratory way without helping the project at all. One such situation might involve a tester getting deeply interested in some little-used aspect of a product's behaviour and neglecting any other testing despite requests from colleagues not to do so.

Context-driven testing is a community, an approach and paradigm around testing. Exploratory testing is an approach to performing testing focused on learning and tester agency.

<h3 id="scripts">Scripts/test cases</h3>

<h4>Do more test cases mean better test coverage?</h4>

If we can assume some common ground on the definition of "test case" and "test coverage" then it's probably reasonable to say that more test cases mean more test coverage. Whether that coverage is *better* is the deeper and more interesting question.

The terms "test case" and "test coverage" are loaded, but for this conversation let's say:

* A test case is a description of a procedure for setting up and observing conditions that we could examine in the course of a test, and
* Test coverage is a measure of the extent to which the test cases, when executed, exercise the software under test.

If the test cases don't help you to uncover important bugs that matter, then how many you have is irrelevant. If they don't help to fulfil the mission of testing, then it is reasonable to say that the coverage is not better just because there are more of them. Quantity isn't quality! 

Are the test cases adding value? Are they trying new things in interesting ways? Are they covering multiple dimensions of quality or just verifying narrow acceptance criteria? Are the tests run in combination to discover potential problems with sequences of events? Are the tests run in such a way to vary the inputs (in interesting ways), or just using the same values over and over again?

One way to think of a test case is as a container for a test idea. It could be helpful or unhelpful in finding out information about the product. Having more test cases isn't a meaningful measure, a larger number of bad ideas is still not helpful. 

Even with lots of good ideas about what to test, it's worth remembering that the test cases themselves are not testing. Until you actually start to test, there is *no coverage at all*. Moreover, until you start to test the risk areas, quality dimensions, and other concerns the team has identified as important, it's questionable whether you have *valuable* coverage. 

So, whether having more test cases results in better test coverage really depends on how well the test cases are designed and how they address your most important concerns - and, of course, no amount of them will provide any benefit unless you actually perform the testing described in those test cases!

<h3 id="testers">Testers</h3>

<h4>Why don’t we replace the testers with AI?</h4>

You can't replace testers with AI simply because there's no AI capable of doing all the things that testers are doing (as of the time of writing, April 2024).

You might consider replacing testers with AI because:

* You don't understand what testers actually do.
* You don't value what testers do and so see AI as a cheaper alternative.
* You don't appreciate the variability, novelty and complexity of your context; the domain, company, and technical knowledge needed to navigate it; or the ability of a person to use a combination of heuristics, logic, and instinct to identify risk and prioritise work across diverse concerns.
* You conflate testing with test cases and see test case creation as a mechanical task easily done by, for example, a large language model (LLM).
* You focus on deliverables and think that testing artefacts could be replicated to an acceptable level faster and cheaper by a black box full of who-knows-what statistics (without considering how many of those are interesting, relevant, or useful).
* You fall for the LLM illusions of reasoning, so think it's creative and capable without looking critically at its output.
* You don't consider the total cost of ownership, focusing on how quickly work items are drafted but ignoring the less tangible costs. You forget the human time and effort spent sifting, evaluating, and correcting the AI's outputs, as well as any training, testing, maintenance or other costs of the AI you plan to use.

However, you might consider it inappropriate to replace testers with AI because:

* Testers bring a human perspective to the process, understanding user experiences in a way that AI currently does not.
* Testers can think outside of the box to identify new approaches, methods, and techniques for discovering potential risks and issues that AI currently does not.
* Testers are needed to validate and verify the AI itself to investigate whether the learning models are correct, complete, consistent, verifiable, secure, ethical, responsible and more. 
* Artificial intelligence is not human intelligence.

AI "taking testers jobs" might not be a problem we are going to have anytime soon. Until AI autonomy is met with an equal level of trust, there will likely be human-in-the-loop checks and balances. If you think AI can replace your current job, testing or otherwise, it's probably time for you to start thinking about transitioning to the more human side of your profession. Rather than thinking about replacing testers, given the current state of AI, you should instead look for ways to leverage these technologies to augment, assist and extend the capabilities of human testers.

<h4>Pair and ensemble testing look like a waste of time and resources to me. What do you think?</h4>

Pair and ensemble testing are approaches to collaboration and they may or may not be wasteful (or helpful) in your particular situation.

There are some potential benefits of pair and ensemble testing, including:

* Sharing knowledge between team members
* Gaining multiple perspectives and insights
* Learning from one another
* Sharing our personal opinion and experience
* Investigating difficult bugs together
* Helping non-testing folks understand how testers work, think and test a product

Pair and ensemble testing might not be beneficial too, including when:

* Participants are skeptical of the value of the activity
* These approaches are not well suited to the task at hand (e.g. document reviews might be better left as solo efforts)
* Your sessions are not well prepared (e.g. there is no set end goal, rules of engagement, and sufficient time to review outcomes)
* The people involved don't have the skills or understanding of the approach

Pair and ensemble testing are tools and, like any tool, they have benefits and costs, learning curves, contexts where they make more sense, practitioners who hate, enjoy or flourish with them, and numerous other factors that trade off against each other. It may be worth running a small experiment with pair or ensemble testing then review and analyse the outcomes to determine whether they provide value in your situation.
    
<h4>What's the right ratio of developers to testers?</h4>

There are so many factors that can influence the answer to this question that it simply doesn't make sense to talk of an "industry standard" ratio.

Some factors that can influence the developer:tester ratio include:

* The type of work the team does (greenfield, maintenance, integration, research, etc.)
* The mix of personnel (experienced, expert, newbie, enthusiastic, completer-finisher, creative, etc.) 
* The skills of the team members (development, testing, architecture, co-ordination, leadership, etc.)
* The team's familiarity (with the tech, with the domain, with the customer's system and with each other.)
* The timeline for the product
* The software development process used to develop the product (e.g. are good development practices such as unit testing, static code analysis, code reviews, etc. in place?)
* Any regulatory requirements that need to be met
* The inherent testability of the product
* The level of automation (reducing the amount of regression testing performed by humans, perhaps)

It's important to consider factors such as the above when determining team structure. Furthermore, particularly in agile teams, the team members are usually more [T-shaped](https://en.wikipedia.org/wiki/T-shaped_skills) in terms of their skills and developers will have responsibility for some types of testing. This makes it hard to delineate "developer" and "tester" when it comes to the testing activities being performed in the team.

If you really need to get a quick estimate for setting up a new team, then a reasonable strategy would be to get numbers from ongoing projects, assume nothing much will change about how projects are set up in the coming 12 months, and use that as the basis for your response. But you really should be taking into account the unique set of factors comprising the context of the team and product to decide on your ideal team make up.

It's likely that talking to the team members and looking carefully at its practices, its interfaces with other teams, the business, and so on is a better way to work out a good balance of developers and testers than waving some arbitrary and context-free mathematical wand. Focus less on targetting a certain ratio and more on determining how much you want to learn about the product and how to accomplish that. This will determine who does what testing and how many of each kind of team member you need - and this will almost certainly differ from project to project.

<h4>Testers are the gatekeepers of quality</h4>

We don't think of scientists and journalists as gatekeepers of public policy. Just like them, though, testers observe, investigate and report on things - but testers are not gatekeepers.

As professionals, testers accept responsibility for the quality of their own work, but testers can neither accept nor usurp responsibility for the quality of the product, and for making decisions about it. Like news journalists, investigators, scientists, researchers and building inspectors, testers are gatekeepers of the information they communicate from what was discovered when testing. They are responsible for the quality - the value - of that information delivered as a product to decision-makers - value that is subjectively determined by those recipients. Sometimes, this information may be in the form of opinion or recommendations.

The goal of the tester is to help the team to build a great product. Assigning them gatekeeping responsibility (slowing down and blocking inadequate products to pass) puts this goal at risk. 

A tester in a position of quality gatekeeper risks being blamed if a problem does get to production, and also puts them on a path of friction and internal politics with the rest of the company when deciding to stop a release due to severe known bugs. If we are holding the entire team accountable for their work, it makes little sense to designate someone to be the gatekeeper. 

Although testers may sometimes feel empowered by the idea that they are the gatekeepers of quality, it sets them up for unrealistic expectations and isolates them from their teams. The idea of testers being gatekeepers also massively undersells the wide range of benefits that a good tester can bring to an organisation by opening or even crashing through gates, rather than standing next to them.

<h4 id="depends">Stop saying "it depends" when I ask you a question</h4>

"It depends" is a truthful answer to many questions in any non-trivial context but, unfortunately, it's not usually a very helpful answer. Our aim, as context-driven testers, is to be truthful but also clarify how, why and on what our answer depends. 

By leading with "it depends", you flag to the questioner that they have not given sufficient information for you to provide a decent answer. You might follow with a clarifying question or two to refine your understanding of what information they are actually looking for or your analysis of what options are available. Take care when responding to a question with a question because, as you've doubtless found, many people in business have little patience for nuanced conversation. 

In composing an answer to the question, use your experience and the context to decide which variables matter to the questioner. You will need to make assumptions about how much time they have, how deep they want to go, and how much they care. All of this reasoning is necessarily imprecise because you don't know what their need is, or what they plan to do with your answer. 

Initiating your response with "it depends" is a way to indicate that you're thinking about contextual factors that will influence your answer. Following it with an appropriate summary of the perceived important variables and their potential consequences, while being ready to add depth or clarification, will signal that you are a valuable contributor and collaborator. As the context-driven principles say: people, working together, are the most important part of any project's context. 

[See also "Stop answering my questions with questions"](#questionsquestions)

<h4 id="questionsquestions">Stop answering my questions with questions</h4>

Being able to ask the right questions is one of the most important parts of our job as testers. We often find ourselves being asked questions that require further clarification or information before we can provide answers. Answering questions with questions to help close the gap is not something to be avoided. 

In this situation, it's perhaps worth explaining that you're not intentionally trying to evade the question, but rather looking to get to a point of shared understanding for the particular context you're in. 

Many questions are not well posed, so use follow on questions to ask for more information and gather more context. Asking for more insight gives clues into the motivation behind the question and the person receiving the question(s) gets confirmation they are being heard. Making the effort to ask such follow on questions helps to make sure we're answering the question they're really asking and not potentially answering something else because of a misunderstanding.

We sometimes need to "answer" questions with questions, not to be evasive or confrontational, but because we care about giving responses that suit the context.

[See also "Stop saying "it depends" when I ask you a question"](#depends)

<h3 id="testing-status">Testing Status</h3>

<h4>What's the best testing metric?</h4>

Much like [there aren't universal best practices](#there-are-no-best-practices-really), there is no single "best" metric. 

A metric is a model or system of measurement. Testing is an open-ended analysis and so not usually something worth measuring in and of itself, especially not without a strong relationship to the product being tested.

Metrics can deliver insights by delivering data to help people or teams progress or improve. It makes sense to define goals that testing should help to achieve, e.g. faster development cycles, less rework, fewer rollbacks, more informed decision making, or reaching compliance. Each of these goals (and more) have some aspect that testing can help to address and, since improving them is the real goal, there's no need to measure testing separately.

A generally good metric for testing could be:

*The extent to which the people who matter are satisfied with what they're getting from the testing, given what it costs.*

Assessments of the happiness and morale of your team are also important metrics (and not just for testing teams).

Even if some testing metrics might be useful, they can't be equally useful for every team or organisation in all contexts. Focus instead on what a good testing metric looks like in your context and how it can help you to improve.

<h4>We need some productivity metrics from testers</h4>

We understand that testers are knowledge workers and so traditional, simple measures of productivity do not apply. A concept as complex as productivity cannot be assessed with numbers alone.

When asked for metrics, it's important to understand:

* Why are the metrics wanted?
* What decisions will these metrics support?
* What are the behaviours these metrics are expected to encourage?
* Who needs them?
* How they will be used?, and 
* That the data could be flawed.

In his essay [Knowledge-Worker Productivity: The Biggest Challenge](https://ams-forschungsnetzwerk.at/downloadpub/knowledge_workers_the_biggest_challenge.pdf), Peter F. Drucker contrasts knowledge work with manual work to show how traditional, simple, measures of productivity such as the number of identical widgets produced per hour cannot apply directly to knowledge work. How do you "count" thinking and evaluating? It is very easy to produce useless and misleading metrics - such as hours of availability, bug counts and test case counts - that are easily gamed and are bad indicators of value and productivity.

It might be useful to find out if the questioner has some thoughts on what a productive tester looks like or whether they have some concerns about existing tester productivity. If the question really reflects a lack of trust in testers, then discussing those trust issues is likely far more important than any metrics the testers could provide. The question may also reflect a genuine concern that the testers are being distracted from the job at hand, in which case the testers could provide some metrics, such as the hours actually spent testing in the working day - but these would, again, need to form part of a wider conversation. It might be more impactful to look at measuring the productivity of the engineering group as a whole, rather then trying to optimize the testing activity separated from the rest of the tangle of creating a product. 

Measuring knowledge workers' productivity is a difficult task and every metric we use might have adverse side effects we need to take into consideration. We can measure and improve certain behaviours, but they probably won't be directly linked to "productivity". 

<h3 id="project-scheduling">Project Scheduling</h3>

<h4>Testing is a bottleneck</h4>

The statement that "testing is a bottleneck" warrants deeper investigation to determine whether the symptoms being observed are in fact indicative of a testing problem, whether a genuine bottleneck actually even exists, or whether other issues are at play.

Let's take a definition of bottleneck (from [Investopedia.com](https://www.investopedia.com/terms/b/bottleneck.asp)): "A bottleneck is a point of congestion in a production system (such as an assembly line or a computer network) that occurs when workloads arrive too quickly for the production process to handle." 

If testing is a bottleneck in this sense, then we need to think about why the testing is taking a long time. 

Are the testers working inefficiently? Are there enough of them to handle the development work being passed to them at the required speed? Are there testability issues within the product/application/system?

Are there processes that are slowing the team down? One common time consuming part of a slow testing process is the demand that certain checks or scenarios must be repeated every time something new is about to be released.

Are the testers finding lots of bugs that slow down the pace of development? Note that this doesn't mean that testing is a bottleneck!

Maybe it just seems from management's perspective that testing doesn't happen quickly enough and leads them to think of it as a bottleneck in the delivery process. Is the way that testing is reported to management perhaps creating this perception? Are management not giving testing the priority it needs because of a lack of understanding of what value they get from the testing effort?

There is also the definition of bottleneck as "someone or something that retards or halts free movement and progress". It could mean that testing as an activity in and of itself is resented. Maybe testing is seen as getting in the way of 'getting valuable updates into the hands of our users quickly' or the idea of shipping code as fast as possible is seen as more valuable than having high confidence in the stability of the code. Testing might then be seen as restrictive and unnecessary. The key is to balance the desire to ship with the prudence afforded by good risk assessment informed by the testing. Testing is not really a bottleneck here, provided that a mutually acceptable balance is struck.

So, is testing a bottleneck? It might be, but the complaint (as the statement typically seems to be framed) may be more about other things and not solely about testing. It's worth digging deeper to find out if there's a problem related to testing and whether a bottleneck actually even exists.

<h4>Will the testing be done by Friday?</h4>

Testing *can* be done by Friday, depending on what we mean by "testing" and especially what we understand by saying it's "done". We'll see that this question often really boils down to how we make decisions about when to stop testing.

This question can be interpreted in a number of different ways.

If the question relates to some prior discussion about scenarios we've agreed to run through before Friday then we can base an answer on the experience gathered so far. How similar are the scenarios to each other, how long has each taken to set up and explore, what kinds of issues have been found, how many of them do we want to fix, how long will fixes take to deliver and so on. We may have agreed ahead of time about a specific set of testing activities to complete by Friday, but there's no guarantee that this set of activities will be completed. It also doesn't guarantee that, at the completion of those activities, everyone will be satisfied that testing is sufficiently "done."

The question might imply that Friday represents a new deadline or at least that there's something important about Friday. We can stop testing by Friday but need to remind the questioner that, in general, testing isn't "done" done, because there's always another question, another set of constraints or another variable that we could consider. Whether we will have covered all the things we (as a group) consider important by Friday is a different question, not least because we don't know what problems we'll find between now and Friday. However, knowing that Friday is a deadline we can have a chat about what areas to priortise that would give us the best chance of finding the most useful information for the project in the time we have.

Perhaps the most likely interpretation of the question is as a request for status and whether some kind of agreed test report will be available by Friday. As testers we should be able to clearly communicate testing status in terms of:

* The areas we've looked at so far, from which perspectives and to what depth
* The kinds of problems we've found and the perceived importance of them
* The risks we are aware of, some sense of their likelihood given what we know and any open questions
* Any impediments to doing our best testing work

We should be ready to report such status by Friday - or at any other time it's requested of us. Whether or not the testing is "done" is a matter of making a decision. The decision to stop testing does not lie with the testers but with the stakeholders based on the information provided by the testers. The decision to continue testing (or not) should be made by the entire team and the stakeholders after reviewing the test report.

Testing could be "done" in an hour, or in a week or in a month, depending on what testing we perform and what it means to call that testing "done". The answer to the original question is more than a "yes" or "no" - a context-driven tester would look to find out what's really being requested by digging deeper to understand the motivation for the question to help provide a more contextual, meaningful and valuable answer.

<h4>What's the best format for a test plan?</h4>

There is no single "best" format for a test plan. You should use a format that works for you, your colleagues, your intended audience and the context you're in right now. 

A test plan may serve a number of different purposes and the format for your test plan needs to find the right balance between them.

As a **thinking tool**, it could act as a set of points that are most important to you - it could be a list of relevant risks, a checklist of affected modules, or a reminder to think about security tests. The plan can aid conversations to refine these details.

As a **communication tool**, it should be as short, structured and focused as possible, and yet still manage to tell a story that is of value to its audience.

As a **piece of evidence** that might be needed to pass some audit, it should be properly labeled and linked to other related evidence.

The content will be determined by many factors:

* If you work closely with a knowledgeable and self-motivated crew, it might be a simple bullet list of test ideas or a handful of sticky notes on a board.
* If you're in a highly-regulated industry, it might be some heavily-templated and standardised document that forces you to include all of the information necessary to comply with internal, regulatory, and statutory requirements.
* If you know the system under test well, your plan might be well-populated before you start, but if you don't then it might be sparse and higher-level with more open-ended and exploratory tasks.
* If you want to revise the plan as you go then a format which permits editing, perhaps with some kind of audit trail or history, might suit your need. 
* If you need the plan to also show status over time, a mindmap can be an interesting approach.
* If there is a pre-existing convention for plans in your workplace, and it's widely used with reasonable outcomes, you might decide to stick to it, at least to begin with.
* If there is familiar tooling that you can exploit then you might prefer to do that.
* If you don't have much time, choose a lightweight format to begin with but be prepared to revise it if things get complicated.
* If the plan is likely to persist over time, consider a format that will support it. This probably includes at least more context-setting, links to related materials, storage in a standard location and so on.
* If it's politically advantageous to document your plan in a particular way, then be prepared to consider it. But also be wary of getting involved in politics.

While there is no single "best" format for a test plan, taking into account the purpose of the plan and the content required in your context can help to produce a test plan that has value to your audience - and help you avoid creating a hefty document full of pointless content that is wasteful to produce and doesn't satisfy your audience's needs.

See also [What Should A Test Plan Contain?](https://developsense.com/blog/2008/12/what-should-test-plan-contain) (Michael Bolton) and [The Ideal Test Plan](https://qahiccupps.blogspot.com/2021/08/the-ideal-test-plan.html) (James Thomas).

<h3 id="career">Career</h3>

<h4> Whenever possible, you should hire testers with testing certifications</h4>

While holding a testing certification may be a signal that a candidate has a learning mindset, it doesn't guarantee that they're a great tester. Taking additional factors into account in your hiring decisions is likely to be beneficial.

If you decide to only hire testers with testing certifications, it creates a [funnel problem](https://recruitingdaily.com/podcast-episode/advanced-rpo-the-invisible-costs-of-open-jobs-with-pam-verhoff/). Many skilled testers are *not* certified and excluding them reduces the number of available applicants. When an open position doesn't get enough applicants, it becomes much harder to find a match.

Only hiring testers with testing certifications also increases the risk of groupthink, which is dangerous in testing. Many great testers have come into testing as a second career from a variety of backgrounds and those backgrounds often help them be better testers. 

Testing certifications are just one of many ways of seeing that someone is developing their skills. Any form of testing education (including certifications) on a resume might be taken as a positive signal. It may signal their desire to learn more and that they've had some kind of training - which might be useful, but might not. There are many other signs that a tester is developing their skills, though, such as leading on an aspect of testing, writing an article on a subject or taking courses on test automation. 

It's worth noting that most certifications do not prove that a tester can test and merely having the piece of paper tells you very little. Most testing certifications focus more on the visible artifacts produced by some testing processes and less on the core skills needed to function as a tester. Focusing on certifications can indicate that the tester over-appreciates knowledge while undervaluing skills.

During your hiring process, you still need to evaluate the tester's skills and abilities, regardless of whether they hold any certifications. This requires them to demonstrate actual testing and critical thinking skills, by asking them to test an application or come up with test ideas for example. A certification won't tell you how strong the candidate is in terms of valuable testing skills and attributes, such as analysis, curiosity, creativity, passion, ability to assess risk, working under pressure and empathising with their teammates.

You might also take the opportunity to nudge your candidates in the direction of good quality training education, such as the AST's well-regarded [Black Box Software Testing](https://associationforsoftwaretesting.org/bbst-black-box-software-testing-courses/) courses and the various [Rapid Software Testing](https://rapid-software-testing.com/rst-courses/) classes. 

<h4>For your annual review, I’ll need to see evidence of what you produced this year</h4>

As knowledge workers, it can be challenging for testers to demonstrate their achievements and provide evidence of their output at annual reviews. 

Testing is an information service on software quality that helps the team make more informed decisions. The process in your organisation might require you to produce evidence of the service you've provided, so you could show the information that was communicated to the rest of the team. This could be test summary reports that include what was tested, how it was tested and what was found out (including the most serious problems).

You could also provide test plans, bug reports, test strategy mind maps, test designs, test notes, risk assessments, emails, messages, minutes of meetings, code that you've written to extend your testing capabilities, review comments on documents and Jira tickets, and so on. You should be mindful that it can be hard to relate these types of evidence to the context in which they were produced, especially over such a long timeframe.

It is worth suggesting that the appraising manager ask your team members how valuable you were as a tester or what you were like to work with. If you've done your job well, they can give a first-hand account of how you've made a big difference through the communication of insightful, timely information.

You could suggest that, while outputs are important, questions about your approach to work, the outcomes of your work, and the satisfaction of customers with your work might also be interesting. For example, the knowledge and context that you bring to conversations about what we're building and how we're building it, the collaboration that you have with other members of the team on their work, the process improvements that you've initiated and so on are likely all evidence of a job well done.

It can be difficult to summarize a whole year of achievements and contributions to satisfy such a request, so consider asking your manager for opportunities to show your value in small increments on a regular basis rather than annually. You can show evidence of your contributions by providing outputs like the ones suggested above and also by gathering feedback from those you collaborate with.

If you're looking for prompts for recording your great work through the year in readiness for reviews, Julia Evans recommends writing a [brag document](https://jvns.ca/blog/brag-documents/)!


<h2 id="acknowledgements">Acknowledgements</h2>

<h3 id="the-association-for-software-testing">The Association for Software Testing</h3>

Our mission: _The [Association for Software Testing (AST)](https://www.associationforsoftwaretesting.org/) is dedicated to advancing the understanding of the science and practice of software testing according to Context-Driven principles._

We are an international non-profit professional association with members in over 50 countries. We strive to build a testing community that views the role of testing as skilled, relevant, and essential to the production of faster, better, and less expensive software products. We value a scientific approach to developing and evaluating techniques, processes, and tools. We believe that a self-aware, self-critical attitude is essential to understanding and assessing the impact of new ideas on the practice of testing.

<h3 id="contributors">Contributors</h3>

This book only exists thanks to the thoughtful contributions from the testing community. We thank the following individuals for their contributions to this book.

<h4>A</h4>
Olga Aksi, 
Hoang Ngoc Anh,
Emma Armstrong
<h4>B</h4>
James Bach, 
Jon Bach,
Andrew Bishop,
Michael Bolton,
Carol Brands
<h4>C</h4>
Andrew Clark,
Mario Colina, 
Caleb Crandall,
John Creson,
Stu Crock
<h4>D</h4>
Anders Dinsen, 
Mirek Dlugosz, 
Arun Kumar Dutta
<h4>E</h4>
<h4>F</h4>
João Farias, 
Ben Fellows,
Elizabeth Fiennes, 
Andres Flores,
Marius Francu
<h4>G</h4>
Matt Gilbert,
Ashley Graf,
David Greenlees
<h4>H</h4>
Jason Hamilton,
Mike Harris,
Peter Hawkins,
Andy Hird,
David Högberg,
Paul Holland
<h4>I</h4>
Sandro Ibig
<h4>J</h4>
Katharina Jaks, 
Klára Jánová,
Andrew January
<h4>K</h4>
Jonathan Kean,
Chris Kenst,
Rachel Kibler,
Tariq King,
Joel Kruse
<h4>L</h4>
Luke Liu,
Paul Lyles,
Petteri Lyytinen
<h4>M</h4>
Paul Maxwell-Walters,
Matt Middleton
<h4>N</h4>
Chris NeJame
<h4>O</h4>
Sophie Obomighie
<h4>P</h4>
Hussain Pardawalla,
Rahul Parwal, 
Linda Paustian,
Roman Podolyan,
Simon Prior,
Eric Proegler, 
Maaret Pyhäjärvi
<h4>Q</h4>
<h4>R</h4>
Venkat Ramakrishnan,
Bhavani Ramasubbu,
Alex de los Reyes,
Connor Roberts,
Heiki Roletsky,
Wayne Roseberry
<h4>S</h4>
Paul Seaman, 
Huib Schoots, 
Djuka Selendic,
Nicholas Snogren, 
Sebastian Stautz, 
Ady Stokes,
Karo Stoltzenburg, 
Scott Syme,
Damian Synadinos
<h4>T</h4>
James Thomas,
Frances Turnbull
<h4>U</h4>
<h4>V</h4>
<h4>W</h4>
Amit Wertheimer, 
Tim Western
<h4>X</h4>
<h4>Y</h4>
<h4>Z</h4>

<h3 id="licensing">Licensing</h3>

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.
