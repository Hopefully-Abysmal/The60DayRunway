---
Date Created: 2025-04-27 15:42
Last Updated: 2025-04-27 15:42
tags:
  - Resource
Index: 
Topic:
  - "[[MetaGov Knowledge Organization Infrastructure]]"
Link: https://www.youtube.com/watch?v=zTaK09Lo94A
Status: Unweathered
Published: true
---
---
# Key Terms:


# Reflection:

## Misc. Notes
- Very rich in conceptual systems for knowledge organization infrastructure
## Curiosities
- 
## Ideas
- 
## Questions
- 

# GPT Refinement: [[KOI-LLMchat]]

# Transcript:

0:00

today we're going to be talking about architecting knowledge organization infrastructure and I I'm going to start

0:05

off with some more kind of theoretical background about how I think about the problem and then move into practical

0:11

examples predominantly from from metago uh metago as Anessa just mentioned is a

0:16

us-based nonprofit focused on uh digitally mediated

0:23

self-governance so uh my obligatory bio slide I have a PhD in electrical and

0:28

systems engineering from the University of Pennsylvania I'm the founder and chief engineer at block science board

0:34

member and research director at metov I am a trustee uh of a Data Trust called

0:40

superset and I'm a a lecturer and adviser at a variety of different organizations and as an ASA mentioned

0:46

I'm a advisory council member at num Focus um which is particularly relevant to this community uh how I got here

0:54

today I was at the uh num Focus project Summit talking about some work that

0:59

we've doing at metago around knowledge organization infrastructure which is based on some ongoing research and

1:05

development and in-house implementations and client projects at block Science And so there's a a lot of very a lot of

1:12

organizations kind of contributing to and experiencing the benefits of This research but I I really felt like this

1:19

community could benefit a lot from thinking about how we um both design Implement um operate and govern our our

1:26

knowledge infrastructures and so I decided to take that that lightning talk and blow it out into a full talk and

1:33

that's what we're going to do today so for starters um I'm G to kind

1:40

of review what um I think of as architecture and keeping in mind that

1:45

I'm a systems engineer not a software architect which means my experience is in architecting things like robots

1:52

business decision systems and a lot of um elements that contain or systems that

1:57

contain more than just software elements so they can use human and operational processes they can include legal

2:03

components then if I I'm not the one provisioning the specific legal items that includes licenses and contributor

2:10

agreements um legal entities um and you can imagine that that these kinds of

2:15

systems when they involve technology and humans that they have a lot of components um what I want to emphasize

2:21

here is that architecture is about the way those components are arranged in relationship to each other and in fact

2:28

the same components can produce lots of different behaviors um depending on how they're organized relative to each other

2:34

and so a lot of this discussion today is going of focus on using almost out of the box components at least wherever

2:40

possible and just organizing them in in new and interesting ways um that that

2:46

achieve our our goals from a behavioral perspective so um I'm gonna start off by

2:52

doing a little bit of theory which I hope you guys appreciate so there's this um concept of of an institution which

2:59

the sort of canonical definition from Douglas North is a humanly devised constraint that structures political

3:05

economic and social interaction um I'd like to compare that or contrast it with

3:10

infrastructures which are the basic physical and organizational structures and Facilities EG buildings roads power

3:17

supplies needed for the operation of a society or Enterprise and part of the reason I like to emphasize this these

3:24

are actually very similar um and if we think about it from the the perspective of Our Own organizations we um we

3:31

establish practices um and we develop infrastructures and the infrastructures

3:37

enable facilitate standardize automate and decentralize the various practices the the human constraints and activities

3:45

um and those practices actually are used they they include the use of the operations of the monitoring the

3:51

maintenance the governance of those infrastructures I this is especially true when we're talking about um

3:58

digitally uh media ated organizations where the infrastructures in question are technical but I would not exclude

4:05

from this literal physical infrastructures as well um as a systems engineer I sort of attack this problem

4:13

through something like a standard engineering validation and verification V but I've broken it down into something

4:20

that's a little more commensurate with a um kind of startup our software development mindset where we are

4:26

thinking about narrative models in terms of Storytelling but also Al requirements in user stories and theories of change

4:32

and then we digest from those more formal requirements designs um you know

4:38

metrics for testing you know if you're doing test driven development your tests might be the best representation of your

4:44

intended design um but ultimately those models have to be um compared back

4:51

against the human expectations and there's always a little bit of a gap here just due to the legibility

4:57

difference between people's stories and formal specifications of course formal specifications are the things we use to

5:03

implement and implementations can be um verified against those uh specifications

5:10

but implemented systems also have users and operators and experiences produced

5:16

by the use or operation of those uh those systems and of course we get

5:21

validation when we look at whether or not the system is producing the intended outcomes um ultimately we're comparing

5:28

back and forth the users are operators experiences against the narratives and in fact users experiences and their own

5:35

commentary about those experiences produce new narratives and you end up with a kind of closed loop system um

5:41

interacting between the sort of technical um potentially very complex

5:46

systems and the desired experiences and the lived experiences of the users and

5:52

operators and we view these systems as successful when we can actually align people's expectations and that doesn't

5:58

mean that everyone always gets everything they want the real world is full of tradeoffs But ultimately we're

6:04

setting expectations that can be met and meeting them and then continuing to

6:09

maintain that alignment is tantamount to governance um in systems engineering we

6:16

talk about architecture and a variety of different levels of abstraction and I think there's often a lot of confusion

6:21

um by jumping between layers so as a sort of lview um conceptual architectures are

6:28

really just like

6:35

idea do and kind of what the subsystems are functional architectures break systems down into um like components

6:43

that actually do something so they they may take inputs and produce outputs um they may fulfill key functions within a

6:50

data supply chain or otherwise um meet some Express need including some

6:56

subsystems meeting the needs of other subsystems to create an overall um

7:02

system that can and deliver on um a preferred set of behaviors um you get into a logical architecture when you

7:08

start to specify how um the difference here might be a functional architecture might call for a model that takes a

7:15

certain set of features and returns a certain set of labels but a logical architecture starts to specify like what

7:21

kind of model to use are you using random forests and or are you using um

7:26

you know logistic regressions um and then as you move into physical architecture you're concerned with the

7:33

actual specific implementation so in my you know machine learning model example you might be like using a a very

7:39

specific model from a pyit learn package with a like a specific even down to a

7:45

specific instantiation of that um the more specific the more concrete or literal you get the further you are into

7:52

the physical architecture and then obviously there's ultimately the thing itself but working your way from

7:58

conceptual through function and logical to physical is how we go about architecting particularly complex things

8:04

especially when there are aspects of the functional architecture that are not actually implementable they just exist

8:10

in the world and this is um commonly the case when you're dealing with systems with humans in the loop when you're

8:16

concerned with um a group of stakeholders who are directly participating and the system that you're

8:21

architecting accounts for both their their contributions and their

8:27

expectations and needs so what is knowledge organization infrastructure it's systems tools

8:34

processes rules governance mechanisms that enable The Collection curation management sharing and utilization of

8:40

knowledge within a specific context it encompasses both the technical and social components required to ensure

8:46

that knowledge is discoverable accessible reliable actionable basically that it serves the needs of its

8:52

stakeholders and so the key here is that we're talking not about just like a data lake or a particular data com or pool of

9:00

data but actually it's incorporation into a specific operating context specific group of people doing a

9:06

specific thing um that means that they have specific desires wants and needs and they have specific limitations

9:13

available attention you know resources to spend on the effort of um maintaining

9:18

and using that knowledge um and so I'm I'm going to briefly review some material from a

9:24

paper called why is there data it's by David sisen and Alon benm and David's

9:29

actually in the audience so if uh if I grossly abuse it he should interrupt me and tell me that I'm wrong um but uh I'm

9:38

I'm going to start with this Clos loop system model uh which basically shows a feedback loop from what you can think of

9:45

as raw serialized data collected from some location out in the world whether that's a physical sensor or an online

9:53

platform we're basically suggesting that this is low-level event data of some kind it's it's it's raw facts and and

9:59

raw facts go through something we refer to as information processing and this will be a pretty traditional data flow

10:06

which I'll review in a moment um but it is going to be recognizable to everyone in this community I think uh where we're

10:12

focused today is actually on knowledge processing and sort of understanding how we uh move from an information

10:19

processing way of reasoning onto a knowledge processing way of reasoning and how that serves understanding and

10:25

that understanding is still at least in my opinion uh the province of humans whether that's kind of humans in a group

10:31

or individuals um this is how we take knowledge we take it into context and we

10:37

render decisions and those decisions then affect the world of course then the consequences of those um effects on the

10:44

world may feed back to us through our sensors through through our observation um but at the end of the day um this

10:51

ongoing Loop is something that we can think about as having um an Effectiveness if we're able to produce

10:58

desired or intended effects which is distinct from something like how efficiently can we process data and I

11:04

think a lot of the times when we talk about intelligence especially artificial intelligence there's a tendency towards

11:11

focusing on efficiency um scale throughput um Etc but not necessarily as

11:18

much focus on like the quality of the um of the outputs and whether they are

11:23

actually having the intended or the desired effects so kind of traditional information process

11:29

you know we acquire data we put it in a raw store we conform it which means we standardize it to a particular schema we

11:36

may have a variety of different data sources so we can um you know enrich records with data by joining and

11:42

connecting uh fields from other data sources we can aggregate maybe we um

11:48

Group by and compute some statistics maybe we learn some machine learning models but at the end of the day what

11:54

we're uh pushing out is something that is higher level we've we've gone up

12:00

we've said hey all this low-level data without um without some sort of uh

12:06

confirmation enrichment and and processing isn't super useful for for us

12:12

just yet so as those uh serialized uh data sets come out we can think of them

12:18

as feeding into knowledge processing and knowledge processing is fundamentally different from information processing

12:24

under this model because it's circular it is um not item potent it's not

12:29

something where we'd expect the same results if you apply the same operation to this to an object you're going to get

12:36

a new object the kinds of operations that we're interested in are you know compose so combining things decompose

12:42

breaking them down kind of decorating which is an a form of adding additional

12:48

information you know mutating so literally just revising or editing you know producing diffs uh curating which

12:54

may involve filtering certain things out um searching or or discovering new objects or even generating new objects

13:01

and you can see there's a feedback loop baked in here that this stage is meant to be more circular and we'll come to a

13:08

concrete example in a moment that I hope will elucidate the difference but this

13:13

still is feeding into a process um that we are referring to as understanding and

13:20

you can think of this as a a more deliberative process it still involves knowledge objects so you know papers

13:26

open source software projects um again these higher order um objects that aren't just the data the data may have

13:33

been uh collected analyzed plots might have been made you you're you're

13:39

consolidating that information into things that you know describe what's going on or interpret it and and and

13:46

kind of render it ready for input to a human sense making process and so this

13:51

diagram here is a a derivative of some early work on a concept called computed air AED governance where we take

13:58

principles of datadriven decision- making in business and apply them to participatory governance so you can

14:04

imagine having like a data science team or a participatory citizen science team

14:09

within a community doing work to make sense of what's going on and to help make policy make rules make decisions

14:16

and so here we see the knowledge objects as the inputs to the understanding

14:21

process and that that deliberation and discussion process can itself produce knowledge objects so if you do an

14:27

analysis or a scenario plan and you share it with your other community members as support for a proposal that

14:34

you're making uh whether or not that proposal gets passed that analysis or that proposal can effectively be

14:41

recorded serialized and stored as a knowledge object so I guess I should probably um jump back quickly and say

14:48

that reassembles here so those three slides are these three boxes orange uh

14:53

yellow and green and in in effect together they they form a process that result results in action in the world

15:01

and information then incident on the system again now I want to point out

15:06

that this isn't a particularly novel idea especially for communities steeped in open source I would argue that an

15:12

open source software project is already a pretty good example of this and you can start to see some of the pieces

15:17

we're like all right well we have some of the infrastructure of organization here we have code of conduct we have a

15:23

contribution guidelines we have a variety of um documentation about the

15:29

organization itself we have uh semantic versioning for releases software

15:34

licenses and so on and so um what I'm talking about today is how to move

15:41

Beyond something that is pretty well contained within code I would argue that a GitHub repo or a GitHub organization

15:48

combined with a little bit of extra institutional wrapper for example a nonprofit fiscal sponsor like num Focus

15:56

provides most of the core needs of an open source project and and to the

16:01

extent that there are gaps people kind of fill those gaps in by you know instantiating maybe private

16:07

communication channels where they need them you know there was some interesting back channeling when when things go

16:12

wrong like the period when it was um uh one project got a GitHub takedown

16:20

notice last year I think it was Senpai and there was like a whole um kind of

16:27

human response to make sure that that got rectified and it got back up and I I would also consider that to an extent

16:32

part of the social system but not something that you can specify a priori and so as I move into the rest of the

16:39

talk I'm going to be talking about how I think about this problem when we're dealing with communities that are a lot

16:44

more heterogenous they have more stakeholders more diverse work products more diverse working environments um

16:50

really kind of pressing on the the challenge of infrastructuring um with actually some of the insights taken from

16:57

experiences in open source software development where I think um the the best practices around managing

17:04

contributions you know using workflows like like get and establishing specific workflows for specific projects um and

17:12

including how one becomes a contributor with the authority to say merge a poll request Etc are all quite good um as we

17:19

move beyond the environment of managing code where like a particular software project is the thing we're managing I

17:25

think it gets messy and hard pretty fast so um one way to think about the conceptual

17:31

architecture here is to do um uh a little bit of a layering so I like fling

17:38

the social and the technical view side by side and so I I look at the um

17:43

overall system as being uh fundamentally human so when I say evaluate emerging

17:49

properties of soot technical assemblage against Mission Vision and values I'm basically allowing for a um a

17:57

intervention over the system itself so if what's in the small box that I've labeled koi is uh a set of practices and

18:04

Technologies then when you account for the organization and its governance processes the thing that I've labeled

18:10

ooy which is organizational integrated knowledge organization infrastructure I know it sounds like a mouthful it's

18:17

actually because ooy is a a Greek uh root word of economics and refers to

18:22

household and so it's kind of a like Easter egg inside joke thing but anyway we have our uh integ ated system that

18:29

incorporates the human The Entity and the human governance processes and then

18:35

we have this object which contains any number of interfaces um logic and rules

18:41

databases and Integrations or various kinds of data stores ranging from literal databases to web platforms air

18:48

tables Google Sheets you get the idea um but when we look at this from a social perspective um the interfaces are the

18:56

place where you produce the experiences the logic and rules are the place where you embody policies and the databases

19:04

and Integrations they the places that you sort of entrench ontologies so basically practices algorithms and World

19:11

models and as someone who comes from more of a robotics background I'm actually like pretty attuned to the fact

19:17

that um your world models are uh like important grounding like you can't write

19:23

an algorithm that uh tries to implement something that refers to a concept that

19:28

doesn't exist in your ontology and the algorithms are the things that often

19:33

produce the um circumstances or the incentives uh within which the practices

19:39

emerge so it's actually quite difficult to work from the top down here you really have to work from the bottom up

19:45

but then if you're off in your ontology if you're off in your data your data models your um your data dictionaries

19:53

the things that represent the concepts in your in your world then you're also going to run into issues and so one

19:58

thing that we're really interested in in knowledge organization infrastructure is ensuring a degree of flexibility in that

20:05

base level so you need enough um consistency to render these systems

20:10

interoperable or just computable over stable enough that systems aren't breaking when you make changes but you

20:17

still want to preserve flexibility so that to the extent possible ontologies can emerge from practice and therefore

20:25

better fit the communities they're serving and adapt as those communities adapt they grow change fork merge

20:33

Etc uh so the kinds of systems um that that we've been working on they have roughly this uh shape we have uh a group

20:42

of actors within an organization interacting with the system through a set of interfaces uh what they

20:47

experience as a consequence of both data and rules and that technical infrastructure facilitates further

20:54

action onto the world and reading um sensing information from the world and

21:00

we see humans as both following um following rules as well as potentially

21:05

updating those rules and being able to interact directly with each other sharing and learning from their

21:11

experiences um and we've further moving towards a model where we can have multiple instantiations of this kind of

21:18

again sort of conceptual architecture um interacting with each other and we see a lot of this at the social layer and at

21:25

the technical layer so you get social um interoperability when you have common members of communities or when you have

21:32

kind of discussions or negotiations like if you're on a zoom call or in a chat Channel together you're able to communicate kind of human to human

21:38

especially if people have representative Authority with n org they can form Partnerships you know set up projects

21:45

together apply for Grants together um and the technical Communications layer these are effectively data services like

21:51

you open up an API it has a specific um set of queries that it will respond to

21:57

maybe it has an access control regime but you can have technical Communications part of what we're seeing

22:03

with the uh Advent and the adoption of llms is a bit of mixing of this where you could have a technical interface

22:09

talking to a human or vice versa and that opens up both opportunities and challenges and some of what we'll get to

22:16

later is attempts to uh wield that capability but in like a careful and respectful way um the the technology

22:24

that we've been developing for this um it basically um has the goal of being

22:30

instanible governable and interoperable at this stage uh I would say we have a

22:35

bunch of bespoke instances I guess technically three now and some other folks that are that are interested still

22:42

a little bit um kind of a little bit of work you have to have someone with a lot of uh knowledge who's been contributing

22:48

to the project in order to do that but we're moving in a direction where there'll be um sort of software that's

22:53

easier to pull and it's it's more realistic for someone to create their own instance with the out that since

22:59

most of what we're building is not actually software it's a glue for assembling things um it can be a little

23:05

bit tricky um we're pretty excited about it though and we're looking at breaking these down the interfaces by the

23:11

different actors that would interact with those interfaces going all the way from instantiation to kind of the

23:17

technical Administration through the sort of data governance and um kind of tagging and curation through the

23:24

discoverability kind of visualization and exploration as well as uh kind of writing rules and adjusting the um

23:31

internal policym Within These systems and finally um kind of natural language chat interfaces and as you see when we

23:38

get to the concrete examples there's um quite a bit to it but we're pretty focused on using out of the box tools

23:45

and combining them into um kind of interesting assemblages and um now I'm going to come

23:52

back to the point where we we step out of the tech for a moment and think about the other aspects of the architecture so

23:59

these kinds of systems um they don't exist outside of the the human world but

24:04

they still have to have an accountable party and so I've um labeled this blue box um Authority and there's a couple

24:12

versions of this diagram floating around I think in another one it says decision but what I really mean here is like the

24:17

decision-making Authority do you as an entity have the ability to write

24:23

agreements to to enter into them who is responsible for the behavior of the system because anytime we're getting

24:29

involved with developing software data products or Services you know there's an it's really important to understand like

24:36

who um who's responsible for that thing that these Technologies are not in and of themselves um separate from the

24:43

humans that are producing operating maintaining and using them and so that Authority is a is an entity and with the

24:50

stuff that we've built at my firm lock science has some things that we own and operate metago as a legal entity a

24:56

nonprofit kind of owns and operates things and you know in settings where there are projects that are too small to

25:03

have their own entity you end up with a fiscal sponsor or some sort of signatory with legal personhood um again metago we

25:10

basically sponsor a variety of projects that are run by research directors um at num Focus there's a bunch of fiscally

25:16

sponsored projects um but in that case then even though there are individual actors running the projects there's

25:22

still a kind of legal accountability layer associated with that with that fiscal sponsor and so then we step down

25:29

a level into policies this is where we have licenses and other kinds of agreements it could relate to what kind

25:35

of consents are are required um in one of the examples later we'll talk about irbs um but for the most part this is

25:43

where we actually enter agreements so you have to have the authority to enter them in blue and then you enter them in

25:49

at the level in green and this could mean following standards it could mean um entering into agreements to consume

25:56

external apis maybe ones that you're buying um and so on and then as we move

26:01

down to Administration this is like the assis the CIS admin layer like sure you might have a set of rules that say

26:08

you're supposed to do certain things but you actually have humans practices and Technologies say access control regimes

26:16

um that are used to actually Implement those policies and it's important because if the authority is accountable

26:22

for living up to the agreements they make and the policy represents the agreements that have been made then the

26:28

administration is the follow through on that and then finally we get to the the system and here the system is the actual

26:35

Information Technology it's the data in the database it's the files in the Google in um drive it's the whatever the

26:43

thing it is that you're you're actually interacting with and you know we may have a variety of documentation technical documentation as well the

26:50

again the data dictionaries the API specifications um possibly like service

26:55

level indicators and other um other data like kind of about the system um and

27:01

then at the level below we have the various technologies that have been kind of assembled to create that system and

27:08

that's going to include your storage your compute transport and then the agreements with any of the entities that

27:15

you are in fact consuming those services from because we're not just talking about software we're talking about

27:20

Services things that are running which means that they they exist somewhere their physical architecture includes a

27:27

place where you can um invoke them and that each of their components have an implementation either internal to that

27:34

data product or um a service that that that data product consumes um so then we get to the

27:41

question of like how do we get from this General stuff to specifics and you know this comes in part from my work with the

27:48

Data Trust where we were trying to figure out like okay sure the devil's in the details but like which details what

27:53

do we care about well it turns out that we care about where the data is coming from so like what's the phenomena of

27:59

Interest what is it a measurement of and um how was it collected things like well did it come from a chat application is a

28:05

social network is it economic data is it GitHub or Google Docs is it a forum

28:11

discussion like where did it come from um and and what what activities produced it and so then we can ask well then like

28:18

whose activities then like from whom so if it's a forum then it's pretty obvious who the um you authors were at least up

28:25

to the level the strength of the identity within that form Forum um but in other environments it can be less

28:31

obvious whose data it is I mean you often see um Clauses in user agreements

28:37

for applications that just basically say by using this all your data is ours which is you know not ideal but it's the

28:43

current state-ofthe-art in a lot of um applications and for this this state

28:49

we're just like trying to be clear like okay but like who who did this come from and what are their expectations and what

28:55

kind of Agreements are are they party to and to the extent that a user agreement

29:01

that just says you know click wrap by using this you consent to all of these things and you didn't read it anyway

29:08

like I don't generally consider that to be a good model it may be totally legal it's questionable um and so that covers

29:15

the first two bullets which are the kind of from side and then we kind of switch into For What and it continuing with the

29:22

discussion of kind of Click wrap the the there tends to be a kind of and we can use this for whatever we want as the

29:29

part's collecting it and again kind of questionable it seems more realistic uh at least from a end user perspective to

29:37

constrain the expected uses of data to you know like defined purposes like is

29:44

it being used by researchers data stewards other researchers companies nonprofits is it medical data is it

29:50

being used by the you know etc etc um but what's important here is that um

29:57

although it is not commonly the case to distinguish what data that has been collected can be used for um it is

30:05

something that uh one can do and and it's in fact much more realistic to do in smaller uh in smaller uh settings so

30:13

in these knowledge organization infrastructures which are serving specific communities where it's actually

30:19

the members of those communities who are the people the data is from and to the extent that those communities and their

30:26

partners of the people who the dat is going to there's a lot more room for um

30:31

kind of policies that say like hey you can only use this for that um and to the

30:37

extent that you are have a relationship with the entities that are are managing that data um collecting it using it

30:43

organizing it um you may be more willing to share data if you're confident that it will only be used for the things that

30:50

you have said that it's okay to be used for um right so now I'm up to examples

30:57

this should be the fun part um I'm going to talk mostly about an organization called metov in metago we have a board

31:04

of directors we have an executive director uh we have a kind of Finance operations manager that helps with the

31:11

back office we have a community manager that helps with our organization um and

31:16

kind of the activities the Seminars the um you know working groups Etc um and we

31:22

have research directors uh research directors are volunteers like the board is and they lead projects um they some

31:30

are professors some are um entrepreneurs but a variety of people who are kind of

31:36

pushing um pushing the envelope uh within the scope of metag Go's Mission

31:42

um to cultivate tools practices and communities that enable self-governance if you're interested in

31:48

the or check it out the metag of.org is the link um but we're going to be looking at knowledge organization

31:54

infrastructure in metago for the rest of the talk because um it gives a concrete situation an operating context to

32:00

discuss things and So within that operating context we have some challenges and I think those challenges

32:07

are also opportunities so medic includes people from all over the world a mix of researchers practitioners and leaders of

32:14

other organizations diverse experiences and opinions and that means you know great collaborations but also debates

32:20

and arguments we've got you know a website we've got a seminar with recordings on the internet archive we've

32:27

got a public black as a primary access point um there are lots of discussions in public channels but they can be kind

32:33

of Meandering um kind of breett first uh lots of discussions in private channels

32:38

they can be opaque people might not even know about them they're more like working groups people working on projects maybe don't want to be

32:44

interrupted maybe they're focused um but also it's not clear to people that that's even going on if they're not

32:50

there it's kind of an in the room thing um and then we have work Project work that's both curated and emergent so

32:57

research directors are nominated and approved but then are highly autonomous in their projects they secure funding

33:03

from government and philanthropic grants and as a member it can be really hard to keep track of the project portfolio to

33:09

know what's going on you know where and how they can contribute and you can see some aspects in common with the open

33:15

source projects but without the nice clean like locus of coordination in the form of like a GitHub organization or

33:21

get repo there's it's a lot more spread out um so some things they or started to

33:27

do to try to um kind of counteract that so one of the first projects was something called gov base uh gov base is

33:35

uh a data set it's in air table it's actually a bunch of different data sets believe it's licensed under Creative

33:41

Commons the point of contact is the actually one of the founders of metago Josh tan um and it's administrated via

33:47

working groups in slack it's its access controls are managed through air table and the system is really just an air

33:54

table instance um and to try to answer some of these questions like where's the

33:59

data come from manual data entry and our import from Individual researchers spreadsheets or local data stores it's

34:07

primarily for those same researchers um as a broader group maybe

34:12

um because they want to look at comparisons between data sets um I think

34:17

there's some secondary use cases around synergies between the data sets and

34:23

eventually it's going to be um incorporated into this broader metago koipond which I'll talk about as I go a

34:30

little further but actually what I want to emphasize here is that this particular piece of infrastructure kind

34:36

of got out over its skis at the beginning when it was small group and it was only a few data sets it was stewarded pretty well but I think anyone

34:43

who's tried to manage a database that in a non- database technology quickly

34:49

realizes it get it can get out of control um and I sort of see gov basee as an example of something that was both

34:56

very effective and eventually hard to govern and so it may be better suited to

35:02

stewarding data in in other um in other infrastructures uh another data set that

35:08

is curated in metov is um its members directory uh opin and public so it's

35:14

actually displayed on the website it's primarily managed by a community manager gets pushed to the website via web

35:21

developer and uh it's largely part of the onboarding uh so people join they

35:28

can be directed to or Community manager will direct them to an onboarding type form they fill out things that they're

35:33

interested in decide how much information to share about themselves um there's a private version of that data

35:39

set and there's a curated version of it that's actually on the website and you can kind of scroll through it and you

35:44

can click on people's LinkedIn if they chose to share it or see information about their other

35:50

affiliations um some of the more interesting let's say homegrown uh knowledge organization infrastructure in

35:57

metov includes something called telescope um it was originally developed under a grant that uh Ellie renie got

36:04

she's a professor focused on Automation and Society at rmit in Melbourne um it's

36:11

actually was developed to be um consistent with her irbs and it is a set

36:17

of bots that allow you to uh like if you're researching a community that

36:22

exists predominantly online you're able to give them a Emoji tell telescope that

36:28

will flag a message as being important that me that triggers a flow where the person who wrote the message gets a

36:35

consent and the ethnographers get a curation flow and the result is it

36:40

actually builds a data set that was partially developed by the community itself so the community members in the

36:46

Discord are actually participating in the process of determining what's important and organizing it uh for the

36:53

use by The ethnographers Who Would in turn you know provide feedback guidance you know research papers Etc there's a a

37:00

paper um on a project called Source cred that was written based on um

37:06

ethnographic research that included this bot and uh today there's also a slack version of this and as we'll see later

37:12

um we further integrated it with some of the other tools but one of the reasons I like it is because it um emphasized

37:19

including the people who were discussing topics Within These channels um in the

37:25

process of determining like what was relevant um another pretty basic piece

37:32

of um uh organization knowledge organization is Project cards this is

37:37

Project documentation again can be very difficult to Wrangle with a particularly

37:42

uh dacraic kind of community-driven group but here we have uh on our website

37:48

a variety of project cards uh our rd's research directors are theoretically

37:53

required to write them arguably we don't do as good of a job as we should and we're increasingly supported by a

38:00

project manager who helps make sure that they get generated they're public um the

38:05

kind of social pressure happens in the research director's group meeting and ultimately the pushed content has to be

38:13

um added by the the web developer there's a lot of room for automation there but for the time being they're

38:18

pretty simple basically you're filling out a schema making sure you answer a certain set of questions providing a

38:24

image and then it gets uploaded um and the the Practical system here is the

38:29

website itself uh the project slack channels the zoom meetings as well as

38:34

actually any Google Docs and content but the content from the projects themselves is spread pretty wide and we're not

38:41

trying to aggregate or reproduce it and again I'll bring that up in a moment um

38:46

so another thing that metago has is a curated collection of papers and blogs this has been started I want to say like

38:53

six months ago um and a group of people in a working group group in a slack channel are like basically just filling

39:00

in this uh Google sheet and capturing the title and authors and a URL um and

39:07

some metadata and then the checkbox on the left determines whether something has been ingested has it actually been

39:13

um brought into a database because the Google sheet here is really more of an interface it's not the data it's not the

39:20

the core data it's a way of referring to things and saying hey this belongs in

39:25

our data set and these things can be uh embedded we can have vectors uh Vector

39:31

embeddings for use with llms and we also have um or in the process I guess of

39:36

implementing the rid database which is a graph database where you can think of it as a Knowledge Graph but where the nodes

39:43

in the knowledge graph are um are knowledge objects um which uh brings us to

39:50

reference identifiers this is a piece of uh python code that connects with Neo

39:57

for J graph databases that's developed at block science it's under an MIT license it's primarily beneficent

40:03

dictator with Luke who's the the main developer um guiding development with

40:08

contribution from a peer review from other working group members there's a weekly standup and it's a GitHub repo

40:14

with python code um and the kind of material for developing graph databases

40:20

and I think the most important part here though is plugins and this is a a thing where you know we need to get the nodes

40:26

automatically we we don't want to be building these things from scratch so you can curate at the graph database level but you want to be scraping the

40:33

content and that ties back to the previous where look if the um Google sheet is something we know about it's a

40:39

knowledge object then we can actually run a process that says okay go get all

40:44

of these things and create nodes for them as well as um create uh Vector

40:50

store embeddings for them and then finally this brings us to the koi pond which I think is the the exciting um the

40:58

exciting thing here is um organizing this stuff into a coherent system that

41:03

that uh supports accessibility and discoverability of metag of's knowledge of its uh local local knowledge because

41:10

again it's pretty opaque it's spread out everybody's working in their own place and we want to get to a point where um

41:17

you know you have uis like the chatbot you have search interfaces um you have other applications that you can build

41:23

that hit these things via apis and for that we have the vector store embeddings we have the graph database we have um

41:31

search uh we have llm inference via thirdparty um uh apis and then the actual actuators

41:39

and sensors they're bespoke and you know we've been talking about them the things I just shared with you were a bunch of

41:45

the uh potential the current and future data sources that we're Gathering From

41:50

and that they the actuators actually at present are are primarily the um the

41:56

chatbot again that's not that the chat bot's the end goal it's just that that's the thing that people like to interact

42:01

with and so you can see on the right here an example of U an interaction this is from a testing Channel and um this is

42:09

Lee Lee U Elanor doota and she's been working to help develop this project at

42:15

metov um amongst the other team members and so here's a kind of high level maybe

42:21

a bit more cartoonish view of what's going on so we have uh a bunch of data sources where we want to meet the

42:28

members where they are rather than push them into new tools or workspaces so the website is a thing that gets produced

42:34

according to existing processes documents in Google Drive are produced according to existing processes with

42:39

different in some cases many different groups of people there's GitHub um there's lots of other things air table

42:45

as an example um we have the ability to then connect our plugins and run um

42:53

services that write to the rid Graf database and the vector embeddings and

43:00

the koi API effectively orchestrates this so it includes the ability to

43:05

invoke the LL llm inference and in the future potentially other services and

43:11

most people actually interact with this information directly via a chat Buton slack um keeping in mind that slack is

43:19

itself also a data source and for reasons of managing consent we have an instance of the telescope bot so if your

43:25

slack data is being being telescoped and is getting gathered then it's not just

43:31

going to be automatically done without you knowing about it you'll get a DM it will ask for your consent it'll give you

43:36

the option to anonymize and so this is a an example of a slightly more structured flow or in a way a place where we're

43:43

trying to be very explicit about um what people are and aren't contributing and what they are and aren't consenting to

43:50

especially in a space like slack where people are just having conversations and it's not clear that they want everything

43:56

they say to be surveilled and so creating a a mechanism through which uh

44:02

that is filtered and toned down so that people can have more confidence in that

44:07

this system and make their own choices about what actually gets into this system um there's also an interesting

44:14

phenomena that this system feeds back on itself because it's the chatbot acts in slack and slack is sensed so it sees its

44:21

own past and we have not totally um figured out how to study that yet I think it's really interesting I think

44:28

there's no way around that um as an important factor but I I can say we don't really know um what the consequen

44:35

of that are um so that is actually I believe the last slide

