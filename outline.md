# Open Source 101: Create your first open source project the “right way” - Presentation Outline


## Slide 1 - Title Slide

* Good afternoon and welcome to "Create your first open source project the 'Right Way'."


## Slide 2 - Not An Expert

* Before we get too far into the presentation I need to make clear that I am not an expert in doing open source the 'Right Way.'


## Slide 3 - I Am A Fan!

* I am however a big fan!

* I have been working in and around open source since roughly 2010. 

* My fandom started out as a consumer of open source projects that helped me cobble together slightly useful applications that I was fortunate to get paid for.

* In 2012 I was part of a team that created an open source platform for document analysis called Infinit.e. It was surprising how exciting it was to release all of that that code into to the wild.

* Finally, in 2014, my career moved into a phase that involved selling open source. And yes, you can actually give away and sell open source software although the selling part can be more challenging than creating the software in the first place.

*  So for the last seven years I have made my living out of a combination of using, writing, and selling open source software...


## Slide 4 - Opinions

* That is to say that everything I say in this presentation is just a collection of my opinions and we all know what they say about opinions.


## Slide 5 - How Not Why

* So what we are going to talk about now is HOW to create an open source project not WHY.

* There are quite a few reasons WHY you might create an open source project but those are beyond the scope of this talk and some might argue better discussed with the aid of adult beverages.

* What I want to focus on is some of the things that you can do once you have decided to create an open source project to make it something other developers might actually want to use.


## Slide 6 - "The Golden Rule"

* Let's start with an agreement that as open source developers we should all strive to follow the golden rule: "Release onto others as you would have them release onto you."

* In other words, create your open source project the way that you would want other developers to create their open source projects if you were going to use them.

* Unfortunately this golden rule doesn't really mean that you will end up profiting from your work...


## Slide 7 - Sad Face

* Or that others will follow the golden rule.

* If you have tried using other people's open source projects you might have felt like this.

* I have spent a lot of time metaphorically weeping while searching through open source projects to find something useful.

* So how do you avoid bringing other developers to tears?


## Slide 8 - Todo List

* I have developed my own personal 8 point to do list that I strive to follow when I create a new project.

* This is by no means a comprehensive list of everything you can or should do to create a successful project, rather I think it sort of the bare minimum of things you can do to get started down the right path.

* So what are the 8 things? Hopefully most them are pretty obvious like: picking the right license, putting your code somewhere people can find it, and documenting your code well.

* Some of the other items might be a little less obvious like: documenting bugs and enhancements, including unit tests in your code, having "official" code releases, and asking for and gratefully taking help.


## Slide 9 - choosealicense.com

* If you are going to open source your project one of the first things that you will want to do is a pick a license under which to open source it.

* I tend to stick with the Apache 2.0 license because that's what I have the most experience with.

* That said I am not an expert on which license you should should choose so I highly recommend that you do some research.

* One great resource that makes it really simple to pick a license is choosealicense.com. If you aren't already familiar with it I highly recommend taking a look.


## Slide 10 - Github

* Let's be honest there are only a few places where you would choose to host your open source project and Github is the 900 pound Gorilla in the room.

* If you really want to look at alternatives there are options out there like Bitbucket,  Microsoft's Codeplex, and Slashdot Media's SourceForge (which itself used to be the 900 pound Gorilla). 

* I should note however that even Microsoft hosts its important open source projects on Gitbhub...

* The thing to remember about where to host your open source project is that it isn't just a place to dump your code so that other people can access it. Whatever host you pick should at least have features like support for your favorite source code control tool (git), a place to capture issues (more on that later), wikis and documentation (which we are going to talk about next).


## Slide 11 - Documentation

* One of my biggest pet peeves with a large number of open source projects is no, or lousy, documentation.

* You've probably heard, or even said, something like "this code is self documenting."

* Whether or not your code is self documenting, making people read through your code to figure out if it might be useful to them isn't the way to get people to use it.

* Which isn't to say that you need to write a novel.


## Slide 12 - What Is It?

* In fact, if you can answer the question the questions "what is it?" and "how do you use it?" you are off to a great start.

* "What is it" seems pretty obvious right? 

* Need an example? Here is the one sentence introduction for one of my open source projects:

	"A basic JDBC driver for Basho's open source Riak TS (Time Series) database"

* Hopefully you will agree that the description is succinct and clear and leaves little to the imagination.

* "How do you use it" might require a little more effort but is also quite important.

* Depending on the type of project you will want to provide your end users with some minimal level instruction on its usage including:

	* How to build the project or where to get pre-compiled binaries 

	* Clear, simple code examples showing how to use your project

* One of the important things I want to impress upon you on the topic of documentation is to not fall into the trap of thinking, "that's obvious so there's no reason for me to even say it..." 

* Instead strive to make your work accessible, through the use of clear, concise documentation.


## Slide 13 - Issues

* The need to document your project doesn't end once you open source it.

* Beyond the obvious need to keep your documentation updated whenever you update your code, a healthy open source project will also collect more transient documentation for things like bugs, ideas for enhancements, or requests for help.

* If you use Github this type of documentation get lumped under the header of Issues. 


## Slide 14 - Bugs

* Your code has bugs. Don't be ashamed. Embrace the bugs. Document the bugs.

* You will find bugs in your code and be tempted to just fix the code and commit the fixes. Don't do it!

* Document the bugs before start correcting them. What are the steps required to recreate the bug and what kind of error message, if any, is generated? Where in your code is the bug hiding and how do you plan on fixing it?

* When the bug is documented sufficiently go ahead and fix it but don't forget to reference the bug when you commit the fix to your repository (and close the bug report of course). The combination of bug reports and commits will create additional history that can come in handy later when you are trying to figure out why you made different choices within your code.

* And, who knows, maybe you will post a bug and one of the thousands of users of your project will jump in with a fix!


## Slide 15 - Enhancements or Ideas

* Not everything labeled as an issue is a bad thing.

* You can and should use issues as a way to think "out loud" about ways to improve your project especially if you want to get input from your community.

* The most common way to think out loud is to propose enhancements.

* I also like to think about enhancements as bugs you haven't written yet. Don't write the code before you write the documentation!


## Slide 16 - Tests

* Still think that good code is the best form of documentation?

* How many people in the room make writing unit tests an integral part of their coding process?

* If you are going to release software as open source then unit tests should be a part of your process.

* Unit tests serve a couple of key functions:

	* First, if you follow a test driven methodology than your tests serve as a highly practical form of requirements to focus your development efforts.

	* Second, after you have implemented the functionality covered by the tests you can implement new features in your software confidently knowing that your unit tests will alert you to any changes that break existing functionality.

	* And finally, units tests really do serve as a form of documentation in that they demonstrate all of the various ways that you can interact with the software.

* Do everyone a favor and write your unit tests!


## Slide 17 - Releases

* Ok, so at this point we have code that we have written (with unit tests), released with an open source license, hosted someplace like Github with enough documentation that would allow people to figure out how to use it. What do we do next?

* We release it!

* And just to be clear, in this instance when I say release what I mean is to take a snapshot of your code (and any binaries, documentation, etc.) at a given point of time, slap a version number on it, and call it a release.

* Even if your project is nothing more than a single script it makes sense to deliver releases.

* Releases, theoretically, give your users stable check points, versions of your code with documented features and bugs (of course). 

* Releases are also a great way to record the history and progress of your project over time so don't forget the release notes!

* One of my favorite software development sayings is "Release early and release often."


## Slide 18 - Ask For Help

* Quite a few open source project maintainers never bother to ask for help. Maybe they don't want it?

* I am going to assume that most of the folks in this room feel that community is an important part of the open source movement.

* Community can mean different things to different people. 

* For me, in terms of open sourcing code I write, I find community to be:

	* A motivation to write better code;

	* A resource for learning to be better developer;

	* And a way to give back to the larger community that has helped me grow in my career.

* So when I release something as open source I always explicitly ask for help because I want to encourage community.

* If you want help, ask for it.


## Slide 19 - Accept Help

* Of course if you are going to ask for help you should also be willing to accept help when people offer it.

* Right now you might be thinking "well duh!"

* Accepting help seems like such an obvious thing to do but unfortunately plenty of maintainers of open source projects only pay lip service to community and don't really include contributions from the community.

* My thoughts on your basic responsibility to your community as an open source maintainer can be summed up as:

	* If someone cares enough about your project to submit a bug, feature request, question, or a pull request, you owe it to them to (at a minimum) to craft a friendly response.

	* If you can merge a pull request do it! That is if a merge request fixes a bug or adds a new useful feature

	* If you can't keep up with your community think about promoting one or more community members to a position of within your repository where they can help you OR, if you are ready to let go you can transfer the project to someone else in its entirety.


## Slide 20 - Contact Information 

* And that's it! Everything you need to do to create your first open source project the "right way."
