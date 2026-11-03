# 🎮 SNACK DEFENDER: DOBBY'S RUSH 🐶🦝🐥🐿️
yana’s first solo project<br>
for my precious little corgi who takes his snacks very seriously ♡<br>
<br>
<img src="assets/dobby.jpeg" alt="dobby" width="350"><br>
<br>
DRAFT<br>
*will update this properly once the game is actually done<br>*
<br>
<br>
<b>inspiration</b><br>
dobby obviously. bc he’s my baby and i love him more than anything on earth.<br>
<br>
i originally came up with this idea for my fundamentals of interaction design assignment about a year ago? it was a conceptual arcade machine with bone shaped hammers, motion sensitive gloves and animals popping out of bushes. my tutor said the game design was really interesting. i randomly remembered the assignment while planning this project and thought why don’t i actually make this???<br>
<br>
so this is my attempt at turning that arcade concept into a little browser game people can play on their pcs or phones.<br>
<br>
<br>
<b>idea</b><br>
a tiny cute project as a little warmup to get back into coding before jumping into bigger projects over summer break.<br>
something small enough to finish quickly & fun that i actually feel happy working on.<br>
can personalize ofc featuring dobby bc why not???<br>
give me some programming logic to practice.<br>
<br>
*est. time: around 5 days for the first version depending on how much time i spend debugging & making dobby look cute (very important) lol<br>*
<br>
<br>
<b>concept / plot</b><br>
dobby has collected his favorite snacks and is having a perfectly nice day until some sneaky raccoons decide they want a share.<br>
um.. excuse me????? absolutely unacceptable.<br>
help dobby protect his snacks by bopping the raccoons when they pop out of the bushes. sometimes a squirrel or duck appears too. so pay attention cuz those are friends.<br>
score as many points as possible before the round ends.<br>
<br>
<br>
<b>physical arcade machine to online game</b><br>
\- hammers -> clicking or tapping animals<br>
\- popup holes -> illustrated bushes<br>
\- pressure sensors -> code checking which animal the player clicked<br>
\- LED indicators -> icons and visual effects<br>
\- paw shaped start button -> clickable/tappable paw button bc that stays<br>
\- dobby’s reactions -> switching between images based on what happens<br>
~~\- motion gloves -> idk this just wouldn’t transfer directly.. maybe measure response time and fast acurate consecutive hits could earn a combo bonus<br>~~
<br>
<br>
**first version**<br>
*will focus on the basic tapping game. simple and manageable with room for other stuff later<br>*
<br>
1\. start screen<br>
\- game title, dobby saying “protect my snacks”<br>
\- paw shaped start button<br>
\- short instructions showing the raccoon and forest animal friends<br>
<br>
2. playing screen<br>
\- six bushes<br>
\- one animal appears at a time in a random bush<br>
\- animals stay visible briefly then disappear<br>
\- raccoons appear more often than animal friends<br>
\- one fixed speed to start with<br>
<br>
3. basic game logic<br>
\- 30 second round<br>
\- raccoon hit: +10 points and happy dobby<br>
\- duck/squirrel hit: -5 points but score stays at zero or above<br>
\- missed raccoon: no points<br>
\- duck/squirrel left alone: no points or penalty. good job minding ur business dobs lol<br>
\- tapping an empty bush: nothing happens<br>
\- each animal can only be scored once<br>
these are starting values. i’ll adjust them if the game feels too easy, too fast or annoying.<br>
<br>
4. dobby’s reactions<br>
\- normal / watching<br>
\- happy after a raccoon hit<br>
\- sad after hitting a friend<br>
\- short messages like “woof woof!” and “oops that was a friend”<br>
<br>
5. end screen<br>
\- final score<br>
\- a message from dobby<br>
\- play again button<br>
<br>
6. restart<br>
\- reset the score, timer, animals and dobby’s expression properly<br>
\- starting a new game should actually start a new game<br>
<br>
<br>
**extras for later**<br>
\- easy / normal / hard modes<br>
\- combo counter and bonus points<br>
\- multiple animals appearing at once<br>
\- saved personal best<br>
\- more expressions and character animations<br>
\- sound effects, background music and sound controls<br>
\- extra locations (beach, park, etc.) or different snack collections<br>
sounds can wait until the basic game works<br>
<br>
<br>
**skills / tech stack**<br>
html, css, javascript only. no overcomplication. bc it’s meant to be fun not give me headaches.<br>
<br>
html<br>
\- organizing the start, game, end screens<br>
\- buttons, images, score and timer text<br>
\- using proper buttons so keyboard interaction works too<br>
<br>
css<br>
\- grid layout for the bushes<br>
\- positioning animals inside each bush<br>
\- showing and hiding different states<br>
\- making the layout fit both desktop and phone screens<br>
\- simple visual feedback when something gets hit<br>

javascript<br>
\- arrays and objects for the animal types<br>
\- functions for starting, spawning, scoring & ending a round<br>
\- random numbers to choose animals and bushes<br>
\- conditions to decide whether a target is a raccoon or friend<br>
\- click events<br>
\- timers and cancelling timers<br>
\- updating text, images and classes on the page<br>
\- keeping track of game state<br>
<br>
<br>
**programming logic**<br>
the basic round: start game → reset everything → show an animal → player hits it or it disappears → show the next animal → stop when time runs out.<br>
<br>
things the game needs to remember<br>
\- on the start screen, playing or finished?<br>
\- current score<br>
\- when the round should end<br>
\- which bush is active<br>
\- which animal is there<br>
\- the animal’s already been hit?<br>
\- which timers are currently running<br>
<br>
when someone taps a bush<br>
1\) check the game is still running<br>
2\) check there’s an active animal there<br>
3\) check it hasn’t already been hit<br>
4\) mark it as handled immediately<br>
5\) update the score and dobby’s reaction<br>
6\) remove the animal and continue the round<br>
i’ll keep this information in javascript and update the screen from it<br>
<br>
<br>
**tricky parts**<br>
keeping the game’s state correct!!! (what if someone clicks too quickly or restarts midway..?)<br>
movement and timing.. ughhh will probs need to actually play it and adjust<br>
double tapping (one raccoon giving unlimited points)<br>
artwork & phone layout (bushes need to be big enough to tap & spaced out enough to avoid accidental hits)<br>
handling timers (overlapping after a restart, countdown accuracy. how to calculate remaining time from an actual end time?)<br>
and more.....<br>
<br>
<br>
**ui design**<br>
\- bright colorful cute little garden arcade<br>
\- sky blue background, green bushes and grass<br>
\- dobby and his snack beside the playing area<br>
\- score and timer clearly visible at the top<br>
\- 6 bushes arranged in a grid<br>
leaning towards simple cartoon illustrations to match my original concept. raccoons and friends should look clearly different!! should be easy for players to understand the game. might just use simple static images for the first version cuz the personality can come from dobby’s expressions and messages anyway.<br>
<br>
<br>
**realistic 5 day plan**<br>
day 1 setup + basic layout<br>
\- create project folder and files<br>
\- sketch where the screens, bushes, dobby will go<br>
\- build the score, timer, 6 bush layout<br>
\- make one test animal appear & clicking it change the score once<br>
*goal: can click one animal and see the correct response<br>*
<br>
day 2 make the main game loop work<br>
\- choose a random bush and animal<br>
\- make animals appear and disappear repeatedly<br>
\- handle raccoon hits and animal friend mistakes<br>
\- stop repeated clicks from scoring twice<br>
\- add basic dobby messages<br>
\- check that each appearance only finishes once<br>
*goal: animals keep appearing and the scoring rules work<br>*
<br>
day 3 complete the game logic & prototype<br>
\- add the 30 second round, start and end screens<br>
\- stop everything when the round ends<br>
\- show the final score<br>
\- implement restart (reset timer and everything!!!)<br>
\- test rapid clicking, missed animals, restarting midway<br>
*goal: can start, finish and replay a complete round<br>*
<br>
day 4 polish ui + decor + make it feel like dobby’s game<br>
\- add character images and expressions<br>
\- style the garden, buttons, bushes, etcetc<br>
\- check keyboard focus and instructions<br>
\- play a few rounds and adjust the speed & layout for phones & add feedback for hits<br>
*goal: the game looks clear and cute & feels comfortable to play<br>*
<br>
day 5 test + finish<br>
\- test on my pc & phone<br>
\- make someone play without me explaining & take a moment to appreciate how cute dobby is, ask for feedback<br>
\- fix confusing behavior or bugs if theres any<br>
\- write a proper readme with screenshots, what actually works, reflection, future improvements, etcetc.<br>
\- put the finished first version on github yayyy<br>
*goal: someone else can play the game without getting stuck<br>*
<br>
<br>
<br>
\*** if i run out of time ***<br>
<br>
keep the artwork simple and use fewer expressions, cut whatever isn’t necessary<br>
the main goal is a complete playable game<br>
<br>
future dobby can have the fancy animations ♡<br>
