[![](https://yt3.ggpht.com/ytc/AIdro_nZ5ueJjjL96dwUkge4nSaCspm2iFowU1247MfdHiwGuw=s88-c-k-c0x00ffffff-no-rj)](https://www.youtube.com/@ProtocolLabs)

[Protocol Labs](https://www.youtube.com/@ProtocolLabs)

57K subscribers

<__slot-el>

<__slot-el>

<__slot-el>

<__slot-el>

1,796 views Jun 24, 2022

Speaker: David Dalrymple (aka davidad) Abstract: This is a self-contained introduction to the concept of “hypercerts”, a highly versatile new approach to tracking the impact of contributors to nonrival goods and their prospective funders, & facilitating their interaction with mechanisms like retroactive public-goods funding. A hypercert is a kind of “impact certificate” (see    [![](https://www.gstatic.com/youtube/img/watch/yt_favicon_ringo2.png) • Funding the Commons | Impact Certificates ...](https://www.youtube.com/watch?v=viMd7y4bVK0)  ) which represents a particular hypercubic region of a 6-dimensional “public goods space”. The hypercerts framework can support a wide diversity of approaches to impact evaluation, credit allocation, and funding styles, and enable clean interoperability between them (see    [![](https://www.gstatic.com/youtube/img/watch/yt_favicon_ringo2.png) • Interoperable mechanisms for non-rival goo...](https://www.youtube.com/watch?v=acbBeGcevok)  ). This talk kicked off an active initiative now supported by Protocol Labs, Gitcoin, and others to implement and standardize the hypercerts protocol as an Ethereum smart contract. Slides can be found here: [http://github.com/protocol/hypercerts...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbXJja2hnWUtmbk90ek0wclEzVkV1UERZREZtd3xBQ3Jtc0ttNnhfNmk5Ri15QTZtZF96eWxjWW5XMV9CMWpuNEtlZEt4UzhmUEppb0paV0dhdy1Ud0x3b0dnRU1LZGVhOURrVXFkSDFXN0piamw3X01HNHREOHotS2tuZk16OFAwUnVZeWltdm5EWkJCQmVQOFY2OA&q=http%3A%2F%2Fgithub.com%2Fprotocol%2Fhypercerts-docs%2Ftree%2Fmain%2Fstatic%2Fpdf&v=2hOhOdCbBlU)

## 

Key moments

Transcript

## Transcript

0:02

this talk is all new content and i hope

0:04

to leave you with some uh new

0:07

perspectives on what hyper certs are all

0:10

about and why they're a good idea and

0:13

how we could go about making a hyper

0:14

cert system in the real world

0:16

by which i mean on a blockchain

0:19

anyway uh to go into what hypersearch

0:22

are about i'm going to start by stepping

0:24

back for a minute and talking about what

0:26

certs are at all what's the problem

0:28

space that impact certificates are

0:31

trying to address well

0:33

when a contributor performing an

0:34

activity produces a public good it's

0:37

often the case that some members of the

0:39

public such as philanthropists and

0:40

others would be happy to exchange money

0:43

for that impact having been realized but

0:46

unfortunately because it's a public good

0:48

that was produced in the past by this

0:50

point there is no one to give the money

0:52

to and nothing to exchange it for so

0:54

this transaction doesn't really seem

0:56

feasible what the funder really wants to

0:59

do is to send the money back in time and

1:01

retro causally use it to fund that

1:04

activity making it more likely to have

1:06

already taken place

1:07

but unfortunately this seems physically

1:09

infeasible

1:11

but there is the potential of using a

1:13

wormhole

1:16

a less costly idea is impact

1:18

certificates

1:19

this represents the right to future

1:21

retroactive rewards for a public good

1:24

producing activity and whenever an asset

1:26

that represents the right to a future

1:28

cash flow is on the table that induces

1:30

the presence of a special kind of person

1:32

called an investor who specializes in

1:34

anticipating future cash flows and

1:36

exchanging money for them today

1:38

in a transaction where they purchase an

1:40

impact certificate from the contributor

1:42

in advance of the activity by by

1:44

providing the funding signal that

1:46

anticipates the future rewards that are

1:49

caused by the impact and

1:52

caught the the you know closing the loop

1:54

here

1:55

actually also makes that transaction

1:57

possible by giving

1:59

the public someone to hand the money to

2:02

after the fact and a plausible story

2:05

about how doing so actually does retro

2:07

cause the activity to be more likely to

2:10

have been funded via the investors

2:12

anticipatory signal so that's what

2:14

impact certificates are trying to do

2:16

but in reality activities are not

2:19

isolated points like individual

2:21

paintings that one might trade in an nft

2:23

market they're highly interconnected so

2:25

when one of them produces a public good

2:28

it's not always obvious who owns the

2:30

right to that retroactive funding that's

2:33

where hyper certs come in

2:36

i introduced this concept of the public

2:38

goods space

2:39

this is a sort of geometric space with

2:43

many axes for example the time the work

2:46

was done and the scope of the work and a

2:48

hyper cert represents a territorial

2:50

claim in this public good space it

2:52

represents the right to retroactive

2:54

rewards that are attributable to that

2:56

region of public good space

2:58

here we've pictured a two-dimensional

3:00

slice but there are actually more

3:02

dimensions than just that the full space

3:04

in addition to time of work and scope of

3:06

work also includes the time in which the

3:08

impact actually bears fruit and the

3:11

scope of the impact different kinds of

3:13

funders might be interested in different

3:14

sorts of impact ranging from carbon

3:16

capture to averting an existential

3:18

catastrophe from ai

3:20

there's also an axis for the set of

3:22

contributors who are included an

3:24

invariant maintained by the system that

3:26

all contributors who are listed

3:28

consented to the minting of the

3:30

certificate at some point along the way

3:32

and there are different types of rights

3:34

that's another axis most of them will be

3:36

the right to retroactive altruistic

3:38

rewards but some of them will be

3:39

deprived of that right and retain only

3:41

bragging rights while others may contain

3:43

additional rights such as the right to

3:45

passive income from intellectual

3:46

property licensing auctions

3:49

thus the name hyper certs there's really

3:51

a hyper space and a hyper cert as

3:53

depicted here in a square is really a

3:56

hyper cube in that region or a claim on

3:58

a hypercube

4:00

now i'm going to talk about the core

4:02

operation that hyper certs need to

4:04

support which is atomic merge and split

4:06

and i'm going to go through some

4:07

examples so if i have

4:09

two hypersuits call them y1 and y2

4:12

and the owners of those hyper certs want

4:14

to propose a different way of splitting

4:16

up the same region of the public good

4:19

space

4:20

then as long as the the different

4:23

before and after sets add up to the same

4:26

region then this is an allowable

4:28

transaction

4:29

and now these hypersuits exist instead

4:32

here's another example uh here we have

4:35

three incoming hyper certs these add up

4:38

to the same region as these two outgoing

4:40

hypersuits that's a valid transaction

4:44

finally third example the region doesn't

4:46

have to be contiguous this is just the

4:48

same geometric subspace subset of public

4:52

good space not necessarily contiguous

4:55

if we wanted to make it have to be

4:58

contiguous that would just be more

4:59

complexity in the code to check the

5:01

condition and there's no problem all the

5:03

invariants are maintained regardless of

5:05

that so this is another example

5:08

now you're probably wondering why what's

5:11

the point of supporting the seemingly

5:12

bizarre and complicated operation

5:15

well let me give you a user story

5:17

imagine that hypersuits existed as a

5:19

functioning market in 2013

5:21

and uh juan binette is making

5:26

ipfs and

5:28

every quarter he mints a hyper cert and

5:30

offers it to his funder or sponsor in

5:32

exchange for funding

5:34

going along one quarter at a time

5:36

now at some point when this reaches a

5:39

critical mass and the work really begins

5:41

to pay off the funder can make a more

5:43

appealing nft out of this collection of

5:45

hyper certs by merging them into one

5:48

hyper that represents inventing the

5:50

first version of ipfs instead of just

5:53

one particular quarter of work even

5:55

though the funder wanted to do the

5:57

funding transaction one quarter at a

5:59

time while it was happening

6:01

now suppose this nft is successfully

6:03

auctioned off to some other trader

6:05

participating in the hyper cert market

6:08

this trader now considers that there are

6:10

some people out there who would value

6:12

the conceptual development of the ipfs

6:15

concept almost as much as this entire

6:17

body of work

6:18

and yet there are other people who would

6:20

value the actual implementation of the

6:22

first working version of go ipfs almost

6:24

as much as the entire body of work so

6:27

the trader can realize a higher total

6:29

value by splitting along the scope of

6:31

work access and then selling the

6:33

separated hyper certs to different

6:36

parties who have different value

6:37

functions

6:39

rotating now from the time of work

6:41

access into a different axis the time in

6:44

which impact is realized here by default

6:47

both of these hyper certs cover the

6:49

entire scope of time but when it comes

6:52

to evaluating impact assessing what the

6:56

actual impact is or is likely to be well

6:59

there's obviously a difference between

7:00

assessing past impact and future impact

7:02

past impact is about observation future

7:04

impact is more about prediction there

7:06

are completely different sources of

7:08

uncertainty and different methodologies

7:10

so when it comes time to assess it's

7:12

often going to be useful to split the

7:14

hyper certs along the time of impact

7:16

access separating the past impact from

7:18

the future impact and assessing them

7:20

separately

7:21

and when another assessment is performed

7:23

the hyper certs which had previously

7:25

been the future it will make sense to

7:27

split them again into the newly passed

7:31

impact and the still in the future

7:33

impact and assess those separately

7:36

because the times at which assessments

7:38

happen are not necessarily fixed up

7:40

front it's valuable to be able to

7:42

perform these splits dynamically in the

7:44

future

7:47

now that's a segue into another benefit

7:49

of the hyper cert scheme which is to

7:51

make the job of impact assessors a

7:53

little bit easier if i were hired to

7:56

assess and impact nft at least for me

7:58

some of my first questions would be like

8:00

you know are we talking about past or

8:02

future it can we split those up somehow

8:04

what scope of work exactly is covered

8:06

who were all the people that were

8:07

necessary to make it happen did they all

8:09

agree to this did they agree to the

8:11

allocation that's being proposed that's

8:12

listed on the certificate

8:14

when when was when was the work that's

8:16

supposed to be evaluated done am i

8:17

supposed to be considering the prospect

8:19

of future work on this project am i

8:21

supposed to be evaluating like last

8:22

month can we please like freeze an

8:24

interval of time so that i can take some

8:26

space to consider with the work that had

8:28

been done in that period without it

8:30

changing as i'm evaluating it

8:32

so hypersearch answer a lot of these

8:34

questions right off the bat

8:36

and they make the others a lot easier it

8:39

doesn't immediately answer the question

8:42

did all of the people who were necessary

8:44

to make this happen sign on because some

8:46

people could just be left out

8:48

the impact assessors just like in an

8:50

ordinary impact certificate market will

8:51

have to do some interviews and do some

8:53

digging to satisfy themselves that there

8:55

aren't people who are being unjustly

8:57

left out but other than that the hyper

9:00

basically does the bookkeeping to keep

9:01

track of at least that the people who

9:03

are listed signed with their

9:04

cryptographic identities and agreed to

9:06

the split and so on

9:09

another advantage is for a type of

9:11

participant called a donor a donor wants

9:14

to contribute to a project

9:16

and not receive anything any tradable

9:18

asset in return there may be all sorts

9:20

of reasons why that's the case but they

9:22

do want to have some on-chain bragging

9:24

rights say like hey

9:25

i'm one of the donors who supported this

9:28

hypersearch supports this by default

9:31

because a donor can engage in a

9:32

transaction where they merge into the

9:35

contributor list a hyper cert that they

9:37

meant themselves in exchange for a

9:40

transfer of eth to the existing project

9:42

team and leave the ownership of the

9:44

entire hypercert in the hands that it's

9:46

already currently in without taking any

9:48

extra for the donor this is a

9:49

transaction which would then be on the

9:51

chain and that that donor would be

9:54

listed as one of the contributors in the

9:55

project from there on out it's sort of

9:57

like

9:58

a transaction in which you get listed in

10:00

the special thanks at the end of a

10:02

youtube video for being a patreon

10:04

subscriber we could even imagine without

10:06

changing any of the underlying hypercert

10:07

framework building smart contracts on

10:09

top of this which would automate a

10:12

patreon-like system where every time

10:13

there's some new piece that comes out

10:15

and a new hyper cert is minted a

10:17

transaction takes place some eth is

10:19

taken you get listed on the special

10:20

thanks list i.e the contributor

10:22

dimension and so on

10:24

so these are just a few examples of some

10:26

unusual use cases that we've thought of

10:29

since devising the hypersearch framework

10:30

which it already permits because

10:32

hypersearch sort of seemed to

10:35

accommodate all the transaction patterns

10:37

that you would expect like oh that

10:39

should be allowed that should be

10:40

something that you can do with property

10:42

rights in public good space

10:43

and that's basically what hyper certs

10:45

are they're a representation of

10:47

allocation of property rights in public

10:48

good space that allow exactly all the

10:50

things that don't break some fundamental

10:52

invariance like every point in space is

10:55

either unclaimed or fully claimed

10:58

the contributors for a given slice of

11:01

public good space have to approve

11:02

minting in that slice

11:04

claimed space once it's claimed never

11:06

becomes unclaimed you can burn a

11:07

certificate but you can't make it

11:09

unclaimed such that someone can show up

11:11

in the future and claim it again

11:12

owners must approve transfers very basic

11:15

and variant of any kind of bookkeeping

11:17

system

11:18

so basically hypersuits are a great

11:20

platform for experimentation with

11:22

different kinds of mechanisms and

11:24

different kinds of transaction patterns

11:26

because it just takes care of the

11:27

bookkeeping and make sure the invariants

11:30

are upheld while providing a great

11:32

amount of flexibility for all sorts of

11:34

different patterns and ways of getting

11:36

public goods provisioned

11:38

and it will also enable like the

11:40

different experiments to interoperate

11:43

with each other to exactly the extent

11:45

that such interoperability would make

11:47

sense from a property rights point of

11:49

view

11:50

another thing is

11:52

i don't have too much time to talk about

11:53

this hypersearch is only about 10 of

11:56

what i work on and i also think about a

11:57

lot of other mechanisms for provision of

12:00

public goods and hyperservice integrates

12:01

well with those part of that's about

12:03

intellectual property open auction based

12:06

licensing

12:07

part of that is about causal modeling of

12:09

impact with formal road mapping and part

12:11

of that is about mechanisms for

12:13

collectively allocating attention based

12:15

on future

12:17

you know anticipations of reward based

12:18

on causal models and so on all of these

12:20

would be much easier

12:22

with hypersearch than with an

12:23

unstructured kind of impact certificate

12:26

okay final question how do we do this so

12:30

to answer that i'm going to start by

12:31

talking a bit about erc 1155 which i'm

12:34

sure you've all heard of

12:35

and it's one of the first things that

12:36

people suggest as a way of approximating

12:38

something like a hyper surge ledger

12:40

it's the latest sort of ethereum

12:43

community accepted standard for

12:44

non-fungible and also semi-fungible

12:46

tokens hypersuits are not exactly

12:49

non-fungible in that i think it's

12:51

important for hyper certs to be

12:52

infinitely divisible or you know

12:54

divisible up to 10 to some large number

12:56

um but they are semi-fungible because

12:59

there are many different types of hyper

13:00

suits which are not interchangeable with

13:02

each other

13:03

required operations for your client 55

13:05

are just transferring from an address to

13:08

an address importantly a particular

13:11

token type an amount and then some

13:13

callback data

13:15

and getting the balance how much does a

13:17

given address own of a given token type

13:20

and there's batch versions of those and

13:22

there's a couple functions to delegate

13:23

authority to approve transactions and

13:25

that's it those are the interface

13:27

operations required for erc 155

13:30

so some key facts about this that i

13:31

didn't know when i gave my last talk at

13:33

funding the commons in merch

13:35

one erc 1155 contract doesn't just

13:39

manage a single token type like erc20

13:41

does it manages a whole suite there is

13:43

this argument you went 256 so your

13:46

256-bit token id that you can use to

13:49

specify which token you're talking about

13:51

to a single contract which manages all

13:53

of them that's important because the

13:54

atomic merchant swap transaction is one

13:56

that cuts across many different types of

13:58

tokens and even creates and destroys

13:59

types of tokens so there needs to be in

14:02

order for us to be practical a single

14:03

smart contract that manages all the

14:04

tokens and erc 1155 allows that

14:07

also an important fact that i didn't

14:09

quite realize a few months ago is erc

14:11

1155 is just a protocol specification

14:13

it's not a piece of code there is of

14:15

course a piece of code it's written by

14:16

open zeppelin that is often copied and

14:18

used to implement the interface for

14:20

standard

14:21

nfts and sfts but it's

14:24

it's not required that you copy that

14:26

piece of code and have those behaviors

14:28

to comply with the specification

14:30

the token types in erc 155 don't have to

14:33

be urls it is i was over indexed on how

14:36

everyone associates nfts with actually

14:38

just naming a single url and saying okay

14:40

now this is a tokenized thing it would

14:42

be a little bit difficult to wedge this

14:44

idea of regions of this high dimensional

14:45

space into a uri but that's not how it

14:48

has to be in fact uris are an optional

14:50

extension to erc 1155 and that extension

14:53

is implemented not as a data field but

14:55

as a function so it can be

14:57

programmatically constructed based on

14:58

data that's tracked

15:01

in other formats so our hypersearch

15:03

contract can track all the extra

15:04

structured data about what region of

15:06

public good space is represented by each

15:08

token id that's been used so far and

15:12

finally erc 1155 doesn't mandate a too

15:15

strict kind of invariant that would be

15:17

appropriate if it were really nft only

15:20

it doesn't for instance mandate that

15:22

tokens not suddenly disappear for

15:24

reasons unrelated to any operations

15:26

requested through the interface that's

15:28

actually fine with erc 1155 and that's

15:31

great news for hyper certs because when

15:32

someone wants to invoke an atomic merge

15:34

and swap transaction that's not part of

15:36

the erc 155 interface and it'll cause

15:38

some tokens to spontaneously disappear

15:40

that's fine because we know what our

15:42

invariants are as a hyperspirit market

15:44

and erc 1155 will just handle it and uh

15:47

and and report it to its

15:50

report events that these tokens have

15:52

been transferred now

15:54

so since hyper certs should support

15:56

functions the basic functions like

15:58

getting the balance of how much of one

15:59

somebody owns and transferring an amount

16:01

that somebody owns to someone else

16:03

without doing any fancy stuff then hyper

16:05

certs should be erc 1155 compliant in

16:08

addition to providing implementations of

16:10

a more complex interface for atomic

16:12

merchant swap that's hyper specific

16:15

the data structures and the algorithms

16:16

for doing the boolean algebra to check

16:17

that an atomic merging swap is valid are

16:20

not trivial but it's far from a grand

16:21

challenge

16:23

my biggest risk is that it might cost a

16:24

lot of gas this is something that you

16:26

know what we should work out try doing

16:28

some implementations i'm optimistic that

16:30

there will be something that's not too

16:31

hard to manage

16:32

my current estimate in terms of

16:34

complexity is that this will be

16:35

somewhere between basically three to

16:36

five times as complex as vanilla eoc

16:39

1155 which is really not that bad

16:41

although it's going to be expensive to

16:43

formally verify something like that but

16:45

we can get started without doing any of

16:47

that

16:48

so then complying with this standard uh

16:51

means that we'll be able to integrate

16:52

with a lot of platforms um directly

16:55

without doing anything um and it also uh

17:00

besides openc and wearable um ixo and um

17:04

uh and and others um use erc155 there

17:07

will be work to do to make that

17:09

integration a good experience

17:11

um there's also a need for a specific

17:15

web platform that's specific to um doing

17:18

these hyper cert specific operations and

17:20

this will require a lot of so sort of

17:22

thoughtful development of a product

17:24

across all spectrums and then there will

17:26

also be work to do to convince

17:28

people on various sides of this market

17:31

that they actually should mint and trade

17:33

and buy hyper certs

17:35

and not just use

17:37

nfts for science and that sort of thing

17:40

basically marketing

17:42

so in summary

17:43

the wish lists

17:45

for hypersearch for this year there's a

17:48

a need for a experienced evm contract

17:51

developer to to actually

17:53

implement the interface there's a need

17:56

for for product user experience web

17:58

interface development a back end to

18:00

connect the web interface to the actual

18:02

ethereum blockchain

18:04

and some kind of community manager so if

18:06

you or anyone you know might be

18:07

interested in helping us make hyper

18:09

search a reality please reach out to

18:11

me or hulkabrammer who is also working

18:13

at protocol labs and spearheading our

18:15

hypersuits effort

18:17

thank you

18:18

[Applause]