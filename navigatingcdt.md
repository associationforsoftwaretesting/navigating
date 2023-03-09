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

[Appendices](#appendices)
        
<h2 id="introduction">Introduction</h2>

_Navigating the World as a Context-Driven Tester_ provides responses to common questions and statements about testing from a context-driven perspective.

The book will be a particularly useful resource for those new to context-driven testing, akin to an FAQ for day-to-day situations and how to approach them. It will also serve as a reference guide, with answers linking out to broader and deeper information on each topic.

The book is coordinated and collated by testing practitioner and long-standing AST member Dr Lee Hawkins, using input from both AST members and the broader testing community via Twitter, LinkedIn, Slack and the AST mailing list. We are glad to provide an opportunity for testers to contribute to a useful reference piece and all contributions are [attributed](#contributors).

<h2 id="content">Responding to questions or statements around testing</h2>

<h3 id="testing">Testing</h3>

<h4>Developers can't find bugs in their own code</h4>

Developers can and do find bugs when coding. They not only find them in the code they are writing now, but also in code they wrote earlier, in their colleagues' code, and in the code of third-party libraries and applications they are using. 

It's worth noting that the developer is likely testing at layers lower than the tester. The developer might test something impossible to know about at any higher level. Something obvious from white box analysis could be a hidden, random guessing game from the perspective of a black box tester.

Developers - with their intimate knowledge of their own code - have hunches and concerns that can help testers find rich areas of concern to investigate - if the tester asks.

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

(See [Appendix A](#appendixa-1) for an alternative way to respond to the statement using the "Mary had a little lamb" heuristic from Gerald Weinberg.)

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

<h3 id="automation">Automation</h3>

<h4 id="letsjustautomate">Let's just automate the testing</h4>

While automation can be a valuable tool in testing, it can't replace the human.

A context-driven tester believes that good software testing is a challenging intellectual process. While there's often a great deal of scope for automating a path after it's been trodden, it takes intent and agency to find the paths worth following and the things to look for while walking along them. 

When people speak of "[automating the testing](https://www.developsense.com/blog/2017/04/deeper-testing-2-automating-the-testing/)", they're often talking about automating the typing, or the mouse clicks, or the looking up of results in a table, and comparing it to output from the product we're testing. But testing is far more than mashing keys and moving mice and looking stuff up. Tools can assist us with our testing in powerful ways, but testing cannot be automated.

A computer can check whether or not certain conditions are met, when programmed to do so, but only a human can make the judgment call on what checks are necessary, and when. Also, only a human can interpret the (meaning and significance of the) results, or the lack thereof, and decide whether or not we have a problem. Sometimes, a failing check, or a missing result, is the desired outcome even if, some other time, that exact same outcome would be a problem. A computer cannot make this distinction.

We need to be deliberate in our thinking about how automation can help us to test and also what makes sense to automate. Perhaps there is some repetitive confirmatory work that humans currently do that is time-consuming and boring and is amenable to being implemented in code - this seems plausible as a target for automation. We'd probably want to consider effort and value factors such as the costs associated with developing and maintaining the automation, the risks it would mitigate, and the potential multipliers that it could bring (such as documenting behaviour, and being runnable in different environments).

The diminutive "just" in the statement ("Let's just automate the testing") makes it seem like such a quick and easy thing to do, a casual activity that we can engage in that takes minimal effort. Implementing automated checks requires significant human effort and should be considered as software development work in its own right.

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

<h4>Stop saying "it depends" when I ask you a question</h4>

"It depends" is a truthful answer to many questions in any non-trivial context but, unfortunately, it's not usually a very helpful answer. Our aim, as context-driven testers, is to be truthful but also clarify how, why and on what our answer depends. 

By leading with "it depends", you flag to the questioner that they have not given sufficient information for you to provide a decent answer. You might follow with a clarifying question or two to refine your understanding of what information they are actually looking for or your analysis of what options are available. Take care when responding to a question with a question because, as you've doubtless found, many people in business have little patience for nuanced conversation. 

In composing an answer to the question, use your experience and the context to decide which variables matter to the questioner. You will need to make assumptions about how much time they have, how deep they want to go, and how much they care. All of this reasoning is necessarily imprecise because you don't know what their need is, or what they plan to do with your answer. 

Initiating your response with "it depends" is a way to indicate that you're thinking about contextual factors that will influence your answer. Following it with an appropriate summary of the perceived important variables and their potential consequences, while being ready to add depth or clarification, will signal that you are a valuable contributor and collaborator. As the context-driven principles say: people, working together, are the most important part of any project's context. 

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
Emma Armstrong
<h4>B</h4>
James Bach, 
Jon Bach,
Michael Bolton,
Carol Brands
<h4>C</h4>
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
Marius Francu
<h4>G</h4>
Matt Gilbert,
Ashley Graf,
David Greenlees
<h4>H</h4>
Jason Hamilton,
Mike Harris,
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
Joel Kruse
<h4>L</h4>
Luke Liu,
Petteri Lyytinen
<h4>M</h4>
Matt Middleton
<h4>N</h4>
Chris NeJame
<h4>O</h4>
<h4>P</h4>
Rahul Parwal, 
Roman Podolyan,
Simon Prior,
Eric Proegler, 
Maaret Pyhäjärvi
<h4>Q</h4>
<h4>R</h4>
Venkat Ramakrishnan,
Bhavani Ramasubbu,
Alex de los Reyes,
Heiki Roletsky,
Wayne Roseberry
<h4>S</h4>
Paul Seaman, 
Huib Schoots, 
Djuka Selendic,
Nicholas Snogren, 
Ady Stokes,
Karo Stoltzenburg, 
Scott Syme,
Damian Synadinos
<h4>T</h4>
James Thomas
<h4>U</h4>
<h4>V</h4>
<h4>W</h4>
Amit Wertheimer, 
Tim Western,
Frances White
<h4>X</h4>
<h4>Y</h4>
<h4>Z</h4>

<h3 id="licensing">Licensing</h3>

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

<h2 id="appendices">Appendices</h2>

<h3 id="appendixa">Appendix A - alternative answers</h3>

<h4 id="appendixa-1">We test to make sure it works</h4>

An alternative way to respond to the statement "We test to make sure it works" is to use the "Mary had a little lamb" heuristic from Gerald Weinberg and tie everything back to the [seven principles of context-driven testing](https://context-driven-testing.com/):

_"We"_

Testers, Developers, Analysts, and everyone else involved in making software perform tests - examining and investigating software to learn about it. Testing is an activity and sometimes a role, even for those who do not make it their profession. Those of us who do are typically working alongside people who are doing their own sensemaking, with different backgrounds, perspectives, and needs. People, working together, are the most important part of any project’s context.

_"Test"_

Investigating and assessing the software that was actually built, and comparing that to our models of what we think is needed.  Those models come from our general expectations about how software should look, feel, and behave, along with more specific expectations about what the software is going to be used for. Sometimes, these expectations are described explicitly, but even specifications can miss the mark. Often these expectations are not explicit (especially around dimensions of quality such as performance, security, usability, reliability, etc.) and we need to use our judgment and experience to evaluate what we're looking at. What are the expectations we bring into our testing? Where do they come from, who do they represent, and in what quantities and priorities should we balance overlapping expectations? Whose opinions matter? Whose opinions matter most? What tradeoffs are stakeholders willing to make? Good software testing is a challenging intellectual process.

_"to Make Sure"_

Testing is an information-gathering process. We share our findings, using our training to assign and communicate meaning and the context we believe is necessary to evaluate our findings. What the people guiding the project choose to do with the information that is gathered is a separate concern than the gathering and reporting of the information itself. The information gathered in testing on the state of the software and the project helps us make decisions with imperfect and incomplete information. There can be reducing amounts of uncertainty as more is learned and the team calibrates on standards and expectations, but there is no being sure. Projects unfold over time in ways that are often not predictable.

The people considering what they know about the software may decide that a reported problem is serious and needs to be fixed; or they might decide the reported problem is not serious and choose to ignore it. A software release could be made, delayed, sped up, or skipped. Sometimes, it is appropriate for us as testers to share our opinions about what decisions should be made, and sometimes we are asked to quietly leave our findings at the door. We should remember that we are typically the experts about quality on the project, and our opinions are neither trivial or unnecessary. Only through judgment and skill, exercised cooperatively throughout the entire project, are we able to do the right things at the right times to effectively test our products.

_"it Works"_

Software is never perfect. The question we are trying to answer is whether it is good enough to solve the problem it was created to address (and typically, other problems too). We might not need to deeply understand the subject matter the software is helping with to test it, but we do need to understand the expectations of the people who will live with it, and include our experience and judgment in our evaluation. The product is a solution. If the problem isn't solved, the product doesn't work.
