---
Date Created: 2025-05-04 12:52
Last Updated: 2025-05-04 12:52
tags:
  - Resource
Index: 
Topic: 
Link:
  - https://www.youtube.com/watch?v=lYSJo36KYZk
Status: Unweathered
Published: true
---
---
# Summary:


# Key Terms:
* 

# Reflection:

## Misc. Notes
- https://www.mercurial-scm.org/
	- https://wiki.mercurial-scm.org/
- Git good tho...
	- I also like github because it allows for people with no experience in it to access and use basic functionality
- Basic answers to questions: 
	- lack of large Filestore?
	- "better performance"
	- Owned by microsoft now (~2018)
	- Custom tooling
- Per interviews:
	- "stat-ing" all of the files back in the day
		- linear extrapolation on file count to long term -> 45 mins per op
		- 44k files -> 1.3million files in a couple years was a crazy assumption
	- Git wanted them to split into sub-repos (honestly yeah tho thats better for releasing too)
		- over the years gained support for larger monorepos
- graphite.dev/blog/why-facebook-doesnt-use-git
	- Interesting AI code reviewer tool; something to look into later on.
## Curiosities
- Public Facing Repositories with mercuruial SCM
	- https://wiki.mercurial-scm.org/PublishingRepositories
	- https://wiki.mercurial-scm.org/MercurialHosting
## Ideas
- 
## Questions
- 

# GPT Refinement: 

# Transcript:


0:00

I've seen this on the Reddit a few times and I just never got to it so I'm actually kind of excited about this idea

0:05

of why Facebook doesn't use git I work on building graphite which is fundamentally inspired by internal

0:10

Facebook tooling when I set out to create a startup with friends I had never heard of maerial uh despite being

0:15

really I mean I've heard I've actually never used maerial has who's here used maerial yeah I don't think I didn't

0:21

think maerial was a SN That's how little I know about it is that I don't know what it is I just know it wasn't tortois

0:28

I used SVN and I used tortois SVN okay so when Mel came out I had no I had like

0:34

literally no idea you seem to be right yeah I thought I thought as I thought Mel had some rules around lock files is

0:40

that true cuz perforce also had this idea of lock files and all that I used tortois yeah who didn't use tortois okay

0:47

I went hard on tortois okay I went hard on tortois despite being passionate

0:52

about all things Dev tools my previous engineering experience has included personal projects College homework iOS

0:57

development at Google and infr development at Airbnb throughout my life get by the way Airbnb I does everybody

1:05

universally hate the Airbnb JavaScript recommendations is that like a thing

1:10

that we all is that a requirement of being a JavaScript front-end developer is to hate

1:15

Airbnb like style guides and requirements I've never heard somebody

1:21

say they're great throughout my life a git was common as water it was so common in fact that I assumed it was the only

1:28

viable tool for creating and managing code changes so yeah I was lucky enough to start coding with a SVN or with a a

1:36

source management I think in like 2018 so only about three years after git was created and so at that point I you know

1:43

git was very it was not popular at all and so actually at that point SVN was like at the height of its popular and so

1:49

it's like I either chose between Mercurial Mercurial Mercurial Mercurial or uh SVN and I chose SVN and I think

1:57

that's because dream host had an like a public SVN option and I was hosting on

2:02

dream host back then funny enough maerial expert Gregory sorc sat a few

2:08

seats away from me at Airbnb though I only knew him as a uh as a kind of deskmate and knew nothing of his

2:13

contributions in 2021 my teammates Thomas and Nick opened my mind they came from Facebook and to my surprise hardly

2:19

knew get instead they were deeply trained on material patterns and Facebook stack diffs workflow over time

2:25

they sold me on the benefits of non-it tooling and patterns and we ended up making an early company pivoted to bring

2:30

stack diffs to GitHub developers in the process we made a CLI that incorporates the idea from HG into GI okay so I

2:37

didn't realize that HG mcir is that true I know dream host yeah holy F dream host

2:43

yeah for those that may remember dream host I was a dream Hoster so hold on does that mean that stack diffs and

2:49

these things are actually a maerial concept and they're not I think I explained further down okay okay to me

2:54

that's kind of crazy because I always thought maerial was like a bad version of source control I actually I had no

3:00

idea that Facebook used it as apparently their primary type I mean when I start when I joined Netflix perforce was the

3:06

primary type for quite a bit of time this post is not about our startup rather it's about the rude question that has neged me for over the last three

3:13

years why do facebookers metam mates

3:19

what please don't please tell me that's not true they're called metam mates please tell me that's not true sus dude

3:25

metam Mates is just the worst name ever why adopt maerial instead of let's see instead and build custom workflows on

3:31

top of it I know Google doesn't use git but that makes sense Google's engineering predates git by over 5 years

3:38

yes uh but I mean you can always upgrade that's not hard to do Facebook on the other hand was founded at the same time

3:44

that git was created in 2004 by the time Facebook was seriously evaluating Source control tooling git was more popular

3:50

than maerial so why does Facebook not use git this question is Niche but I think it's a fun one to consider I guess

3:57

you know what's strange I am so ingrained in using git at this point I

4:03

would have just simply never thought to ask any other question so this idea of

4:08

not using git just seems kind of let's let's answer this question if Facebook

4:14

had learned let's see leaned into git and contributed back in the early 2010s the engineering world might have looked

4:19

different git might be more userfriendly and might natively support stacked changes I would never call git not user

4:25

friendly for me git has always been really really user friendly and I guess that's probably because I come from an

4:31

SVN world where I I know when people say get is hard I've never understood that I've never understood this kind of

4:37

commenting get is so confusing how is G confusing like what about git is confusing that's what that's I get I

4:45

guess that's the thing that I've never understand is like what is confusing about git G is confusing how can someone

4:52

like is is it possible for you to try to type in a reason why it's confusing in a few words like can someone just hit me

4:58

with like a a few words reason check out Prime's G course I do technically have a g course by the way I mean hey hash okay

5:04

now this is an actual ad boot. Prime for my G course and by the way get course number two is coming out next week and

5:10

that will be all about merge conflicts uh work trees working as a team that kind of stuff but I'm just curious G can

5:18

eat dick I'm on FTP okay crazy literally ignored my concise explanation I didn't

5:24

literally ignore it did you not see chat going by 100,000 miles hour I think there's a fundamental principles that people don't learn so it's confusing to

5:31

them that just seems that seems like a stupid reason I want to see a real reason someone give me a real reason

5:37

subm modules and sub trees are confusing sparse checkouts and shallow clones are a bit tricky get rebase master I do that

5:45

all the time rebasing is great it's easy to get yourself into a bad State and it's hard to dig yourself out really so

5:50

okay so General my general rule of thumb is that I think rebasing multi-branch conflicts issues with PRS on those

5:57

branches I think all of that is because you've never actually learned it like what you know I'm I'm going to be really

6:03

real here for a second I think that most of you have just never taking taken the

6:08

two hours of time it takes to learn get well enough to not be confused by any of

6:13

it I've only been in a state where it's actually confusing very few times and I think it's because I've ran into a bug

6:19

with Git and I I I've ran I've ran into a problem with Git every now and then uh

6:24

which which is much different which this actually just happened to me just a little bit ago where I had a I had a file that said it was changed and when I

6:31

would add it the file would disappear it was gone and when I but then my file was

6:37

incorrect and so then I'd reset hard and then my or then my file would then show

6:43

changes again and it would be like in this really weird state where there's somehow a cash problem or something has

6:49

gone on where there's some sort of out of like inconsistent state that uh just

6:54

a little bit and so that that was like uh the file wasn't binary and that only happens in very rare circumstances I've

7:00

actually had something where it's like yeah yeah some sort of line ending yeah something like that that's just super

7:05

confusing mine wasn't a line ending it was a single character change but it was really confusing what was happening

7:11

whatever right like besides for that happened which has happened probably four times over the last 10 years of me

7:16

using git the rest of it is like if you don't know re rebase rebase is super easy okay here I'm just going to give

7:23

you guys a quick rebase you have two different branches okay and here's the

7:28

histories this is Master this is feature all rebase does is simply allows you to

7:35

move where you were pointing at to somewhere else that's it if you think of

7:41

rebase in any other way you're just making it entirely too complicated it allows you to take your commits and

7:47

perform an action over those commits you don't use rebase over merge you don't use rebase over merge you rebase and

7:55

then merge I I think I don't see I think you guys are all using rebase incorrectly this is actually shocking

8:01

how many of you okay how about this one how about how about this one how about August we'll say how about this one

8:07

we'll say how about August 14th approximately I will go over my git course on boot dodev I will do the

8:15

entire thing both courses first one and second one and I'll answer every last

8:20

person's question and then on boot. we will release a six-hour video of me

8:25

going over everybody's question and we'll just simply do get because I cannot believe how confus like that's

8:32

crazy how confusing you guys are like gets not hard this is shocking to me

8:38

personally okay this is shocking to me personally

8:43

that this is so hard gets hard no git is

8:49

easy all right GitHub might make devel uh developed better support for closed Source software development ex early

8:56

facebooker companies like uber and Pinterest might have also used used git and GitHub as their Source control

9:01

rather than fabricator and material leading to less fragmented ecosystem over the last decade but Facebook didn't

9:07

stick with Git for their primary monor repos instead they adopted material for their Version Control and incrementally added custom tooling on top why first I

9:15

tried Googling the answer and found the following definitive blog post scaling maerial at Facebook all right the

9:22

10-year-old writeup along with some later YouTube Tech talks gave me a starting uh answer because

9:28

performance I mean even to me that sounds confusing even this feels confusing for me what is G doing that

9:34

there's a problem with performance I don't I don't really even understand that because I I guess this might have been before the day days of large file

9:40

stores right large f file stores uh Microsoft owns no this was Microsoft started owning GitHub in like when 2018

9:46

2020 git does not scale well for large repos yeah I guess if you're if you have a big enough repo git starts to suck

9:54

that's fair and pre-large file store that's also Fair they must be committing large binaries and well that's what you

10:00

I mean to be completely Fair there was 400 megabytes worth of Json in a tvi

10:05

directory that we had to download every single CI run so I mean things happen I'm just saying sometimes you download

10:13

400 megabytes okay that's all I'm saying sometimes you download 400 megabytes okay a Jon Json is not binary you're

10:20

right it's just it's really really fat and big binary uh but I wanted to go deeper and hear from the original

10:26

deciding Engineers with the help of a lot of teammates I post the question on an exf facebookers group asking about

10:31

the history I also code cold emailed two of the original Engineers working on the project to migrate into material they

10:37

were kind enough to call me off the Record and give personal accounts of the project here is what I was able to learn from the full reason behind not using G

10:44

at Facebook hopefully this post can uh help further document the history behind why our Tools in 2024 are the way they

10:50

are this is going to be super interesting I'm actually super excited about this note I've never worked at Facebook this is uh and this account is

10:57

my best understanding of the facts as someone who wasn't there myself I am I was able to speak to a few people who

11:03

worked on the project and received their permission to write about what they explained to me this is crazy note Greg

11:10

spends a full let's see Greg spends full work days writing weekly deep Dives on

11:15

engineering practices and Dev tools this is made possible because of these articles help get the word out about graphite if you like this post try

11:22

graphite today I can't say it's a hashtag ad I'm just saying I'm getting Bamboozled here somehow I know what do

11:29

we call this is this an ad or not an ad now I don't even know now it feels like an ad hash ad [ __ ] uh why let's see why

11:36

and how Facebook migrated off git according to the 2014 Facebook blog post Facebook started out on git as one would

11:44

expect it was their default choice at the time for a source control system but around 2012 they started hitting scaling

11:50

limits I know shut okay guys guys shut up flip take this out flip take this out

11:55

flip be my scrub Mommy and take this out right now but around 2012 they started hitting scaling limits the post claims

12:01

their code base was many times larger than even the Linux kernel with uh which checked in at 17 million lines of code

12:09

and 400 or 44,000 files I mean that doesn't sound honestly that doesn't sound like terribly large is anyone else

12:15

here thinking this is crazy because I don't think this is very this is like I think uh the files the things that I

12:20

worked on at Netflix uh we had multiple repos with tens of thousand 20,000

12:26

25,000 files JavaScript files by the way and just seems kind of wild uh specifically get operations started

12:31

feeling slow for engineers not crippling slow but slow enough to Warrant an investigation yeah like clone will always feel slow I mean the reality is

12:38

is that I guarantee you whatever slowness they felt npm [ __ ] the bed

12:44

and requiring you to delete your node modules and reinstall them even installing from cash had to feel longer

12:50

right uh the key bottleneck was the process of statting all the files G examines every file and naturally

12:55

becomes slower and slower as the number of files increase this had to change

13:01

right this was 2014 because I assume git doesn't do all this statusing all the

13:07

time I'm curious about all this if that's that's true and even stating is stating 44,000 files going to be that

13:13

slow it has I know it's changed a lot but it's still interesting the engineers tried running a simulation creating a

13:20

dummy repos that matched the expected scale of Facebook's code base in a few years the result was horrifying basic

13:26

git commands took over 45 minutes to complete [Laughter]

13:31

I guarantee you Facebook the the the so-called stat files look something like

13:36

this they did their initial Facebook growth of files and then they're like well we're here now we were here earlier

13:43

this is 35x X being of course one month so we're

13:50

going to we're effectively going to grow like that forever and look at this at this point we're going to have 14

13:56

million files and if you grow to 14 million files it actually isn't even possible that's crazy uh in the words of

14:02

the original engineer of the project it's not the kind of thing you want to leave until all your engineers are complaining this is also fair and

14:09

factual uh by that point the thing would be too unwieldy trying to do damage control never mind come up with a

14:15

cleaner solution would be a Herculean effort so ragtag group of SW got to work

14:20

investigating Solutions first they contacted the G maintainers to see what uh it would take to extend git to

14:25

support large monor repos better here are some of the choice quotes from the email with the git maintainers it's 12

14:31

years later and yet I feel somewhat frustrated reading those messages sounds like you have everything in a single git

14:38

split up the massive repository to separate smaller git repos I mean we just did we we when I was at Netflix we

14:45

had uh we had all the JavaScript into one team and then we actually just started splitting the teams it also

14:50

makes releasing a little bit easier when you have like different sub things that can just release and move at their own

14:56

rate and then the main product doesn't have to adopt it until they're ready to and it just makes release trains and all

15:01

that a little bit easier I don't know personal opinion while you can do this it's not a good idea you should split up

15:07

rep pod stories I concur I feel let's see I'm working in the okay what does sick mean

15:13

again I forget what that means dang it uh SI oh yeah oh yeah that's right it's

15:18

it's it's it's to fix it's not just for pointing out errors it usually means to uh point out

15:25

errors and stuff right typically people use it to point out errors that's right that's what it was okay I just wanted to make sure I

15:30

understood what it was I'm working in the company with many years of development history with huge CSV repos

15:36

and we are slowly but surely migrating our codebase from CSV to get split the uh split the things up this will allow

15:41

you to reorganize things better and there is in my humble opinion no downsides while G could be better with

15:47

large uh repositories in particular applying commits in interactive rebase seems to slow down on bigger repositories there's only so much you

15:54

can do about stating 1.3 million files so they did I literally guessed this

16:00

correctly I literally G I unironically guessed what they did correctly they

16:05

were currently at 44,000 files and they made some sort of linear assumption going ah we're going to be at 1.3

16:12

million files in a couple years how would you even create that okay if you created if you created

16:21

one file every 45 seconds every single day 24 hours a day non-stop you would

16:28

get get to 1.3 million after a year and a half genius projections I know this

16:35

seems a little this seems a little seems a little fake the response wasn't Cooperative I I don't

16:43

know is this response not Cooperative or is it just like yo we

16:48

don't know what to do you said how can I make this thing faster on 1.3 million

16:53

files and we're just like you can't

17:00

I mean the fact that they responded and just said hey this would be my this would be my Approach I don't know what

17:05

to do here anyways the response wasn't Cooperative nor has it aged well in the

17:11

future full of large monor repos the G maintainers pushed back on improving performance and instead recommended that Facebook shared the uh Shard their monor

17:18

repo however sharding was a non-starter for Facebook team and they recounted being surprised by gits unwillingness to

17:24

be extended traditionally being offered free open source labor by a major tech company is well received gift that can

17:30

ensure a life let's see a lifelong for projects or a long life for projects I actually usually find this to be the

17:36

opposite when some big company wants to work on your open source thing typically

17:41

there's a lot of push backs because usually what they're working for is sometimes not where they want to go there's all sorts of different problems

17:47

and then once the company has what it wants it leaves you and then you have a lot more code and a lot more things you have to maintain as an open source

17:53

project they tend to get in do what they need to do and get the hell out I don't often find this to be

17:59

a completely true statement they want to add a fe features

18:05

they they need I know it to me this uh this doesn't feel

18:10

that doesn't necessarily feel good uh the big company is going to worry about licensing expect more polls Etc yeah I

18:16

mean there's a lot there's a lot of work to be said whenever that happens anyways that being said the git project was

18:21

under no obligation to bend to Facebook's asks I don't intend to paint them as the bad guys of the story doing

18:26

something because Facebook's asked you to is no way to live one's life interestingly the git maintainers appeared to change their tone two years

18:33

later after seeing Facebook contribute back meaningful improvements to maerial they mailed the list about performance

18:39

issues uh in git from what I saw it was relatively little feedback I had the impression let's see I had the

18:44

impression and I would not be surprised if they had the impression that the git development Community is relatively unconcerned about performance issues on

18:51

larger repositories so the question is if the G Community is interested in being competitive in such large scale

18:56

scenarios something what mcal seems to be now out of the box oh a decade later

19:02

GI has made significant improvements to support monor repos FYI or for uh for what it's worth uh the situation has

19:08

changed pretty drastically today get now with some knowledge of how to do it operates well with really really large

19:14

repos now I may have ADD added an extra now

19:20

okay that's nice so we don't have to worry about this Alternatives considered

19:27

alternatives to get in 20 12 were scarce you know it's kind of funny it's I'm I'm surp then why didn't Mel

19:34

catch on if Facebook was so it was so adamant in using something different and

19:39

they contributed a whole bunch to the point where things changed why wasn't maerial more popular what makes git so

19:46

popular that maerial isn't is it just simply GitHub is it the Hub that really made it

19:55

it turns out nobody actually needs monor repos okay yeah that's I mean I fully agree with that uh but some someone said get let's see

20:01

what's it called G was used for Linux yes git was used for Linux it was created by lonus uh in 5 days after uh

20:07

somebody broke the uh bit Maven bit bit bitkeeper the bitkeeper license by

20:14

reverse engineering its protocol which was a requirement that yeah bitkeeper bitkeeper it was a requirement that they

20:20

did not reverse engineer the protocol and somebody in the Linux uh whatever

20:26

reverse engineered it they broke the license and then bit keeper was like ain't no way and so Lina said f it and

20:31

wrote get in 5 days also just to be fair just because

20:38

Linux uses something does not mean we're going to use something remember Linux still largely operates via email does

20:46

anybody here discuss their issues via email anyone does mailing lists yo [ __ ] that [ __ ] exactly I mean

20:55

it's not fun I don't want to do that right every day yeah I know I I don't I

21:00

mean I am not I'm not a big fan you're I know you're on mailing list but actually

21:06

doing all of your development via mailing list does seem kind of crazy but I actually also see kind of some of the

21:12

benefits of using a mailing list emails are good for logging exactly I was about to say for logging purposes

21:19

that does actually sound kind of nice having a a a little bit better searchable results I don't find that all the

21:26

results are that great for searchability email uh good email lists are very clear unlike huge chat discussions yeah chat

21:33

discussions can be very confusing as well when I don't understand something I create it myself I created my own git Tools in a few years back and learned so

21:39

much yes this is a great way to learn by the way this is why we're going to be doing HTTP from scratch here soon HTTP

21:45

uh from scratch I want to start in September if possible let's see the team considered the closed Source perforce uh

21:50

Google's former uh Source control solution in the an early investigation call with perforce sales Engineers Facebook pointed out architectural flaw

21:57

on perforce local consist between reader and writer knows the response didn't instill confidence the sales Engineers

22:03

weren't aware of the fundamental issues and had no road map roadmap plans to address it damn Get Wrecked further

22:09

Solutions like bitkeeper were considered but all were quickly disqualified the last option was maerial it had

22:14

performance similar to git but had cleaner architecture where git was complex web of bash and C code maerial

22:20

was engineered in Python using object-oriented code patterns and was designed to be extensible object

22:25

oriented did Uncle I just heard Uncle

22:30

Bob I just heard him yeah yeah that's right I think I just heard Alan K and

22:36

Uncle Bob start capping somewhere deep in the Distance by the way can can we all just agree to one thing can we just

22:43

agree to one simple thing objectoriented code in Python is

22:50

the actual devil can we all agree to that can we all agree to object-oriented programming in Python specifically in

22:56

Python is terrible can we all agree to that no come on just just give it to

23:03

just give us one thing objectoriented python equals performance dude object oriented python

23:09

is insane for performance holy cow I changed I changed from object oriented

23:16

python because I thought it was going to be faster than using dicks for everything instead I did a couple dicks

23:22

dude just loaded up my program with a bunch of dicks and it was literally a 100x faster and I was shocked cuz I was

23:29

like ain't no way if I make a class obviously it's faster right obviously obviously it's faster yes the

23:36

dicks I just dude and I have no IDE it it was not faster it was in fact horrible dicks out for harambe dicks out

23:45

for python a class is a dick then why is it so bad dude it was crazy one of the

23:53

investigating Engineers by the way this argument is fairly baseless in the sense that um I somehow doubt that just simply

23:59

because something was object-oriented coding patterns made it much easier to understand I mean at the end of the day

24:05

you still have to understand everything from the ground up to really make good changes to a source control and so to me

24:11

it's like I think you'd I think you'd end up spending the same amount of time either way I think that python is just

24:16

easier to understand I think what I see here honestly is the following I see

24:23

bash plus C versus python and someone's like man this is

24:32

easier which I agree typically python is easier to get going in than a c and Bash

24:40

program okay I'm just saying it is easier almost

24:46

always almost always almost okay you can always make python hard python can get

24:52

really hard spin fire right now I know I'm spin fire these are some hot takes python can actually be harder than C if

24:59

you really want if you really try hard but if you want a bunch of PHP devs to

25:05

extend your version control and options uh that are bash plus C or python I know exactly bash which one should I choose

25:12

one of the investigating Engineers had a strong former experience with Mel and the team decided to attend mcal hackathon and Amsterdam to to

25:18

investigate further oh that's actually such a cool way to do this this is actually a I absolutely amazing way to

25:25

do that go to a place in which a bunch of people that have a bunch of experience on the thing you want to

25:30

change are all going to be in the same area so you can talk to them what a good idea and because I had a lot of Prior

25:36

association with maerial I bent over backwards to pursue every possible alternative before putting maerial on the table Brian O Sullivan ex Facebook

25:44

engineer uh what they found was a system that was easy to extend in the community of maintainers who were impressively

25:49

welcoming to aggressive changes by the Facebook team I think this was the specific hackathon mentioned but I'm not

25:55

positive some real early 2010 video vies I'm not going to watch it I don't want to die of cringe migrating the whole

26:01

engineering org okay so this is going to be kind of crazy prior Association uh after the Amsterdam

26:07

hackathon the Facebook team was convinced all that remained was convincing the rest of the company of

26:12

the migration this was the immediate or intimidating task Engineers can be

26:17

extremely sensitive about tooling changes imagine Vim versus emac and changing Source Control Systems is a big

26:23

deal I Som I I feel like emac versus Vim is a much different argument than using

26:30

mcal versus G like I don't think I would really care that much when I had to use perforce I was like ah I'm using

26:36

perforce now and every now and then [ __ ] happened I didn't understand why so I to go check the docks I don't know it just doesn't feel this doesn't feel like such

26:43

a big deal comparatively like if you tried if you told me I had to quit using

26:48

vim and had to start using emac like that feels like a big change it's just politics yeah uh the team set out

26:56

smoothly let's see out as smoothly as possible so not to trigger defensive responses from the other Engineers what

27:01

ensued sounds like a masterclass in internal Dev tools migrations the team Spends months socializing the

27:06

possibilities of migrating to maerial and took time to map all common commands and workflows between G and maerial they

27:12

went so far as to Source the frequency of git commands run across the company and specifically document how the most

27:18

frequent operations would work in material instead secondly they created opportunities for developers to voice

27:23

their concerns and discuss any edge cases that might be tricky in the new systems going in the team assumed they'd

27:29

get bogged down in flame Wars over eight obtuse eight-way octopus merge uh

27:34

hypotheticals but to their surprise they found their peer Engineers to be accommodating and friendly uh yeah you

27:40

know why does anybody remember the commun the discussion we just had about rebase nobody even knows git apparently

27:46

so there's no eight-way octopus merge that you're going to have to even worry about okay no one's going to come in

27:52

with those kind of things because nobody actually even knows the tool itself so guess what it's not even a big deal

27:58

let's see finally they committed to the migration and cut the company over to Mercurial uh the rest is history

28:03

Facebook contributed performance improvements to Mercurial making it the best option for large monor repos e uh

28:09

Evan pre uh Priestley extended a fabricator to support material Facebook leverage maerial concept of diffs to

28:15

create pattern of stacking unlocking novel code review parall parallelization by the way this is actually I mean this

28:22

is what makes graphite so good as this right here stacking is Honestly by far the most excellent thing thing ever when

28:28

it comes to working with people if you have to work with more than one person and you have to do code reviews this

28:33

idea that Facebook apparently created is by far the best way because that way you can keep working and make changes to

28:39

your previous one without just being just completely bogged down like wild ex facebookers left to uh to uh new

28:46

companies and brought their workflow with them creating a small but vocal Cult of Stack diff Enthusiast finally I

28:51

met some of those enthusiasts and decided to dedicate my 20s to Bringing material style stack diffs to get and GitHub closing thoughts what is the take

28:58

away from the story reflecting on our quotes and interviews I REM let's see I'm reminded of the classic wisdom that

29:03

so many of History's key technical decisions are human driven not technology driven yeah just like git

29:09

being created git was created because a human decided to break to it's that simple right that like

29:17

that's all you have to do someone was like hey man don't touch the red button and someone's like that red button they're like don't touch it I can't help

29:25

it and then touched it and boom get was created for all those reading this I

29:30

think this was Brian's true Brilliance in getting maerial adopted at Facebook and something people should consider when bringing new technologies to a

29:37

company ex facebooker kindness and openness go far in the world of Dev tools and I aim to carry these values as

29:43

I contribute to the history of source control I think that's fair if you could really nail what the problem is and how

29:49

you actually choose to actually fix the problem not just make a new perspective on the problem I think you do actually

29:55

have a real good argument as to why why your product is better and I think devs generally will listen to you I think

30:01

that's what it do because I really disliked a lot of my experiences with Sven I found working with a larger team kind of a big pain in the ass and

30:08

there's all these problems with it uh damn you're on a yeah I am on a bouncy ballb and so I found all those things like real and so when I used Git it was

30:15

a great alternative I actually enjoyed the difference between git and SVN at first I didn't understand it at all cuz

30:21

all I knew was just a very small slice of what git did versus SVN and then once

30:27

I used it a little bit longer then I was like oh yeah this is really great and by the way I don't even know how to do a

30:32

10-way tentacle hentti merge hyp hypothetical like I actually don't even know how to do this I would say that I'm

30:38

pretty good with Git and I don't even know how to do crazy I I didn't even know you can do crazy merges okay I know

30:45

nothing about these merges I don't I don't use those merges anyways the

30:50

name is give me that 10-way hentti tentacle merge

30:56

baby flip keep it in flip keep it in