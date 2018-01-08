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


6. Can you write a palindrome function?
- this exercise pure JS
- familiar c a palindrome?
- build a func that returns true or false depending if string is a palindrome
- response:
	- first clarifies, "how detailed do you want the JavaScript to be?", pseudocode ok to start but need to work to JS
	- ok, I would like to start c pseudocode to tell you my thinking process
	- so it's a function is_palindrome(str) {}
	- palindrome is we have a string backwds or fwds same way, like "gog"
		- so if I reverse it it's the same
		- so I need to figure out how to reverse this str in the func
	function is_palindrome(str) {
		var rev_str = reverse_str(str);
		if (str === rev_str) {
			return true;
		} else {
			return false;
		}
	}
	- obviously I need to figure out the reverse_str function
	- so I'd write that as a separate function on top
	function reverse_str(str) {
	}
	- now correct me if I'm wrong but there's no native way to reverse a string?
		INTERVIEWER:
		- actually, there is a native method, so kill of the call and do str.reverse()
		- that's something you would look up anyway in documentation so...
		- points to "gog" this is your test case, let me introduce another: "Go.g"
		- we want to ignore punctuation and case sensitivity
		- does your current solution meet that?
	- no
		- how would you change it?
	- I would rename my reverse method to reversing cleanup
	- I'll keep this whole logic but then go back up and figure how to get rid of punctuation
	- the first step is to reverse the string
	- need "to look up the exact definition" for string to lowercase
	function rev_cleanup(str) {
		rev_str = str.reverse();
		rev_str = rev_str.toLowerCase();
	}
	- now I need to go and write out these test cases to figure out punctuation
	- puncts: ? . , ; : " ' `
	- now can I assume I just have alpha chars? Can there be numbers as well?
		- no numbers just alpha
	- I would use regular expressions; I would have to look this up; I'll do a-z
	- then I'll need some re.match
	- I'll use reg expressions and find the ones that don't belong to a-z because just looking for all instances of those characters
	INTERVIEWER:
		- I see a potential for a bug here: you're using a var statement down here (main method) but not up here (first line top method)
	- that var statement is actually crucial so I would correct my statement
	- that will guarantee that I'm creating a local variable
		- without that what happens?
			- first try to access any global variables and if not create the global variable
	INTERVIEWER: these functions here will iterate over the entire string every single time, not most efficient
		- regex is correct
		- then just check forwards and backwards, then you're iterating over the str just one time

- My rating: 5
	
	"The candidate spent time going back and forth with the interviewer during the coding process. The candidate could have clarified the problem in advance and fleshed out test cases before building to anticipate some of the interviewer's concerns. This was an interesting example to watch, and the candidate showed off both prior knowledge, honestly stated weaknesses and conveyed ability and comfort with learning more."


7. What is a closure? When whould you use one?
- Are you familiar? Yes. Explain what it is and what are the advantages?
- response:
	- goes back to pointers and pointer references
	- whenever we create a variable, so like var m = 8, it's a pointer to an 8 somewhere in memory space
	- an array holds a reference to the vars inside, like if [m] is my first it's 8
	- so if this pointer starts pointing to a difft num like if I'm looping
		- say I'm looping through to create anonym funcs that will hold a certain variable
		- if I console log here they're all going to equal 10
	var arr = [];
	for (i=0; i<10; i++) {
		arr.push(function() {console.log(i);});
	}
	arr[0];		// 10
	- this bc at the end of my for loop the i will point to 10
	- what I want is for every number to be closed in a variable, so I need a closure, it closes that variable
	function my_func(num) {}
	- as soon as I do this in JS it creates a closure
	- it creates its own space, scoped inside there
	- I could do whatever with num and not have to worry about this num changing
	- otherwise I'm not creating a closure I'm just referencing i here, and i will change in the future
	- so anonym funcs that I want to pass in vars I want to get the value and not just the reference to the value
	- in JS we want to do AJAX requests and closures important
- Interviewer:
	- let me understand where you're going here
	- let's say I have a function rate(), purpose to call a function that's safe to call based on some rate limiting API
		- can only call this API certain number of times per minute
		- make sure we're always returning a safe-to-call function
		function rate () {
			var time = 0;
			return function() {
				time += 50;
				// logic to determine call
				console.log(time);
			}
		}
		var limiter = rate;
		limiter();
		limiter();
		- run me through what's happening in the output
- Answer:
	- so you're calling rate, and time is local in rate scope
	- basically all anon funcs created will share the same time var
	- if a difft func changes time then time will change as well
	- at first time is 0
	- now I call this (pointing to limiter) and time equals 50
	- once I call this (again) time is going to equal 100
	- INTERVIEWER: so is this (pointing to anonym func first line) changing global var time or local var time?
	- ANSWER: it's changing this variable (local) time
- So talking about closures in general, it's a way of maintaining state. What's a downfall of maintaining state?
	- you have a ton of different vars to keep track of
	- time is not one var, each time you run you create new time variables
	- they reside in memory, we can have memory leaks when we have all these mem states not referenced
	- so we have all this garbage
	- can't be collected because JS thinks it's still being used so it can't be GC 

My rating: 3

	"The candidate presented an example of a scenario that captured an case where closures are important, followed through with the example and explained even more than was asked. The candidate showed knowledge of grappling with closures in the past, and showed an ability to apply knowledge from trouble spots in writing code to the general question. The candidate did start out skirting the topic rather than defining closures directly, speaking more about pointers and reference. When discussing key concepts, the candidate introduced terms like "scope" by saying "it's scoped inside there" rather than walking to an understanding of what scope is and why closures matter. Setting up a specific case was a great idea, but it would help to explore the problem domain first, or to explore this one case as indicative of a problem in search of a solution, working towards a practical definition of "closure" from there."


8. What's a problem you had and how did you deal with it?
- I've been learning Python and backend
- I wanted to create a website that has db of pics and make API endpoint to serve it
- first, how do I make an API endpoint
- I know to send off a request to an API server and get the JSON, now how the other side works
- steps:
	- get my query params
	- how to access my db?
	- that db stuff was tough, lots of Stack Overflow example code
	- how would I access this db?
	- people recommended using own data store system like an ORM, an object relational mapping system
	- that's my first time using an ORM because I'm used to running SQL commands
	- so I need to understand how to access this object, it was confusing for me
	- so I watched vids and read example code
	- once I figured that out went back to my project
	- now needed translate btwn Python dict, similar in structure, to JSON
	- last, how do I output that?
	- Stack Overflow, oh, you need to write some headers and tell the type of content you're returning
	- then I have my JSON library, so convert my dict to JSON and use normal func to output that
- that's my whole story, took figuring out all these other things step by step, focus on these small little tasks

My rating: 5

	"The candidate explained a task he was attempting for the first time, then walked through a linear account of making progress. The candidate showed a strong ability to think decompositionally, to resolve errors or unknowns through learning and improving, and gave strong indications of being able to think this way about future problems."


9. Mike's analysis of the interview
- interview candidate did "pretty well"
- asked clarifying questions
	- really trying to understand the problem
	- often interviewer has idea of where wants candidate to go
	- BUT it's candidate's responsibility to ask those questions to get self there
- took feedback and tried it out
- more whiteboard practice would've helped
	- start at top L to have plenty of room to write
	- leave space between lines to fill in later rather than closing out syntax, erasing, rewriting
	- don't close tags until you're done
- teach me in 5 mins really likes
	- constantly having to teach fellow engineers
	- this is an important part of the job you'll do numerous times per day
- what interested abt web dev
	- this is a q abt passion and drive
	- constant change so need candidates staying on cutting edge
	- someone who will stay educated
- palindrome as pretty typical q
	- interviewer not interested in whether you can solve
	- they want to see if you think like a programmer
	- can you understand the basic syntax of the language being used?
- img carousel q as another basic
	- simple q get used to writing on the board
	- trying to see if thinking like dev in role
- closure is one q testing candidate's understanding of language
	- does candidate know what's going on when writing code?
- technical challenge and how solved
	- cool-down q coming off of whiteboard
	- understand how candidate challenged self
	- how did candidate get through complicated prob s giving up
- tone
	- good but too fast
	- think abt response to q before answering
	- candidate went on and on a bit s wrapping up

(10. Career Portal Resources again)



11. Project: Interview Practice
Rubric: https://review.udacity.com/#!/rubrics/77/view
Checklist: https://docs.google.com/document/d/1Wv0ZRcKD-ojtC-JxRLh3ZhJT2ONHh3kJWQX9T7w_8vo/pub?embedded=true

- find a job position: https://career-resource-center.udacity.com/job-boards
- answer interview qs below as if doing them in interview
- copy and paste test of job posting in "Notes to reviewer"
- submit answ as pdf, txt, ...

	1. What is the most influential book or blog post you’ve read regarding front-end development?

	2. If you could master one technology this year, what would it be and why?

	3. Describe any front-end web application framework (preferably one that you use). How does it work? What are the upsides and downsides?

	4. Write a JavaScript function that takes only one argument——another function——and returns a "memoized" version of that function. A "memoized" version of a function caches and returns the results of its call so that when it is called again with the same input, it doesn’t run its computation but instead returns the results from cache. Note that previous results should be retrievable in any order without re-computation.

	*Feel free to include your own example use, input, and output (like what is seen below).*

	```
	foo = function (x) {
		console.log("calculating!");
		return x + 5;
	}

	var memoizedFoo = memoize(foo);

	memoizedFoo(5);
	// calculating!
	// 10

	memoizedFoo(5);
	// 10 (notice how 'calculating!' is not printed this time)

	memoizedFoo(10);
	// calculating!
	// 15
	```

	5. Create a simple webpage that has a cow image in the middle (centered horizontally on the page) and a counter label below it. Add the necessary code so that every time you click the cow image, the counter is incremented by 1. The counter should start with a value of 0. You should include a brief explanation of your code. Also, here is a URL for a cow image, https://upload.wikimedia.org/wikipedia/commons/2/21/Cow_cartoon_04.svg, if you would like to include it in your answer.

	6. If you were to start your front-end position today, what would be your goals a year from now?
