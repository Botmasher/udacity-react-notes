Project: Interview Practice (Front-End)

1. Intro
- (first start c the behavioral interview-questions.md)
- this time it'll be a mix of behavioral and technical qs

2. What got you interested in web development?
- grew up c internet
- one of first experiences c internet logging onto AOL
- magical seeing features and parts of browser in AOL
- thought it would be great way to build cool things
- following walkthroughs to build AngelFire site
	- like little website for game he made

- My rating: 3 satisfactory
	"The candidate related personal growth in understanding of the internet throughout life, sharing relevant stories from early experience with web development. The candidate could have made this stronger with more concrete examples. The desire for impact could've been more specific: whose kids does he want to help and how?"

3. What about new web dev excites you?
- one is web components
	- when learning HTML4, HTML5, felt had to reinvent all these little components
	- thought it'd be great if in programming langs could take fleshed-out component and add it onto site?
	- wants to concentrate on making own app and not these little things
	- nuisances:
		- make sure the JS is working fine
		- make sure the backend is communicating fine
	- exciting: empowers future users to make things quicker, faster, and make things better for users
- asked: browsers aren't quite there yet, so have you played with this at all?
	- not so much right now
	- just excited about what's coming about
	- looking at Google IO and Palmer and thought it looks really cool
	- hard to do it for real project bc need to support other browsers besides Chrome c this implementation

- My rating: 4
	"The candidate outlined a problem then presented a new technology that promises to address it. The candidate was excited and clearly knew where to start tinkering and playing with the solution. The candidate showed strong willingness to learn new things. However, there was a reluctance to take action, because of difficulty to integrate into existing projects. The candidate could show strength by choosing some new tech already played with." 

4. Teach me something in 5 minutes (you're allowed to ask what I don't know or whether I'm interested, but then go against the clock)
- It doesn't have to be technical? Oh, great!
- can use the whiteboard too
- Let me teach you about drumming.
- used to play taiko
- talks about history and origin of Taiko in Japan
	- draws quick blob of Japan and a circle for Taiko that he explains is a "huge drum"
	- stick figure striking drum c sticks called "bachi"
	- that's the main form of musicality in taiko
	- the origins go back 1000s of yrs, communal: harvest season play drum and wish gods bring rain, or during war, pray to gods
	- Susanoo thunder god, you play like going all out in hot summer weather to wish good health; harder you play better chance success
- that's the origin in a nutshell (now we have < 2 mins left)
- going into N Am, transferred over into San Francisco by Tanaka Sensei in 1970s, no 1960s actually
	- since lacked drum to bring people good luck and pull commty started own taiko group
	- for next 40 years other groups popped up: SF, San Jose, another popped up in Buddhist group in LA
	- that was over span of 2 yrs then it went viral

	- My rating: 3
	"The candidate clearly demonstrated the history of Taiko from its origins in Japan to its present practice in the US - on the spot! The candidate showed enthusiasm and flexibility. The candidate used illustrations to make the progress even clearer. The candidate could've been more specific about the topic upfront to avoid setting expectations of learning to drum ("let me teach you about the history of Taiko"). The candidate could've leaned more directly on the learner's prior experiences, presenting the topic with either an engaging cold open or a warmer question to prick audience interest."

5. Can you build me a carousel?
- get started on some tech qs
- describes img carousel: cycling L or R thru 5 imgs
- just the HTML you would use to build this out?
- response
	- first I want all my vars and constraints right
	- reiterates the task: I need carousel, pics that show up, L to R
	- separates out section that's visible as a box: I need to define that box first
	- quickly settles on a syntax: I'm going to use semantic tags
	<section class="carousel">
	</section>
	- then we'll define this
		- I'm going to need buttons
		- stops, erases, makes more space
		- add span for button
		- says assume we'll style this in the CSS later
		- within bttns wants the main pic
	<section class="carousel">
		<span class="button-left"></span>
			<img class="carousel-main-pic">
		<span class="button-right"></span>
	</section>
	- to set up these would have some JS that would load
	<section class="carousel">
		<span class="button-left"></span>
			<img class="carousel-main-pic">
		<span class="button-right"></span>
		(JavaScript to preload these imgs)
	</section>
	- if I click on this button would the img animate and shift?
		- we're not worried about animations, just that L img would go away and this pic would be in its place
		- we'll say it moves this way bc semantically and structurally that's what would happen
		- you would have imgs out of view or in view
	- thanks for clarification
	- then begins to whiteboard out tags for offscreen imgs
		- explains that later CSS will take these imgs off the field
	<section class="carousel">
		<span class="button-left"></span>
			<img class="carousel-off-left">
			<img class="carousel-main-pic">
			<img class="carousel-off-right">
		<span class="button-right"></span>
	</section>
	- then stars the ones that will show up in the viewport
	<section class="carousel">
		* <span class="button-left"></span>
			 <img class="carousel-off-left">
			 <img class="carousel-main-pic">
			* <img class="carousel-off-right">
		* <span class="button-right"></span>
	</section>

- a few questions from interviewer
	- Q: you said these are buttons but used span tag; any negative consequences to that as opposed to anchor/btn?
	- A: neg conseq is that span takes up space, but that space will be guided by the bg img I give it
	- Q: let's assume user doesn't have mouse
	- A: ok yeah accessibility. You're right. I would actually change my span tag to an anchor tag.

- My rating: 5
	- The candidate stopped to define and understand the problem space before jumping in.
	- The candidate explicitly settled on a syntax before starting to whiteboard the problem.
	- The candidate asked for help or clarification, appreciated feedback and then implemented changes.
	- The candidate did a good job taking criticism and pivoting on the spot. 
