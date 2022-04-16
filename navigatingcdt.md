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

<h4>We test to make sure it works</h4>

We test to learn and make sure we understand how it works, and for whom; and how it doesn't work, and for whom.

To get to an understanding of what "works" means for a particular piece of software, we start with testing to explore and mentally model it. As we learn more and come to an agreement with stakeholders about what it means for the software to be working, we must still be mindful that any certainty we’ve gained is limited to the types and variety of testing and experimenting we've performed. We can still be fooled – there may be dependency on variables that we might not even be aware of, it might appear to work for us but might not to the customer (and vice versa), or we may have failed to consider particular types of user.

So, when we test the software, we might explore who is likely to be using it, the things they might use it for, and what they would hope to get from it. It’s also worth finding out why we built this particular solution, what else we tried, and why the others were rejected. Through collaboration we are uncovering what "it works" means for different users (and stakeholders), situations, in relation to the purpose and intent of the product. All of these different components of the context of the software help us to test whether it gives the required value to the people who matter and also what risks it poses to these people.

With context in mind, we strive to understand what the software does well enough to tell the team making it enough that they can determine what could be changed to align with the intent. Our understanding also should enable us to tell the stakeholders enough that they can determine if what it does is sufficient to be deliverable.

We also need to be interested in whether the product does things that we don't intend it to, or that users expressly do not want, and what the effects of those things might be. In this sense, we also consciously test to find out how it might _not_ work.

No level of testing can provide certainty that the software works, so our understanding of perceived risks and threats to the value of the software drive our prioritization of what to test and to what degree. As we explore, our assessment of risk may well change in light of new information too.

(See [Appendix A](#appendixa-1) for an alternative way to respond to the statement using the "Mary had a little lamb" heuristic from Gerald Weinberg.)

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

<h4>Stop saying "it depends" when I ask you a question</h4>

"It depends" is a truthful answer to many questions in any non-trivial context but, unfortunately, it's not usually a very helpful answer. Our aim, as context-driven testers, is to be truthful but also clarify how, why and on what our answer depends. 

By leading with "it depends", you flag to the questioner that they have not given sufficient information for you to provide a decent answer. You might follow with a clarifying question or two to refine your understanding of what information they are actually looking for or your analysis of what options are available. Take care when responding to a question with a question because, as you've doubtless found, many people in business have little patience for nuanced conversation. 

In composing an answer to the question, use your experience and the context to decide which variables matter to the questioner. You will need to make assumptions about how much time they have, how deep they want to go, and how much they care. All of this reasoning is necessarily imprecise because you don't know what their need is, or what they plan to do with your answer. 

Initiating your response with "it depends" is a way to indicate that you're thinking about contextual factors that will influence your answer. Following it with an appropriate summary of the perceived important variables and their potential consequences, while being ready to add depth or clarification, will signal that you are a valuable contributor and collaborator. As the context-driven principles say: people, working together, are the most important part of any project's context. 

<h3 id="testing-status">Testing Status</h3>

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
John Creson
<h4>D</h4>
Anders Dinsen, 
Arun Kumar Dutta
<h4>E</h4>
<h4>F</h4>
João Farias, 
Ben Fellows,
Elizabeth Fiennes, 
Marius Francu
<h4>G</h4>
Ashley Graf,
David Greenlees
<h4>H</h4>
Andy Hird,
David Högberg,
Paul Holland
<h4>I</h4>
Sandro Ibig
<h4>J</h4>
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
Eric Proegler, 
Maaret Pyhäjärvi
<h4>Q</h4>
<h4>R</h4>
Bhavani Ramasubbu,
Alex de los Reyes,
Wayne Roseberry
<h4>S</h4>
Paul Seaman, 
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
