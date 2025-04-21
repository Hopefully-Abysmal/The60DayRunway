---
Date Created: 2025-04-20 22:12
Last Updated: 2025-04-20 22:12
tags:
  - Resource
Index: 
Topic: 
Link: https://www.youtube.com/watch?v=7ySVWcFHz98
Status: Unweathered
Published: true
---
---

0:00
I spent 18 months rebuilding my algorithmic trading platform in Rust I'm
0:05
filled with regret I would love it if this article was like I'm filled with regret for not doing it sooner like how
0:11
funny would that be all right Austin Starks take us on a wild ride I was a young hopeful rust fanatic on paper rust
0:18
seemed okay this is not seeming very Pro rust this is not pro rust at all on paper rust seemed like the programming
0:24
language designed by the Gods Not only is it the fastest programming language out there it's also one of the the
0:30
safest well Tech technically it's really hard for us to actually be the fastest language out there um it's very easy for
0:37
it to be not fast you in fact it's quite optimized to be not fast due to the safety but hey uh C++ is not faster uh C
0:44
is not faster none of the languages are faster anything that's at the tippy top just remember right there the the the
0:51
the top of the performance uh pyramid is going to be filled with manage memory language so you got rust you got C you
0:58
got Zig you got C++ I'm sure there's other ones Nim might fall in there uh but the reality is the reason why rust
1:04
often goes from the fastest to the next level is because you use things like RC's uh a arcs and mutases to to
1:12
effectively get around uh rust right or more so uh clone yeah I guess Odin would
1:18
be in here as well so this is like a very typical this is like the typical problem uh here right wait people don't
1:24
use arcs in C++ I mean you use arcs if you use shared pointers in C++ and if you look at the bottom of the if you look at the bottom of the pyramid you
1:31
find a snake and a big yellow Square go goang falls under like falls into these
1:36
two categories right go as fast right once you have runtime managed memory which is RC's and arcs it's no longer
1:44
fast right you fall down into you you you fall down into uh garbage collected
1:50
right I I put a heavy emphasis on garbage collected because there's not garbage collector but you are no longer
1:56
you're no longer managing you're no longer managing your own memory you are letting some something else manage your
2:01
memory Java doesn't exist it's just a fantasy it is where did Java hurt you I'm not alone in thinking rust was this
2:07
perfect language if you read about rust programming language online you'll likely encounter overwhelmingly positive opinions every guide on medium every
2:13
post on Reddit every answer on stack Overflow everything is glowing I can't wait to catch a bullet by this I feel
2:19
like I'm about to catch a bullet by rust given this I decided to migrate away from typescript rewrite my entire open
2:24
source algorithmic trading system in Rust I gave rust a natural rating a neutral rating before I take that back
2:31
dang dang okay I I really hope that we we get some a really some really good
2:36
ones right I hope we get something really good here by the way if you're doing algorithmic trading I would assume you you'd want to be able to react
2:42
really really fast so I could see you using a very I could see why rust would be a natural decision typically you don't want to do algorithmic trading in
2:48
slower garbage collected language because a couple hundred milliseconds could cost you the trade right just real talk that it makes sense why you'd want
2:55
to use something that's better than typescript uh I wrote my let's see I wrote about my experience with rust four months ago in my last article I
3:02
concluded that while I really like the speed and some aspects of the language design such as enums and strong typing I
3:07
didn't really love the language what you're discovering is that you don't in loved imposed safety that's what you're
3:13
discovering My article was met with harsh criticism on Reddit including one highly upvoted comment that accused me of Chad gping to write my article dang
3:21
this is uh this is a lot of upvotes for something that is literally uh that literally isn't true I don't use chat GPT to write any of my blogs I just
3:28
simply don't I hate how it sounds this is just how I write nowadays I don't even use chat GPT to correct my writing
3:33
this is genuinely my writing style dude I'm right there with you I actually tried to use chat GPD to help me with some some stuff and it it just became
3:40
very frustrating I it became very very frustration what if he is a robot ooh
3:45
ooh anyways after posting I had thought that I'd given uh that I didn't give rust a fair shot maybe I was just naive
3:52
or came in with misplaced expectations now after working with the language for a little while longer I can confidently
3:57
make one conclusion the language absolutely [ __ ] sucks I think the language is great so maybe I'm not that
4:04
intense but dude this is funny but I've always said I think rust has this rust feels better than it is because when
4:11
you're solving a black box problem it's like really really easy it's really
4:16
really great he can still turn it around he can still turn it around there's some things that make Russ really good at like I love it for basic command line
4:23
operations along with like Maring that with some some like file reads transforms and stuff it just is really
4:29
good for that uh what I despise about rust I want let's see if you want to
4:34
find an article about what's right with rust look literally anywhere on the internet you'll be hard pressed to find
4:39
anything less than neutral about the language this article will be F focused rant about what I despise about this
4:44
crabby language all right let's see if we can let's see if we can figure this out horrendous verbose unintuitive
4:50
syntax and semantics yes when you get into this level this is what I always say the moment you start getting into this world this is where things start
4:56
getting like good rust becomes shitty really quick like really like once you
5:01
like when you hit into like dude a pin box dying future is crazy like this is
5:07
crazy it's a hascal dressed up as SE like language to trick normes hascal has this exact same problem yeah that's due
5:13
to async I know I've always said async is where things just get all effed up and the moment you get into Ayn land and
5:20
you try to do something that's really clever do it every single
5:26
time what what is what is this okay so send send means it can cross it can go across
5:32
it can go across um Asing boundaries correct and then uh plus uh tick underscore means the unnamed lifetime if
5:39
I'm not mistaken this is where I start breaking down too is once we start getting into this world this means it
5:45
can cross acing boundaries and it can uh and it has a lifetime that you don't need to um that we're not mentioning
5:51
right so that means the function that you're passing in F is a mutable function that takes an a client session
5:57
that returns a future at some point point in the world that that can be crossed over the boundaries and has an
6:04
output of R where R is send and static Asing it's very hard it's very very hard
6:09
yeah like I generally get what I'm looking at here I generally get what I'm looking at it's just that once you get
6:15
into this world it is it's just super hard like generally speaking it's very ve it gets very very hard all right so
6:21
all this looks pretty good all this looks pretty good none of this looks like see the rest of this looks pretty good right I I I would say that
6:27
everything else in here just looks pretty straight straightforward right anybody who ever said that rust doesn't have atrocity SE atrocious semantics is
6:34
lying to your face I see the thing is I think one thing that's really nice though that you're kind of you're kind of missing is the fact that you can go
6:39
operation session await if it's okay we do this if it's not okay we do that like
6:44
I think this is actually really nice right I think that this is a really nice thing and then you have a for Loop you
6:50
have all of this it actually reads really nice like this part this is what I'm talking about when rust looks really good is this right here this is really
6:56
nice rust and there's a lot going on here that is actually shockingly crazy right you have to start a session which
7:02
awaits something you have to start a transaction which awaits something you then have to do this operation then match on the errors and if you get the
7:09
error then you return out the result else you're going to go Max retry is exceeded this is really this is nice code it's this part right up here that
7:15
just gets so effed up this part gets so effed up there are certain things where
7:20
if you don't have access to an extremely powerful large language model then writing the function becomes literally impossible I don't want to spend 90
7:27
minutes figuring out why where claws in my run transaction let's see figuring out the wear Claus of my run transaction
7:33
yeah the wear wear Claus has become exceedingly frustrating I'm on your team and if you define your generics in the
7:39
wrong place run Clauses can be super frustrating like they they can become
7:44
super super frustrating that's why I like a language like o camel though having an exceptionally similar type
7:50
system gets away with a lot is because it's garbage collected it can just simply drop some of these difficulties
7:57
and that's that um yeah the large language model is an interesting is a very interesting call out saying unless
8:02
if I have access to this I I to me it says you just need to understand more about rust internally for you to be able
8:08
to do this and so this is that language curve you know I I jokingly made that video where I said rust learning curve
8:13
is like this once you hit async it's non- differentiable it's because this like skill issues here the problem is
8:19
that the borrow Checker when you're learning is like a steep it's like an upright curve and then you get it and that's it once you get the borrow
8:25
Checker it's easy but then when you add in lifetimes it's like another just upright curve and then when you add in a
8:31
sync it's like just such it like goes It goes off the table and it becomes so hard because it's it's it's just really
8:38
difficult when you marry all the concepts of lifetimes of traits and of async when you put these all three
8:44
together now you get this whole problem that's really really difficult and it is most certainly a skill issue it's most
8:50
certainly a skill issue but it's a very excessive and difficult skill so the rust curve is the Debian logo exactly
8:57
right my God the curve is nonfunctional yeah I know in the end I had to abandon the idea of a helper function entirely yeah so again this is just that's
9:03
because you're writing it the not rust way don't write a helper function can we all agree this is one of those things
9:09
that I always made a problem of is that in JavaScript you abstract out these similar functionalities across async
9:15
operations in Rust you don't want to do that because you will find that you hate your life you do you find that you hate
9:21
your life and it sucks a whole bunch because you do this and you just you have to like be okay with code duplication at some level or you have to
9:29
be a genuine master of rust or just given to arc mutex Arc mutex makes it
9:34
very easy oh I read that one okay uh you say he's also making it Complicated by using [ __ ] transactions I'm not sure if
9:40
that's true a lot of people want to use um by the way this code girl I can see your your experience is showing right
9:46
here wrong duplication is better than wrong abstraction absolutely hands down 100% correct um because you can always
9:53
fix an abstraction you can always or you can always fix code duplication with abstraction very hard to fix fix
9:59
abstraction by the way um I forgot what else oh no my cam died my cam died it
10:04
actually wasn't my camera it's my um it's my uh what do you call them my uh HDMI converter hold on almost there
10:11
almost there whoopsies hold on hold on there we go I blame Karen I thought it
10:17
was my Linux NOP there we go you're moving again there we go there we go all right in the end I had to abandon the
10:22
idea of a helper function entirely because I lit I quit literally let's see because I quite literally couldn't get
10:28
the code to compile yeah I mean dude I've made this mistake a lot with rust and I feel like you make the same
10:33
mistake with Zig as well I think the pro I I I truly think the problem here is what I would like to refer to as JavaScript brain JavaScript brain or
10:41
really Dynamic language brain Dynamic language brain says abstract on all
10:46
forms of code duplication and so you kind of adopt this without realizing it you adop you adopt it really quickly and
10:53
also a big problem about uh dynamic programming along with structural programming such as go is that you you
11:00
adopt uh well structural patterns and you think a certain way you think you think in interfaces and again rust does
11:07
not necessarily make traits easy and zigg they don't even have traits they don't even have traits they don't even
11:14
have them at all and so it makes things really hard what's the meme with like the four people talking about like
11:19
talking about something and then there's the last guy that's like you guys have interfaces what's what's that Meme called dry is overrated and people
11:25
overuse the concept absolutely they use it constantly and it is very very dangerous I it's true I've been coding
11:32
in c89 lately and I find my Js braen really leads me into the wrong uh into some bad places yeah uh what is it
11:39
called We are the Millers oh yeah this one this one this one something along the lines of like uh JavaScript uh
11:47
typescript interfaces are great right goang it's something something along
11:52
like the lines of goang structural I sure there's python there's some sort of
11:59
there's so I'd have to think about this more but this is happening I got to think about I got to think about this
12:05
still I know there's a joke in there so we'll just make the we'll make the quick and easy joke which I'll just grab the first one right I know sometimes bro
12:14
cooked for nothing I know there's something there's something there's something there there's something there's something there that's really good and I don't know what it is Zig
12:21
draft [ __ ] post it's a draft sh there there's definitely something there that's really good it's just it's going
12:26
to take too long to think about and so we say move on okay this is not what it looks like what people claim as Russ's
12:33
biggest strength a strict compiler to eliminate errors is one of Russ's biggest flaws uh just uh just give me
12:38
the garbage collector and let me do what I want to do real talk this is real this is absolutely real Russ biggest strength
12:45
is also its biggest weakness which is also very reflective of all other ones javascript's biggest strength is the
12:51
fact that you can just add a property to anything javascript's biggest weakness is you could just add a property to
12:57
anything right like that that's it's the pro every language has the exact same problem right in contrast if
13:03
I were writing this exact same function in go it would look like something like this well go is actually really great though I mean go gives you the
13:09
abstraction ability of typescript with the with the 99% speed of rust it's it's
13:14
it's very impressive uh run transaction do all this one yeah yeah start a client
13:19
session there we go defer session end yep do all this thing grab all that good stuff do this one Yep this is all
13:26
looking good grab all this stuff oh yeah oh yeah oh yeah oh yeah oh yeah oh yeah do the returns do the attempts Max yeah
13:32
go is just so simple right go is just so dang simple right it's just so simple that's what makes it so fun uh so easy
13:38
to read and understand it really is easy to read and understand and all the people I see a bunch of people saying if
13:43
air equals nil blah blah if we were to do this in typescript one two three four
13:50
five of those would be hidden erors in which you would not know you need to catch or not so you would just get
13:57
randomly borked whereas at least and go I know when I'm about to get borked and I can handle it okay so come on don't
14:03
even try that with me don't come on come on while the core of the function remains relatively the same you don't have to do back flips to figure out how
14:09
to make uh the dang code work it just works agreed horrendous air handling oh that's interesting I would kind of argue
14:15
my only problem I will say this about rust one of its big problems is that due to the question mark operator you defer
14:23
a ton of airor handling really easily the convenience of not handling an error
14:29
is so easy that I often find I think less about errors and I often find
14:34
myself oopsy dazing it's skill ISS you skill issue Fair please please it's a skill issue but nonetheless I find it so
14:42
convenient that I forget to like really think about how I should handle this uh Russ does have some very nice uh things
14:48
with erors as long as you avoid unsafe unwraps oh yeah uh you can uh you can be a damn sure that that the code will run
14:54
and keep running no pointer exceptions and unhandled errors just don't happen anymore yeah y right
15:00
wrong because when your data is wrong or something unexpected happens you'll be fighting to figure out what the hell
15:06
happened maybe I'm just an idiot and can't figure out how to enable stack traces but when an error happens in my
15:12
application I have no idea why well I mean back back Trace equals one right
15:18
rust uncore back Trace equals one am I am I incorrect on that one I don't think so right right yeah definitely some
15:24
skill issues on that one for prod why not I mean if you're going to if you're going to have except
15:29
why not why not have a trace assuming that you that you handled 99% of your exceptions or your errors and this one
15:36
you couldn't handle why not like I totally get when you have one and you handle it you don't need a stack Trace
15:42
right by the way this also would be largely this this also is very uh very nice to consider with um asserts right
15:50
running a bunch of simulations and asserts and ensuring that you can't have these kind of things you can really figure out a lot of your application
15:56
before you actually have it running with actual money doing trading you know what I mean uh I still use uh X er uh XX
16:03
errors and uh percent W for uh stack traces and go see I haven't used I haven't used XX erors I just still use
16:09
errors and pretty much do Wrap Stacks still right in contrast I I actually like ghost handling right I like the
16:14
fact that you don't have stack traces instead you just build your own stack and I build my own stack and so I get all the relevant bits in where the air
16:21
happened and I actually find it to be really nice like generally speaking I find it to be very nice um in contrast
16:26
with a language like python you get these beautiful art like stack traces that tell you exactly what happened down to the line number even in go you have
16:32
airs wrap yep which enable you to look at the entire error stack in your application which is only the places
16:38
you're really concerned about which is also nice perhaps I I'm a goddamn idiot because when I encounter an air and rust
16:44
I'm like I'm in la la land trying to figure out what happened uh to the uh to the or what happened wait trying to
16:50
figure out what the hell happened well I could not read that again I'm going to say it again the question mark operator
16:56
due to the extreme convenience of it all I think leads more people down this there's this concept there's a very
17:03
important Concept in programming that you need to internalize which is called the pit of success you want to make it
17:10
so that doing the right thing is so easy that people just fall into the right move and that's one of the problems with
17:17
uh Russ extremely convenient error handling is that a lot of people just question mark out the errors really
17:23
quickly and so you end up handling an error like 10 functions High
17:29
with absolutely no indication into where this air happened and I see this a lot I
17:36
see this quite a bit I'm not saying that if air is better if air equals nil is
17:41
better but at least you have to think about it a little bit more holistically in go even though it's more boilerplate
17:48
you have to think about it you have to wrap it you have to add context it's also why I like anyhow I can add context
17:55
at every level and by adding context at every level I get go like air handling
18:00
but with the convenience of rust right a d air is just crazy don't do d air a d a is nuts anyhow and this a are friends
18:06
yeah uh I need this uh ePrint Ln litter throughout my application in fact no I'm
18:12
not an idiot this is a flawed language design I think this is just again I think he's just when you use rust you
18:18
don't fall into the pit of success and by not being in the pit of success I think it's very easy to blame the tool
18:24
as opposed to the knowledge of it and remember I'm not I'm not at this point I am not a rust lover I not a rust lover I
18:30
think it has a lot of things going for it but I actually think that Zig is significantly better uh I think it it gives you the right amount of safety
18:37
with giving you the right amount of uh uh control over your program I think it's the best of both worlds and I would say that this this right here is is
18:43
definitely much more of a skill issue that's very obvious like you goofed up you goofed up hey dude it took me like a
18:49
year to really get a good grasp on errors and rust like to really understand a nice way to handle rust it
18:54
took a long it oopsy daisies it took a long time and so I definitely don't blame that at all uh Krabby Community
19:00
hot take the Russ Community isn't as nice and cool as they pretend to be absolutely Russ Community is probably I I would say the least friendly zigg
19:07
might be the least friendly Community but then rust is right afterwards I think JavaScript and typescript generally have a pretty friendly
19:13
Community right like I can [ __ ] well okay PHP has the nicest Community we can
19:18
all agree to that anyone that disagrees that PHP is not the nicest Community I would like to I would like to mention
19:23
Adam Elmore and Aaron Francis okay you can't you cannot beat Adam Elmore and and Aaron and Francis as the nicest
19:30
people in the universe yeah PHP is a very nice they're super super nice very very nice community and I would like the
19:37
reason why I'm going to laravel is that uh I or Lon is that I am obsessed with
19:42
how well and how good they their Community is and I want to learn from it I want to bring it in I want to bring it
19:48
to the mainstream software world where we can stop like where we can actually be a lot better like even notice this I
19:55
I'm not like I'm not dunking on this guy I'm not being mean to I'm saying hey this is a really natural conclusion I
20:01
think a lot of people run into I'm fully on his team I'm trying to like I'm trying to bring the goodness of that PHP
20:06
Community outside because I think it's really healthy and I'd love to see more of it and I agree fully I think R the
20:12
Russ Community specifically in the more leadership roles are some of the meanest people I've ever interacted with in my
20:18
entire lifetime like absolutely the meanest people it is shocking it is shocking how much of their superiority
20:25
now there's some good ones I I I can think of uh uh gosh what it's Shepherd something Shepherd um gosh why I dude I
20:32
can see his name dude his name is like derp Shepherd or derp something derp Shadow oh gosh why can't I remember his
20:38
name really a Shep Master uh dude uh derp yeah derp really nice guy
20:45
Shepherd's Oasis Shepherd's Oasis there you go I actually think he's a really nice guy and he's an exceptionally
20:50
talented person like outrageously talented and still like communicates in a really nice way like I actually think
20:57
that just genuinely a huge amount of uh huge amount of uh respect for the guy right absolutely huge amount of respect
21:04
uh all right because mongod DB is shitty mongod DB is not a real database it's a key value doc stored and no squeal
21:09
storage system that literally designed from uh for marketing metrics it didn't even Provide support for asset or
21:14
transactions until more recently and for the longest time it just blindly corrupted your data due to its poor Q to right design there are better datab
21:21
bases don't make Russ look bad for using mongod DB I mean this is actually just terrible advice I mean really the thing
21:27
that he was struggling with is having helper functions which is typically I find to be very difficult for doing a
21:33
retry over some async operation right you could generalize this to retry over async operation [ __ ] not going to make
21:40
it for sure [ __ ] not going to make it but this response is wild right um but again I'd also like to say that random
21:47
response on the internet is not reflective of the community so just remember this that I don't think you
21:54
know what I mean someone just said something and it's very very true I think generally speaking when I when I think of when I think of the Russ
22:00
Community I think of I I just come back to this picture often and I can't I can't undo it cuz once I once it's in
22:08
the once it's in the brain it's just stuck there it's just stuck there forever I'd really love to see a turnaround in the community and be a
22:14
little bit more approachable uh for example I asked the question on the rust subreddit how to improve air handling with mongodb rust crate the it my answer
22:20
ranged from switch to postgres why am I using mongodb at all mongodb is bad in go and python 2 an actually helpful
22:27
suggestion to improve air mess okay that's good that's good I I do I always find this strange when somebody asks a
22:33
question how do I handle this situation better I've always found it such a strange answer to be like use postgres
22:38
like I will say that to Dax or to TJ but I would never say that to an internet random person you know what I mean
22:43
that's that just feels weird uh there is no other programming Community that's as cult-like as rust they ignore all the
22:49
giant glaring flaws with the language like it's crazy learning curve verbosity horrible error messages crazy syntax and
22:55
questionable language design choices they'd rather say it's a skill issue when the devel uh with the developer that's insane to me I do think you
23:02
you're you're definitely having some level of skill issues I think one of the hardest parts about about writing in different languages is adopting the
23:09
mindset of that specific language and it's very very hard and so I'd revisit this maybe a bit more like I'm on board
23:15
with you that I don't think rust fits all situations but I think that uh horrible design choices I I actually
23:21
think a lot of the design choices are really good I think there's a lot of really cool things like dude imple imple
23:26
uh uh what's it called imple uh from and try from is like one of my favorite
23:31
things of all time yeah he's doing it solo with no Mentor yeah that's very very hard imple from and imple TR from
23:37
is probably my favorite uh design feature of all time it's so good it's
23:43
like shockingly good I I wish more languages had um that I dis like shadowing uh in Rust a lot funny you
23:49
know it's funny you should say that because I was on your team I thought shadowing and rust was like such a bad idea and now I love shadowing and rust
23:57
and the reason being um and the the reason being I have an example somewhere uh here I can just search the word maybe
24:03
there we go I always am like hey get an index of something if it equals null I want to just return this back out but if
24:08
it doesn't equal null I want to like unwrap that null cuz I just I generally hate indenting I try not to indent uh so
24:14
I'm not going to have the inverse of this which is capture grouping uh and then getting out of it and so I I I wish
24:19
I could I really wish I could just do this right like I actually wish I could Shadow I think shadowing is really really nice I actually really do like
24:26
shadowing now that I understand it before I didn't like it even when I used it and I did understand it that's kind
24:33
of a dick phrase to say I did understand it but I just didn't now that I've used enough times I actually really really
24:39
like this right what is shadowing just what I just did right there this right here is a maybe
24:45
uze this right here is a uze so you a shadow is to change its type I'm going
24:50
to change its type from option uze to uze you can use oral so yeah yeah I mean
24:57
those are things you know this is me this is like this is like some of my first Zig I ever wrote I know there's better ways I know there is like an orl
25:04
something something something I haven't quite got there yet right I'm still learning all the things you know I you
25:10
know I like to um I like to write a language in a way that's familiar with me how to handle it and then as I get
25:16
better I like to try to get better at it you know I like to kind like like as you can see right here I'm kind of getting good at the catching right I'm getting
25:23
there I'm getting there just please let me let me get there I'm getting there slowly though I do agree with you I do agree with you that I guess guess I
25:28
could do something along the lines of oh whoopsies I just realized that I
25:35
was yanking the whole wrong thing whoa whoa whoa whoa whoa whoa whoa
25:41
whoa that was crazy so you're saying I can go or else
25:46
return null right that's really really
25:51
nice thank you I know I yanking wrong very very beautiful like these things
25:57
like this again Zig has some really nice operations here this is very very nice uh but again what's the use case of
26:02
shadowing when you wish to change a variable type but keep the same name right very very nice all right final words with all this being said rust has
26:09
some pros it's fast and well that's mainly it no no no no no no uh multi-threaded programming I find to be
26:14
generally speaking multi-threaded programming in Rust is pretty enjoyable uh just multi-threading itself of course
26:20
I cheat with Arc mutex Andor clone forgive me but if you clone Endor Arc mutex async is is really not that bad
26:28
there's plenty of reasons I actually really like it uh airs as values I think generally is a good way to go uh but if
26:34
you're trying to get maximum performance and async I find it very difficult I do like the idea of having the reminder of
26:40
like hey you can't have this like here here's a good example um if you use Channels with go there's like these four
26:46
rules of channels that just make it super super hard to work with and I hate it whereas when you work with Channels
26:53
with rust because it has an optional type it actually makes it really really easy to use a channel you can't get
27:01
stuck in a whole set of things and this just genuinely makes acing programming
27:06
significantly nicer just like at an entire level um I can't remember that let's see the four uh bad things about
27:14
um goang channels right there's like the four things you got to know I know there's one whatever I don't even want
27:20
to I don't even want to look for it we're not even going to look for it but there's like these four rules of things that are very very annoying and Russ
27:25
just doesn't have it due to the options that means you can like here's one thing
27:30
if you return a nil through a channel you close the channel if I'm not mistaken whereas with rust because you
27:38
have options you can have effectively some null right you can say hey this is
27:44
this is empty there's like there's there's a bunch of stuff uh closed channel is only you're mistaken I'm afraid I'm mistaken on that one okay my
27:49
bad my bad I'm I don't use channels a lot I thought there was like no Nils reading from a nil Channel Panic yes
27:55
reading from a nil Panic uh Nils and uh go L and channels I thought there was
28:00
a whole okay yeah I know there's like a whole bunch to it like I said I'm not great at go I use almost all my go has
28:07
no channels except for a couple and I find channels to be really great but I know that rust had a really nice it has
28:12
really nice ways to know what to do here okay let's look at this the a channel
28:18
send uh to uh let's see a send to a nil Channel blocks forever like that sucks
28:24
can we all agree that this is bad that's one really nice part about r is that it just returns an error and says hey
28:31
Channel use of closed channel it's very very nice um receive from ail Channel
28:36
blocks forever can't you get around this by doing a receive with two arguments can't you you can get around that by
28:42
doing a uh a like a receive with uh X and done right can't you get around that
28:47
now with that so isn't that isn't that Axiom kind of uh generally dead yeah not okay yeah yeah yeah yeah yeah it's the
28:53
Val okay pattern yeah that's I I didn't I didn't want to write all this stuff you know what I mean um let's see send to a closed Channel
29:00
panics also again um that's pretty reasonable I'd rather have it return an error though the weird part is that go
29:06
makes such usage of errs I'm surprised that they didn't just send an an air back right I I feel like the usage a
29:13
channel to would be really nice if they had errors and stuff and then what's that receive from a closed Channel Returns the zero value immediately this
29:21
is of course because they don't have options right so again if you had an option you can tell that a Channel's
29:26
closed because it returns a none right that means there was nothing there as
29:32
opposed to something that's empty which is very very different right so an option would be really really nice and
29:39
so I would prefer that over this I knew there was some there's some quirkiness right and so I find that this one is
29:44
like a very I find this one to be very difficult yeah you can always use Val you can always use Val and that that
29:50
should be used you should use Val it's just I would rather have an option type that makes sense and so what I find that
29:57
is when I read from a channel so I do this thing I forget where I do it but I do I do a thing where I check for um I
30:02
check for results and how I check for results is that what I do is uh what is
30:08
it is that I do a like a function call like a fun function get I'm way too zoomed in and I'll do like a select and
30:15
then I'll do like a pull from X and then I'll also do like a default uh return
30:21
return return something right and so that way I have like a default return and this and that way I don't it's like
30:28
non-blocking quick value select and I know this is like a this is some level of a pattern anyways I don't know I F
30:34
you know this article this article is skill issues but I think I think the thing that you have to um you have to
30:40
pull from this is that just because there's skill issues doesn't mean there's not real issues as well I think
30:47
the pit of success with rust is a bit shallow I think it's very easy to do the
30:52
wrong thing and that's why I think it's pretty universally agreed that with rust
30:58
people find that they build something they refactor it they build it new they
31:03
refactor it they build it again they refactor it right and they find themselves in this constant refactoring
31:10
thing because they they they're not it's very hard to write it right the first time or even write it good enough the first time and so that I I find that
31:17
it's just that Russ doesn't doesn't have the same ability to just fall into the uh into the correct way at least that's
31:24
my general perception of it I think if I wrote it all the time I could I could fall into the right way uh very easily I
31:31
think that if I just had enough uh just had enough reps I think rust would be very easy at all points including in the
31:37
async world but I think because I don't have enough reps I don't do it 40 50 60 hours uh a week I don't fall into that
31:45
there you go the pit of skill issues it's it's a pit of skill issues more than anything else rust is fun but it's less practical sure I guess uh it's also
31:52
safe too if we compare it to C++ it's obviously the better language um I I do
31:57
feel like that's also again I think that this just when I when I hear this phrase what I hear is that you're either
32:03
comparing it to C++ 11 and Below or B you've never really done C++ and you
32:08
heard it you heard it stupid and so therefore you kind of like dunk on it you know if you use unique pointers or
32:13
shared pointers and everything you you generally it's pretty easy to do the right thing and go or I mean in C++ it's
32:19
more verbose than I like can we all agree it's more of ver boast than we like but generally speaking long as you
32:25
do long as you stick to a certain things it's pretty easy and then of course there's also like all the crazy operation overloads uh and and the weird
32:32
crazy copy const structures the L values R Val there's some there's some hard parts that I think take a long time to learn to master C++ is like mastering
32:39
rust I'd rather have my application uh take a few dozen milliseconds longer to run if it means my development time is
32:46
cut in half which is an interesting trade-off to make for an algorithmic trading because Al algorithmic trading I
32:52
would assume a few dozen milliseconds can be impactful on the bright side if we choose to write my app application in
32:58
go I'd also probably have some regret what if it could be faster I'd think to myself there's yet another article about
33:04
how Russ is the best thing since sliced bread oh geez I made a mistake at least the uh I mean article fomo influencer
33:11
fomo is real like real talk influ in influencer fomo is super real by the way
33:16
uh I I did build an Arbitrage across us across different trades for cryptos and
33:22
we used belman's Ford's maximum flow problem to detect multile Arbitrage and it was pretty sweet I I made some money
33:28
but the biggest problem is I just didn't have $10 million to put in or I literally could have made an incredible
33:33
amount of money back in the day when there was such inefficiencies in the market uh at the very least now that I
33:39
know rust I feel like I can learn anything maybe I'll pick up o camel for the hell of it it can't be much worse
33:44
than rust can it oam's great but I think you're going to run into things that you dislike about o camel equally but probably less I spent this whole week in
33:51
fixing it's just milliseconds performance dude people do that you can learn anything just put in the time you can learn anything you really can thank
33:58
you for reading if you're interested in uh in algorithm trading in AI subscribe to Aurora's insights want to see how
34:03
fast Russ really is create accounts on Nexus trade today interesting let's see what the comments are oh are there any
34:08
comments I was I was wondering if there's comments let's check out some comments I completely lo I completely lost it in the low IQ article damn damn
34:17
dude it's so much nicer to say the word skill issues dude I do like this well Cornell I went to CMU I am a gem fellow
34:24
and I'm a software engineer making six figures what about me as low IQ winky face you know you don't need tojust
34:30
yourself a little little little word little word from the experienced you you know what instead of that I'll just show
34:35
you go to YouTube uh go to the primagen I have a short that I thought was very
34:41
very good uh which I tried to make it as obvious as possible I have I have a short that I thought was really really
34:47
good right right here we're not going to listen to it nope nope and uh the
34:53
comments are just man discover asserts then we call this defensive program that sounds like strong typing with extra
34:59
steps right like they completely Miss what asserts are about and they say a bunch of stuff so instead in 20 years
35:06
just imagine what else this guy hasn't figured out so instead you just don't you just don't respond sound like like
35:13
you sound like a loser you just don't respond cuz honestly it's easier and I'm okay with that and I try I try just
35:19
never to respond because I'm just like man you know it's just it just makes you feel shitty and then they they then they're like trying to dunk it dude it's
35:25
just like I I ain't about it uh still let's see that's still not rust that's a
35:30
just mongod DB crate you're complaining about brother it's pretty funny uh you're supposed to write your own errors
35:35
and overload The Source methods for the stack Trace anyhow does a good job do context uh you can't blame rust for you
35:41
choosing the wrong language for your use case if you didn't care about compile time safety and needed faster iteration you should have uh you should have known
35:48
to use language like go or python instead the problem is is that you can say these things but often personally I
35:56
don't know those things until I do them and I get burnt by them right because you can you can generalize this advice
36:02
to a whole bunch of you should haves right you ought to have known and I find
36:07
that I don't know until I have goofed up several times you know what I mean and I
36:12
think that that is really really really really obvious only when you're on the other side Prime wants to agree and
36:18
disagree at the same time exactly no I I do I do want to agree because it is correct but it's so hard to tell
36:25
somebody that you know you don't know until you know you know I I've known about asserts for so long I've seen them
36:31
in code for so long I never used them then all a sudden I used them and I really understood them now I can't stop
36:37
using them right like you could not have explained it to me until someone named joran the tiger beetle uh database guy
36:43
gave such an impressive presentation I said I must be missing something I will figure this out and now that I have now
36:49
I effing love it the spite the fact that I've known about him for like a decade oh you too after tiger beetle yeah it's
36:55
just one of those things that's like it's super hard to explain something until you've experienced it programming
37:01
the negative space article yeah it's it's it's good it's very hard you know you should explore and you should use Technologies incorrectly because you
37:06
will never know why to use them correctly performance matters uh standards uh standard let's see for high
37:13
frequency trading yeah standard algo Bots that do crypto not so much okay okay you should see the fpg and alos
37:19
that are Nano second sensitive yeah you're talking about like Jane Street o camel on stuff dude it's crazy been in
37:24
this space for almost a decade and there are some wild stuff out there Rus go ET are not even considered where big money is yeah isn't it like just you're
37:30
burning fpga I know that when it comes to Forex exchange it's or Forex it's all about it's all about fpgas and nanc
37:38
sleep the Beast thank you very much for the five gifted Subs appreciate that anyways children learn by exploring yeah
37:43
and I think that's we shouldn't discredit exploring we really should be very careful about that don't don't I
37:51
think it is good insights in the sense that the pit of success is extremely hard to fall into with rust and I think
37:57
that if you're going to do Rust you got to learn the language really really well to be effective and that is a huge
38:03
danger to most people is learning the language extremely well before jumping in so before you rewrite your stuff
38:11
maybe spend six months really learning the language read through the book understand about allocations read
38:16
through the async book understand that practice pin pin project all that crap
38:21
and then once you get it all done then maybe you know it can be better anyways the name
38:30
this is the primagen I don't know why I slapped my ball I honestly have no idea why the ball slapping just happened


# Reflection
## Curiosities
- 

## Ideas
- 

## Misc. Notes
- 

## Questions
- 