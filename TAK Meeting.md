---
Date Created: "2025-06-03 14:16"
Last Updated: "2025-06-03 14:16"
tags: 
Index: 
Topic: 
Status: Unweathered
Published: true
Author:
---
---

Here are **refined, ready-to-use talking points** for your meeting with **Daniel Fountaine** that show you’ve done your homework and are looking to build strategically:

---

### 🧭 **1. Framing the Goal**

> “The core mission for R4Dash // R4Go is ensuring continuity of operations—especially during disasters. We're exploring how to ensure our volunteer coordination platform can remain useful when infrastructure is degraded. TAK seems like the most battle-tested ecosystem to interoperate with.”

---

### 🔄 **2. Interoperability Vision**

> “Rather than compete or reinvent what TAK does well, we’d love to explore **interoperability**. That might look like:

- TAK Server as a backend we can sync into
    
- A plugin that bridges our platform into ATAK
    
- Or even mirroring core TAK resilience features in our own stack, if we must go fully offline”
    

---

### 🧰 **3. Options on the Table**

**We’ve identified 3 main technical paths:**

|Option|Summary|Pros|Cons|
|---|---|---|---|
|**Plugin**|Build an R4Go plugin for ATAK-CIV|High interoperability; full access to peer mesh|Plugin dev overhead; TAK UI complexity|
|**Server Sync**|Use TAK Server as backend + R4 frontend|Field-tested backend, R4 UX layer|Requires TAK server ops + integration effort|
|**Own COP**|Mimic TAK stack for full control|Total flexibility & no ATO bottlenecks|High lift; less trusted in gov circles|

> “We’re leaning toward a **hybrid model**: use R4Go for sunny skies, and handshake into TAK during disasters.”

---

### 📦 **4. Plugin & TPC Build Notes**

> “We’ve already scoped the TAK Third-Party Pipeline (TPC). We understand how to:

- Use the `atak-gradle-takdev` plugin
    
- Follow the proper Gradle + manifest setup
    
- Submit signed plugins that work in ATAK-CIV  
    So we’re not afraid of doing a plugin if that’s the best route.”
    

---

### 💬 **5. UX & Frontend Differentiation**

> “We think one of our biggest contributions to the TAK ecosystem could be a **friendlier, civilian-facing UI** layered on top of WebTAK or TAK Server. We’d retain TAK’s mission-resilience while improving community engagement, trust-building, and clarity during peacetime.”

---

### 🔐 **6. Deployment + Governance Considerations**

> “We’re aware that full operational use requires ATO, and that TAK-MIL is off-limits. So we’re framing this purely for:

- Open source ATAK-CIV use
    
- Civilian disaster response networks
    
- Peacetime volunteer vetting + readiness prep”
    

---

### 🎯 **7. Specific Questions for Daniel**

Ask Daniel:

- “Which of these 3 options do you think gives us the best short-term feasibility?”
    
- “Have you ever seen a WebTAK or TAK Tracker implementation used in a civilian org?”
    
- “Any gotchas in trying to do TAK Server integration via CoT / overlays?”
    
- “Are there any non-obvious ways to extend TAK’s capabilities with external APIs or plugin-based data bridges?”
    

---

Let me know if you’d like a PDF one-pager or diagram visual for screen-sharing. You’re going into this with **clarity, alignment, and a real opportunity for collaboration**.


---

# Notes

CajunNavyRelief
CajunNavy2016 - supplies logistics etc.
CajunNavyGroundforce bad, 

Micah - Engineering student he met at CNR 
- could be a cool reference

Now with RancherNavy; 2022 texas wildfire fighting
- onboarding: select active vs reserve status, changes training pathway
	- reserve: basic then idle prior to activation
- ticketing "almost nonexistant"
	- webform -> google sheet -> map
	- airtable bad, accessDB alternative?
- funding: donations mainly
	- paypal giving fund
	- social media interactions are key
	- 

Orgs:
SOS - ticketing platform, map data, supposed to do volunteer intake and onboarding
- built out for one testcase only for now
	- made for emergency RVs for displacement
- rancher navy is going to pilot for them next
	- animal rescue and animal related supplies
	- branching into people things too
- Contact Victoria with conversacore in AidArena
	- SOSconnect.org
	- Jonathan is the CEO, may be open to work as well



TAK
- State agencies already use this


Fema ICS form - tracks activity and tasks completed
- ICS form 214, provide that to people for trust
- County EMA would love that form
	- file for reimbursment
- SOS is looking at this
- FEMA training
	- ICS - 100, 200, 
	- NIMS - 700, 800
	-  Create a FEMA Student account
	- command structure; 
	- areas of response all have their own paperwork
		- supplies
		- operations
		- etc.

Caputring people
- target organizations such that they can target volunteers

Specification of type of relief = different fields


Emergency management & emergency response softwares, but would require in depth customizable
- not enough time to customize
- import export after depreciation of any v1 is a big issue

webEOC
10-8 systems
nogginOCA?
	noggin.io

[Salamander](https://www.salamanderlive.com/index.php/industries/emergency-management)
- inventory management
- staff etc. as well, and ID and badging
	- QR on back of badge, shows credentials as well
- walkup as well, autopopulate from drivers license
- 

---
# transcript
0:00

(Hopefully Abysmal (Elryan The Explorer)) Okay, cool, cool, (Hopefully Abysmal (Elryan The Explorer)) cool. Um, and then if we need to get into anything that needs the recording to be

0:08

(Hopefully Abysmal (Elryan The Explorer)) stopped, just feel free to let me (Daniel Fountaine) Well, - (Hopefully Abysmal (Elryan The Explorer)) know. Okay. Yeah. Uh, Daniel, you're just going

0:16

(Hopefully Abysmal (Elryan The Explorer)) to start on your background and stuff. Um, and then Ben, if you want to introduce yourself real (Ben Smith) right

0:24

(Daniel Fountaine) dude. - (Hopefully Abysmal (Elryan The Explorer)) quick. Yeah. Yeah. - (Ben Smith) now. Sure. Yeah. Hey, uh good to meet you guys. (Ben Smith) Good to meet you, Daniel. Uh I met Alan just a couple weeks ago.

0:32

(Ben Smith) Um and uh if you've heard of uh Daniel Schmackenberger (Ben Smith) um I did some work for his institute for a little bit about metacar crisis like

0:40

(Ben Smith) curriculum and understanding the existential risk space (Ben Smith) and um so we kind of worked in the civic landscape here and there and uh

0:48

(Ben Smith) it's just in the last couple months that I was like you know what I think the (Ben Smith) appropriate response to the meta crisis is to light people up and get them

0:56

(Ben Smith) excited about getting engaged in their local communities and understanding their local bio (Ben Smith) regions. And so I thought I'd try to explore developing an app

1:04

(Ben Smith) that would do that that would make it really fun and engaging to make friends (Ben Smith) with communities and uh learn about their local regions. And so I just

1:12

(Ben Smith) started pursuing that metan and then Jesse of R4 and now we're kind of (Ben Smith) combining efforts to build that up. So it's good to meet you. Excited

1:20

(Ben Smith) to hear about your background with us. (Daniel Fountaine) Good to meet you as well. See if I

1:28

(Daniel Fountaine) can maybe get this thing to (Daniel Fountaine) work. Of course

1:36

(Daniel Fountaine) not. Um, so, uh, (Daniel Fountaine) I guess a little bit about my background. I've been in

1:44

(Daniel Fountaine) IT for 18 19 years, something like (Daniel Fountaine) that.

1:52

(Daniel Fountaine) Um, I've worked for for HP and um, (Daniel Fountaine) Loheed Martin, the University of Texas at Arlington.

2:00

(Daniel Fountaine) um develop partnerships with a lot of different people from (Daniel Fountaine) a lot of different uh companies like uh you know Dell and

2:08

(Daniel Fountaine) HP and stuff like that. (Daniel Fountaine) Um I've done a lot of different stuff kind of kind of like you said

2:16

(Daniel Fountaine) in your video like a a jack of all trades, master of none. That's kind of where I sit. (Daniel Fountaine) like I do um coding and scripting

2:24

(Daniel Fountaine) and web design and graphics and video editing and (Daniel Fountaine) uh you know hardware support and stuff like that. Um in my home lab here

2:32

(Daniel Fountaine) I have two older Dell servers that I use just to play around with. (Daniel Fountaine) Uh one of them has like 128 gigs of RAM and like no

2:40

(Daniel Fountaine) hard drive space and the other one has like you know terabytes of hard drive space and no RAM. (Daniel Fountaine) uh just how how I got acquired everything and

2:48

(Daniel Fountaine) built everything in my little bitty home lab. Um I've (Daniel Fountaine) done a lot of work in the disaster

2:56

(Daniel Fountaine) response space both as like an IT director (Daniel Fountaine) and building a team to manage a large organization and

3:04

(Daniel Fountaine) support everything um for (Daniel Fountaine) their IT needs and infrastructure. There's a lot of tech in the back

3:12

(Daniel Fountaine) end of of going out and rescuing people that a lot of people don't realize and (Daniel Fountaine) understand. And that's kind of where I've positioned myself and and

3:20

(Daniel Fountaine) grew my skill set in the space. I've done disaster relief work (Daniel Fountaine) for seven, eight years, something like that,

3:28

(Daniel Fountaine) almost a decade. Um, I (Daniel Fountaine) started with Harvey and I was boots on the ground in Harvey. And then

3:36

(Daniel Fountaine) when I got back home, I realized there's a lot to be desired from the (Daniel Fountaine) the backend infrastructure. And that's where I kind of like plugged in and set out to

3:44

(Daniel Fountaine) do some really cool stuff. I was the IT (Daniel Fountaine) director or deputy IT director and then IT director for Cinjun

3:52

(Daniel Fountaine) Navy Relief, which is uh one of the (Daniel Fountaine) larger I would say one of the larger organizations in the

4:00

(Daniel Fountaine) space. Um there's probably about (Daniel Fountaine) six different organizations that use Kinjun Navy in their name

4:08

(Daniel Fountaine) somewhere. So uh a lot of people don't realize that and so they get the moniker (Daniel Fountaine) just cinjun navy for a lot of those different orgs and and

4:16

(Daniel Fountaine) groups. Some of them are are not on the level and some of them (Daniel Fountaine) are. And that was an interesting thing to

4:24

(Daniel Fountaine) tackle is like to to recognize who's with who and figure out that (Daniel Fountaine) that trust situation. Uh you know KJ Navy 2016

4:32

(Daniel Fountaine) is a good organization. Uh Kinjun Navy ground force and I think (Daniel Fountaine) they changed their name to like humanitarian ground force or something like that

4:40

(Daniel Fountaine) recently. Um they're not good to work with. (Daniel Fountaine) Um there Kinjun Navy 2016 also goes by like

4:48

(Daniel Fountaine) Pinnacle Search and Rescue and that's their like actual (Daniel Fountaine) technical search and rescue folks. Um and then the

4:56

(Daniel Fountaine) Kinjun Navy 2016 is kind of like the supplies and logistics and stuff (Daniel Fountaine) like that. Um, Kinjun Navy Relief

5:04

(Daniel Fountaine) has gone through some growing pains because they went from like a really small (Daniel Fountaine) like seven, eight people group to to be uh

5:12

(Daniel Fountaine) upwards of five 6,000 volunteers and in (Daniel Fountaine) organizing all of that. Um, and I think throughout their growing

5:20

(Daniel Fountaine) pains, they've made some some poor choices and have positioned themselves (Daniel Fountaine) in a not so great place. Um, and I

5:28

(Daniel Fountaine) like I said, I spent a lot of years with that organization and so like I have a lot of respect for the (Daniel Fountaine) people, but there's some bad choices that have been made in in

5:36

(Daniel Fountaine) that group. Um, which is kind of why I left that group and I'm now (Daniel Fountaine) with Rancher Navy, which kind

5:44

(Daniel Fountaine) of did the same thing that everybody else was doing and put Navy at the end of their group. (Daniel Fountaine) Um, Rancher Navy got sto started in

5:52

(Daniel Fountaine) 22 in response to Texas wildfires and they've kind (Daniel Fountaine) of grown and expanded since then. Um, so far

6:00

(Daniel Fountaine) we've done everything from hurricane Helen work and you know (Daniel Fountaine) more wildfire work cuz I think it

6:08

(Daniel Fountaine) was 23 or early early. (Daniel Fountaine) No, it was 23 they had that huge wildfire in the Texas

6:16

(Daniel Fountaine) panhandle that we responded to and um, you know, we've done (Daniel Fountaine) tornadoes and and straight line wind

6:24

(Daniel Fountaine) responses and stuff like that um all over. We've (Daniel Fountaine) done stuff in Oklahoma and Louisiana and Texas. Like we're

6:32

(Daniel Fountaine) based here in Texas, but uh we've gone all the way up to (Daniel Fountaine) Tennessee and North Carolina and stuff like

6:40

(Daniel Fountaine) that. Um I have a little bit (Daniel Fountaine) of military background and stuff like that. I don't I don't know if y'all have any questions about anything

6:48

(Daniel Fountaine) that I've covered so far, but uh I've got a a good (Daniel Fountaine) bit of IT experience. Like I said, just about 20 years and about a decade in

6:56

(Daniel Fountaine) in disaster response. Um, and built (Daniel Fountaine) a lot of relationships and contacts and stuff

7:04

(Daniel Fountaine) like that over the years. So, if there's something that I can I can help with or (Daniel Fountaine) uh maybe even like my skills or my perspective as being

7:12

(Daniel Fountaine) somebody who's done both IT and disaster response at the same (Daniel Fountaine) time, I'm I'm happy to help where I

7:20

(Daniel Fountaine) can. - (Hopefully Abysmal (Elryan The Explorer)) 100%. Um I mean like as stated in the video like we're definitely (Hopefully Abysmal (Elryan The Explorer)) like looking for people who have had experience in IT and disaster

7:28

(Hopefully Abysmal (Elryan The Explorer)) relief. So you fit the bill perfectly, right? Um one thing that does (Hopefully Abysmal (Elryan The Explorer)) immediately come to mind is like we'll definitely probably be reaching out to you for like um

7:36

(Hopefully Abysmal (Elryan The Explorer)) getting thoughts on asynchronous engagement. Um that being like things that (Hopefully Abysmal (Elryan The Explorer)) one can do on like the backend side of things um like

7:44

(Hopefully Abysmal (Elryan The Explorer)) for like information management and like volunteer coordination. (Hopefully Abysmal (Elryan The Explorer)) Um, if that seems like that would be right like in your alley.

7:52

(Daniel Fountaine) Yeah, like I - (Hopefully Abysmal (Elryan The Explorer)) Um, I don't know. But (Daniel Fountaine) said, any anywhere I can plug in to help out where like my skills would be

8:00

(Daniel Fountaine) useful or my perspective or my insight or my contacts and connections, - (Hopefully Abysmal (Elryan The Explorer)) yeah. (Daniel Fountaine) like wherever I can help. I I

8:08

(Daniel Fountaine) haven't looked at the GitHub and I don't know (Daniel Fountaine) exactly what you're doing, but I have a pretty good idea based on, you know, what you covered in

8:16

(Daniel Fountaine) your video. Um, I I do want to say - (Hopefully Abysmal (Elryan The Explorer)) Yeah, they get pretty early, (Daniel Fountaine) that I do want to say that that I've looked at some of the - (Hopefully Abysmal (Elryan The Explorer)) but

8:24

(Daniel Fountaine) other stuff that's coming together from some other uh groups that are (Daniel Fountaine) putting some some software together to help uh and there may be a way to

8:32

(Daniel Fountaine) to integrate or plug in with what they're doing or uh you - (Hopefully Abysmal (Elryan The Explorer)) yeah. Yeah. Yeah. (Daniel Fountaine) useful crossover there. Um, but there's a an or

8:40

(Daniel Fountaine) called uh I think it's SOS something or (Daniel Fountaine) something SOS.

8:48

(Daniel Fountaine) Um I don't have y'all heard of it? No. Okay. - (Hopefully Abysmal (Elryan The Explorer)) That's a pretty pretty (Daniel Fountaine) So SOS is - (Hopefully Abysmal (Elryan The Explorer)) broad

8:56

(Daniel Fountaine) is uh similar to like a ticketing platform where you have your (Daniel Fountaine) your map data and stuff like that. And um

9:04

(Daniel Fountaine) it's supposed to and I haven't seen a whole (Daniel Fountaine) lot of the backend and what it looks like but from what I have seen it will do like

9:12

(Daniel Fountaine) volunteer intake and onboard folks. uh and (Daniel Fountaine) work through the process and build out that process the way that you want it to work. - (Hopefully Abysmal (Elryan The Explorer)) Okay.

9:20

(Daniel Fountaine) So for for ranch or navy, our process is that like you (Daniel Fountaine) submit an application and then you have to select like a an

9:28

(Daniel Fountaine) active or reserve status and that determines your training path and then the (Daniel Fountaine) active status gets a lot more training up front and geared

9:36

(Daniel Fountaine) towards you know going to the field and doing the thing or geared (Daniel Fountaine) towards uh becoming a lot more active in the organization. the reserve

9:44

(Daniel Fountaine) has some basics training up front uh and then (Daniel Fountaine) kind of idles down until there's a need

9:52

(Daniel Fountaine) for that volunteer to be activated and and (Daniel Fountaine) deployed and um so so SOS does

10:00

(Daniel Fountaine) the the volunteer onboarding it does tickets (Daniel Fountaine) uh so requests for assistance whether that's rescue or

10:08

(Daniel Fountaine) uh supplies or or (Daniel Fountaine) whatever Um, it does the tickets, it puts them on a map and it makes uh

10:16

(Daniel Fountaine) everything a lot easier to understand and to to break down from like (Daniel Fountaine) a dispatcher backend perspective on where do you need to send

10:24

(Daniel Fountaine) folks and it allows you to, you know, map that out (Daniel Fountaine) and see where your hotspots are and stuff like that. There's a lot of different uh layers and

10:32

(Daniel Fountaine) integrations to it. Um, but their their (Daniel Fountaine) platform is not uh it's

10:40

(Daniel Fountaine) not 100% active right now. I think they have it uh built out for (Daniel Fountaine) one uh test case and they are working with that

10:48

(Daniel Fountaine) organization to build that out a little bit better and when they move to the next (Daniel Fountaine) phase I think you know my organization Rancher Navy is

10:56

(Daniel Fountaine) is looking to um maybe test pilot some (Daniel Fountaine) stuff for them because we have a little bit different use

11:04

(Daniel Fountaine) case than what their their current test case is. So (Daniel Fountaine) their current test case is like RV RV something uh

11:12

(Daniel Fountaine) it's like emergency RVs or something for people who are (Daniel Fountaine) displaced. Um and then ours

11:20

(Daniel Fountaine) is rescue animal rescue (Daniel Fountaine) and animal vet related supplies. Um

11:28

(Daniel Fountaine) and we also so our organization focuses (Daniel Fountaine) on rural agricultural and underserved communities.

11:36

(Daniel Fountaine) So, we get a lot of that that a overlap with the people stuff. So, like we (Daniel Fountaine) haven't really had a whole lot of requests for the people

11:44

(Daniel Fountaine) stuff because we're positioned to help with the animal stuff, but (Daniel Fountaine) we since I joined the organization, we've had

11:52

(Daniel Fountaine) um basically been testing doing more people related (Daniel Fountaine) stuff. Uh and I think we've proven that we

12:00

(Daniel Fountaine) are also well positioned to to take care of that. We've we've (Daniel Fountaine) took care of I can't I can't remember the number off the top of my head, but

12:08

(Daniel Fountaine) it was something like uh $20,000 worth of generators and (Daniel Fountaine) buddy heaters and propane tanks and uh you know,

12:16

(Daniel Fountaine) carbon monoxide detectors and all that stuff that goes with generators and (Daniel Fountaine) heaters. Um and and got those deployed to

12:24

(Daniel Fountaine) a community that was completely cut off in North Carolina. - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) It was a

12:32

(Daniel Fountaine) Batcave. Um they were they were just I think a little (Daniel Fountaine) bit further down the mountain than Jimny Rock. So, everybody was trying to do stuff with Jimny

12:40

(Daniel Fountaine) Rock and it's like less than two miles down the road, Batcave was cut (Daniel Fountaine) off. They had uh four roads in and out of Batcave and they all

12:48

(Daniel Fountaine) had either been washed away completely or the bridges were completely gone (Daniel Fountaine) or whatever. So, they were just as cut off as Chimney Rock,

12:56

(Daniel Fountaine) but Chimney Rock got all the press. So, nobody was helping (Daniel Fountaine) Batcave. So, we got out there and we helped Batcave. got our vet techs up there to look

13:04

(Daniel Fountaine) at some stuff and and take care of some critters and and we did uh like I (Daniel Fountaine) said some people work there and got some needed assistance to

13:12

(Daniel Fountaine) that area and in turn, you know, built a a really good connection (Daniel Fountaine) with the volunteer fire department in Bat Cave, which is their only emergency

13:20

(Daniel Fountaine) response. Um and I (Daniel Fountaine) think um I think it was one of the phone calls that I made

13:28

(Daniel Fountaine) also got on the Starlink, too. So, they had internet like day two after I showed up. (Hopefully Abysmal (Elryan The Explorer)) Nice.

13:36

(Hopefully Abysmal (Elryan The Explorer)) Well, heck yeah. No, I'm I'm genuinely intrigued to look into this SOS platform. (Hopefully Abysmal (Elryan The Explorer)) Um it does genuinely seem like they're doing what we were trying to

13:44

(Hopefully Abysmal (Elryan The Explorer)) do um functionalitywise. Um the only thing that we were (Hopefully Abysmal (Elryan The Explorer)) trying to posit potentially on top of that is um any like sort of sunny

13:52

(Hopefully Abysmal (Elryan The Explorer)) skies applications of this kind of tech. Um, so potentially that could be something we (Daniel Fountaine) So, - (Hopefully Abysmal (Elryan The Explorer)) could collaborate with them for. Um, but yeah, I'm super

14:00

(Hopefully Abysmal (Elryan The Explorer)) intrigued. - (Ben Smith) Yeah. Um (Ben Smith) I if you might don't mind um like what

14:08

(Ben Smith) we've I think been particularly curious about is (Ben Smith) um like I've worked in and around the civic space quite a bit

14:16

(Ben Smith) and a a lot of it people aren't aware of it unless they need to be (Ben Smith) if they're hit by a disaster then maybe they'll be aware of it. It doesn't get pressed and

14:24

(Ben Smith) a lot of people aren't aware of it. Doesn't make news. You don't see some of these like (Ben Smith) civic superheroes on the like Joe Rogan or anything,

14:32

(Ben Smith) right? And what we were really trying to (Ben Smith) imagine is an app that would streamline

14:40

(Ben Smith) volunteer efforts in a crisis, but also make it like a (Ben Smith) gamified activity to just get engaged in your community when there's not a crisis. You know, it could

14:48

(Ben Smith) be volunteering at the shelter. It could just be going to the farmers market, get know (Ben Smith) your farm or something like gamifying and incentivizing getting involved in

14:56

(Ben Smith) your community. And then we thought, well, it actually be really good to start (Ben Smith) building the functionality of such a thing

15:04

(Ben Smith) where it needs like to be built appropriately. You know, I (Ben Smith) like I immediately thought, well, someone could try to create a gamified community

15:12

(Ben Smith) app that could be useful for volunteer streamlining and then just like create a lot of (Ben Smith) haywire and like problems, you know, and a crisis. And so when I heard about

15:20

(Ben Smith) Jesse and R4 and what they had for streamlining volunteers that (Ben Smith) wanted to help with the hurricane Helen relief and getting like

15:28

(Ben Smith) drivers to where they needed to go and resources and supplies where they needed to (Ben Smith) go, I was like, okay, like that needs matching, needs and

15:36

(Ben Smith) offers should be like an essential piece. And they already have like an active user base using (Ben Smith) that to make sure they get resources and volunteers where they need to go.

15:44

(Ben Smith) Um, and so I thought I'd just describe that because what we're (Ben Smith) after is an app that on its surface would just look like a

15:52

(Ben Smith) game. It would look like um we wanted to call it like Bottowns (Ben Smith) or something like that or maybe even like a like a more fantasy sounding

16:00

(Ben Smith) name like Removerants or something. But it would all be to do (Ben Smith) a quest or like move further in the game, you do

16:08

(Ben Smith) volunteering. You like do stuff locally and um feel like you're getting (Ben Smith) involved. So, as you as I explained that like does anything come

16:16

(Ben Smith) to mind because I I was really disappointed that as far as (Ben Smith) I could tell from the limited researching that I was doing that I couldn't find anything that was doing

16:24

(Ben Smith) something like that already. There's all either either like (Ben Smith) very specifically purposed civic projects for

16:32

(Ben Smith) disaster relief or there's like you know just games and there's like not really (Ben Smith) any like overlap. And so as I describe that, I was wondering

16:40

(Ben Smith) yeah what thoughts come to mind if any or um (Daniel Fountaine) So, I'm not aware of anything that that kind of

16:52

(Daniel Fountaine) gamifies the interaction with the community in in (Daniel Fountaine) that that aspect. Um, and when you talk - (Ben Smith) yeah

17:00

(Daniel Fountaine) about gamifying like the disaster response and (Daniel Fountaine) in uh being engaged in the community,

17:08

(Daniel Fountaine) the I'd say the the first thing that I think of is (Daniel Fountaine) like gamifying disaster response could get in the way of

17:16

(Daniel Fountaine) the actual disaster response. So, I (Daniel Fountaine) would I would

17:24

(Daniel Fountaine) be concerned that it would get in the way. So, so like like my thought process is you have to (Daniel Fountaine) be really really light with the gamification of it and you have to take a - (Ben Smith) Sure. Yeah.

17:32

(Daniel Fountaine) a very sensitive approach to to that aspect of it. Um (Daniel Fountaine) because then you move you move into an area where it

17:40

(Daniel Fountaine) could be counterproductive - (Ben Smith) Right. 100%. (Daniel Fountaine) and - (Ben Smith) Yeah. Like my my thought was that we would have something that

17:48

(Ben Smith) has good streamlining functionality so that if a crisis happens and somebody wants to donate (Ben Smith) clothes or food that it can get it it get to where it needs to

17:56

(Daniel Fountaine) that - (Ben Smith) go. or if they want to volunteer and actually help in person, there's (Ben Smith) a way to streamline that. Um, and so that's

18:04

(Ben Smith) why like I I imagine a lot of these civic streamlining (Ben Smith) efforts run into that problem. And so we we probably run it do it even more

18:12

(Ben Smith) if we're gamifying it because you'd get like teenagers that would want to do it. (Ben Smith) But I like it doesn't dispel me because I I I hope that if

18:20

(Ben Smith) there is a way to do it right, then it just gets more people (Ben Smith) into civic engagement, more people into volunteering, you get more, you know, more

18:28

(Ben Smith) bodies into it. But like you said, it has to be done right. Like we (Ben Smith) we talked about how to validate it, how to stress test it, how

18:36

(Ben Smith) to um yeah, (Ben Smith) a variety of things. And we we would be gradually scaling it. That's why I wanted to

18:44

(Ben Smith) operate with the existing user base in North Carolina. (Hopefully Abysmal (Elryan The Explorer)) Well, I mean, one thing that - (Ben Smith) And go

18:52

(Hopefully Abysmal (Elryan The Explorer)) immediately comes to mind on my end, though, is that it's um I I think it's being (Hopefully Abysmal (Elryan The Explorer)) conflated the gamification of the disaster relief on the side of the

19:00

(Hopefully Abysmal (Elryan The Explorer)) actual first responders and that of the civilians that are like in the disaster - (Ben Smith) ahead. Oh. (Hopefully Abysmal (Elryan The Explorer)) as well. Um those are going to be two separate user bases who would have ideally two

19:08

(Hopefully Abysmal (Elryan The Explorer)) separate um like potentially even levels of gamification. (Hopefully Abysmal (Elryan The Explorer)) Um like to completely avoid

19:16

(Hopefully Abysmal (Elryan The Explorer)) the um like any delotterious effects of gamification. (Hopefully Abysmal (Elryan The Explorer)) Um and then as stated in the video like yes it would be a super light

19:24

(Hopefully Abysmal (Elryan The Explorer)) level um amount of that more on like the actual tracking of what is done (Hopefully Abysmal (Elryan The Explorer)) and then like social rewards and social incentives rather than

19:32

(Hopefully Abysmal (Elryan The Explorer)) just um like actually having like games be (Hopefully Abysmal (Elryan The Explorer)) a part of it. Um when when we say gamification, it's not like turning it into a

19:40

(Hopefully Abysmal (Elryan The Explorer)) game more than it is just adding like this is called the (Hopefully Abysmal (Elryan The Explorer)) dopamine hits um to it. um like ways to kind of like track what you've

19:48

(Hopefully Abysmal (Elryan The Explorer)) done um and then have like some sort of leaderboards, stuff like (Hopefully Abysmal (Elryan The Explorer)) that. Um but more on like the actual civilian utilization of it.

19:56

(Hopefully Abysmal (Elryan The Explorer)) Um being that ticketing system, I think is like one like value (Hopefully Abysmal (Elryan The Explorer)) proposition that something like this would have for the actual disaster relief community.

20:04

(Hopefully Abysmal (Elryan The Explorer)) um because potentially if there's a platform that is like already in (Hopefully Abysmal (Elryan The Explorer)) use um for just day-to-day engagement that could

20:12

(Hopefully Abysmal (Elryan The Explorer)) immediately be transferred over to something that could provide those heat maps. Um (Hopefully Abysmal (Elryan The Explorer)) which is why I'm super intrigued by this SOS like group um to see what they've

20:20

(Hopefully Abysmal (Elryan The Explorer)) done. Um but it's just getting people onto that and keeping that in like the front (Hopefully Abysmal (Elryan The Explorer)) of mind. Um the way that we aim to do that is through some form of

20:28

(Hopefully Abysmal (Elryan The Explorer)) gamification. So it's think of it more like a means to an end (Daniel Fountaine) Yeah. - (Hopefully Abysmal (Elryan The Explorer)) than necessarily the ends themselves.

20:36

(Daniel Fountaine) I I personally it definitely sounds (Daniel Fountaine) like you'll have the the right mentality about like a a

20:44

(Daniel Fountaine) a light touch of the gamification like um you know (Daniel Fountaine) experience points or earning badges or something like that and not like taking

20:52

(Daniel Fountaine) it and turning it into like a game like a full game. (Daniel Fountaine) Um, so that I mean that's just like

21:00

(Daniel Fountaine) when I when I think about this and when I when I watched the video and heard about it like that was the (Daniel Fountaine) first thing is like you don't want to get in the way of the work. Um, but

21:08

(Daniel Fountaine) if you like I said it sounds like you already have you're already (Daniel Fountaine) aware of that and you're you're taking like the right thought

21:16

(Daniel Fountaine) process to make sure that it doesn't get in the way of the work. (Daniel Fountaine) Um, I would just

21:24

(Daniel Fountaine) like I would be concerned about it and I would like (Daniel Fountaine) constantly like like check yourself on on stuff like that. That would be the thing like if

21:32

(Daniel Fountaine) I was building this that would be the thing that I would be worried about is that I would have to to (Daniel Fountaine) make sure to be careful with it.

21:40

(Daniel Fountaine) um (Daniel Fountaine) or in in a

21:48

(Daniel Fountaine) disaster response if if you know there's a there's a hurricane and people (Daniel Fountaine) are responding to it, maybe there's a way to toggle that

21:56

(Daniel Fountaine) off uh off the display so that it still happens, it (Daniel Fountaine) still functions, it it works in the background and keeps track of your tasks and and

22:04

(Daniel Fountaine) rewards you appropriately, but it's not necessarily, you know, taking the whole (Daniel Fountaine) screen to show you that you earned a new badge or something like that, allowing the

22:12

(Daniel Fountaine) the work to continue to be done and the rewards to continue (Daniel Fountaine) to flow. I think that would

22:20

(Daniel Fountaine) be probably the approach that I would think about taking is a way to toggle (Daniel Fountaine) off like animations or display or or something

22:28

(Daniel Fountaine) so that it's a little bit more work focused, but (Daniel Fountaine) you're still getting the the dopamine hits. You're still getting the

22:36

(Daniel Fountaine) rewards. You're just not like blasted with it. And (Daniel Fountaine) then out of disaster mode, you know, you toggle that that - (Hopefully Abysmal (Elryan The Explorer)) 100%.

22:44

(Daniel Fountaine) back on and then every time you unlock a reward or earn a badge or, you know, gain XP, (Daniel Fountaine) you know, full screen that b****. Like, I want to see I

22:52

(Daniel Fountaine) earned something. Hell yeah. (Daniel Fountaine) Um, yeah, that it seems like a really really interesting

23:04

(Daniel Fountaine) idea and I'm, like I said, excited to help where I can when (Daniel Fountaine) I can. Um, and see what it can do for

23:12

(Daniel Fountaine) sure. The, you know, an issue that we're facing as Rancher (Daniel Fountaine) Navy is our ticketing system right now

23:20

(Daniel Fountaine) is almost non-existent. Uh we've (Daniel Fountaine) been doing this for for a long long time. I say a long time, you know, a couple

23:28

(Daniel Fountaine) years, three years, four years. (Daniel Fountaine) But what we have right now is essentially a web form. You fill out the form. That

23:36

(Daniel Fountaine) data drops into like a Google sheet that everybody in (Daniel Fountaine) the supervisory and leadership roles can review and that

23:44

(Daniel Fountaine) data drops into a map. So we have like a lot of the (Daniel Fountaine) basic functionality built out with the the platform that we already

23:52

(Daniel Fountaine) have. um you know through Google grants we (Daniel Fountaine) we have the the workspace at no charge so we're using stuff that we already have and we

24:00

(Daniel Fountaine) don't have to pay anything for uh you said something about moving away from air (Daniel Fountaine) table and I cannot agree with you more uh KJ Navy Relief made

24:08

(Daniel Fountaine) that choice to move to Air Table at (Daniel Fountaine) uh I think it was like 16 grand a

24:16

(Daniel Fountaine) year uh and did not listen to the IT director when the (Daniel Fountaine) IT director said this is a terrible idea Don't do this. This is like

24:24

(Daniel Fountaine) glorified access database. Like you did not do anything great (Daniel Fountaine) here. And somebody else who had zero

24:32

(Daniel Fountaine) IT experience got to pull the trigger on that. (Daniel Fountaine) And it it was bad. Um to the best of my knowledge,

24:40

(Daniel Fountaine) they're still using it. Um to what degree, I'm (Daniel Fountaine) not sure, but they were in a very heavy push to justify

24:48

(Daniel Fountaine) that very large expense. Um, so they were trying to get every (Daniel Fountaine) department to use it uh to

24:56

(Daniel Fountaine) its fullest (Daniel Fountaine) potential and as the IT director

25:04

(Daniel Fountaine) um I 100% did not want to do that. I (Daniel Fountaine) kept utilizing like I had a IT

25:12

(Daniel Fountaine) inventory system to keep track of all the IT assets and stuff like that that I used that was (Daniel Fountaine) not Air Table and then I would export that and drop it into Air Table

25:20

(Daniel Fountaine) so that the my requirements of using Air Table were met but we (Daniel Fountaine) weren't using Air Table for the IT stuff um and I had

25:28

(Daniel Fountaine) um like an IT support ticketing system that was not tied to (Daniel Fountaine) Air Table but you know again I could export and drop the stuff in there so that

25:36

(Daniel Fountaine) anybody body who wanted to see it in Air Table could see it in Air Table, but that was not where (Daniel Fountaine) everything was happening. - (Hopefully Abysmal (Elryan The Explorer)) Is that is that

25:44

(Daniel Fountaine) Um, - (Hopefully Abysmal (Elryan The Explorer)) something you developed yourself or was that a third party alternative? (Daniel Fountaine) so for the most part, if I had the opportunity to use something that was free and open

25:52

(Daniel Fountaine) source, uh, I was using something that was free and open source. Um, (Daniel Fountaine) cuz for a lot of different reasons, but

26:00

(Daniel Fountaine) also it allowed me to better flex my IT budget in (Daniel Fountaine) other areas where we needed to flex the IT budget a little bit harder than like a ticketing

26:08

(Daniel Fountaine) system, you know. Um, did I want to have a a paid (Daniel Fountaine) ticketing system? Sure. Um, there's a lot of features that come with that

26:16

(Daniel Fountaine) that you don't get in the free and open source side, but the free and (Daniel Fountaine) open source stuff is functional, gets the job done, and it doesn't

26:24

(Daniel Fountaine) have a monthly or annual bill (Daniel Fountaine) associated with it. So, it allows us to save that that IT budget to do other stuff.

26:32

(Daniel Fountaine) Um, like we (Daniel Fountaine) we rebuilt and remodeled our mobile command center.

26:40

(Daniel Fountaine) Um, our mobile command center had no computing assets (Daniel Fountaine) and a network switch that was like nine years old

26:48

(Daniel Fountaine) or something like and had no, you know, half the (Daniel Fountaine) network drops were dead and stuff like that. So,

26:56

(Daniel Fountaine) we we came to me and said, "Hey, we want to remodel our mobile (Daniel Fountaine) command center and we want to be very tech heavy, so can you come in on this

27:04

(Daniel Fountaine) project?" And very quickly um I was like, "Hell yeah, let's let's do (Daniel Fountaine) some great stuff with our mobile command center." And when we were done, the

27:12

(Daniel Fountaine) mobile command center had uh six different (Daniel Fountaine) workstations um so that people could come in and sit down and actually do

27:20

(Daniel Fountaine) the things that they need to do. There's a computer there that's on our network and and does its (Daniel Fountaine) thing. Uh we had a very robust network with a couple

27:28

(Daniel Fountaine) of different Wi-Fi networks attached to it. you know, VLAN (Daniel Fountaine) off so there's no crossover between sensitive stuff and nonsensitive stuff

27:36

(Daniel Fountaine) and we had um you know mobile hotspot (Daniel Fountaine) connectivity options uh but usually in the type of things that we

27:44

(Daniel Fountaine) deploy to um you know mobile cellular networks are (Daniel Fountaine) completely down so we had a Starlink on the roof as well uh which was

27:52

(Daniel Fountaine) amazing loved using that thing that was super cool uh (Daniel Fountaine) we were getting way faster connections in a

28:00

(Daniel Fountaine) relatively well populated area on the Starlink than we (Daniel Fountaine) were with the cellular networks that were, you know, they're pulling 5G but

28:08

(Daniel Fountaine) getting it's oversaturated. So, it's it's getting trash (Daniel Fountaine) bandwidth. And then we were getting way better on the Starlink. It was it was

28:16

(Daniel Fountaine) awesome. We were a little worried about it (Daniel Fountaine) because Louisiana's got a lot of trees. Um, but we found that it

28:24

(Daniel Fountaine) it does everything that we needed to do. It's not, you know, we're not getting, you know, (Daniel Fountaine) a gig connection from Starlink, but, you know, we're getting enough that, you know,

28:32

(Daniel Fountaine) all six workstations get to do what they need to do, plus everybody's laptop (Daniel Fountaine) and a uh near constant Zoom meeting

28:40

(Daniel Fountaine) connection, so there's like an open window to the the dispatchers on the back end that we can just talk (Daniel Fountaine) to. Um, we had a I think it was a 65 in

28:48

(Daniel Fountaine) touchscreen display on one of the workstations so that you could (Daniel Fountaine) do like really broad area mapping and

28:56

(Daniel Fountaine) uh mark what you needed to mark. Yeah. What do you (Ben Smith) Sorry. Um

29:04

(Ben Smith) I I don't want to start a different thread, but I'm (Daniel Fountaine) got? - (Ben Smith) curious um because we're somewhat new to this and

29:12

(Ben Smith) we're just bootstrapping it financially for right now. Um these (Ben Smith) these projects that you're talking about um like Rancher Navy,

29:20

(Ben Smith) where do you where do you guys get funding from? Do you guys have like a grant writer that is able to (Ben Smith) pick up stuff or

29:28

(Daniel Fountaine) So for Rancher Navy, we're we're a little tight on our our (Daniel Fountaine) budget, too. We we do get uh a good amount of donations.

29:36

(Daniel Fountaine) We have um a donation platform that's on our (Daniel Fountaine) website. we're we're part of the PayPal giving

29:44

(Daniel Fountaine) fund and stuff like that. So, we we have a lot of different ways that people can (Daniel Fountaine) donate. Um and then the real driver is social media

29:52

(Daniel Fountaine) interaction. Um when when I left (Daniel Fountaine) Kinjun Navy Relief, I brought the social media manager with me.

30:00

(Daniel Fountaine) Actually, they they removed her from the organization (Daniel Fountaine) probably a week before I left. Um, so I brought the social media

30:08

(Daniel Fountaine) manager with me and she brought most of her team with her. (Daniel Fountaine) Um, because the the way that they did that, again, they're making poor

30:16

(Daniel Fountaine) choices. Um, the way the way that they got rid of her was not the right way to to handle that situation (Daniel Fountaine) in my opinion as somebody who's been, you know, a

30:24

(Daniel Fountaine) director of departments for multiple organizations. That was just not the right (Daniel Fountaine) way to do things.

30:32

(Daniel Fountaine) Um, anyway, so I brought the the social media team with me when I came over to (Daniel Fountaine) Rancher Navy, and that that's pretty much how we drive a lot of our

30:40

(Daniel Fountaine) donations is social media interaction and posts. (Daniel Fountaine) Um, we do occasionally do uh like fundraisers

30:48

(Daniel Fountaine) for a particular project. So, if there's a project that we we want to get kicked (Daniel Fountaine) off, um, and and a lot of that ties back to that social media

30:56

(Daniel Fountaine) interaction and posting and talking about it on social media drives the traffic to (Daniel Fountaine) the the website and the donation platform and stuff like that.

31:04

(Daniel Fountaine) Um, we have had some (Daniel Fountaine) large donations come from

31:12

(Daniel Fountaine) some other donors, um, like a there's a (Daniel Fountaine) a hunting association that liked what we were doing and

31:20

(Daniel Fountaine) they went out and bought our Amazon list all at once um, (Daniel Fountaine) and got it shipped to us. So, they took care of a lot of

31:28

(Daniel Fountaine) I think the first time they did that, we were we were in the panhandle wildfires and they just (Daniel Fountaine) like bought out our whole Amazon list uh and shipped

31:36

(Daniel Fountaine) it all either directly to the the AO or shipped (Daniel Fountaine) it to one of our uh drop sites where we were coordinating

31:44

(Daniel Fountaine) supplies to be trucked in because it was larger stuff. (Daniel Fountaine) Um, and then I think we've done a fundraiser with them

31:52

(Daniel Fountaine) again afterwards and and (Daniel Fountaine) there may have been a couple of other um

32:00

(Daniel Fountaine) organizations or or well-known individuals that have donated. I know (Daniel Fountaine) at CNR um and this is all public record. You could

32:08

(Daniel Fountaine) look it up, but uh Elon Musk actually made a really large donation (Daniel Fountaine) to to Cinjun Navy Relief. Um, some of it

32:16

(Daniel Fountaine) was was a was a was a (Daniel Fountaine) monetary donation and some of it was power walls to be deployed

32:24

(Daniel Fountaine) to uh the Lake Charles area after Hurricane (Daniel Fountaine) Laura. And I think we coordinated with local

32:32

(Daniel Fountaine) contractors to get those set up so everything was done correctly. And then we also (Daniel Fountaine) had a couple of them installed at the like community

32:40

(Daniel Fountaine) civic center or something. Uh so that the that's where the (Daniel Fountaine) main shelter was. So people that were displaced were were there.

32:48

(Daniel Fountaine) Uh but they were also without power. So we got them a couple of (Daniel Fountaine) the power walls. And there was

32:56

(Daniel Fountaine) another I'm not 100% on this one, so don't quote me on it, but I think (Daniel Fountaine) there was another group that brought in solar panels to pair with the power

33:04

(Daniel Fountaine) walls so that the power walls were were building power (Daniel Fountaine) storage uh even when the power was out. Um the

33:12

(Daniel Fountaine) National Guard set up a generator there so it was like not a super heavy (Daniel Fountaine) need uh that they were getting power from that the National Guard generator.

33:20

(Daniel Fountaine) Um, but in the future they're better (Daniel Fountaine) positioned to be able to support the community with the with the power walls that

33:28

(Daniel Fountaine) were distributed. (Ben Smith) Um kind of

33:36

(Ben Smith) a bold uh ballsy question. Um we've (Ben Smith) gotten only as far as we've gotten now because we've kind of

33:44

(Ben Smith) um found collaboration with existing projects. Um, (Ben Smith) and we want to try to better operationalize

33:52

(Ben Smith) that because I don't, you might get a similar sense that some of (Ben Smith) the great civic stuff that's going on can sometimes be isolated

34:00

(Ben Smith) or, you know, disperate or disconnected and people kind of doing their own thing. (Ben Smith) And there's there's a, you know, makes sense that, but

34:08

(Ben Smith) like I'll just uh I don't know. I'll aim high and then you let me know what you think (Ben Smith) is practically achievable. But if we're really open- source

34:16

(Ben Smith) and collaborative and at the end of the day, we just want to try to get some app (Ben Smith) that can be broadly known about that makes volunteering and

34:24

(Ben Smith) engaging in a positive way really fun and engaging. (Ben Smith) Um, do you see any possible like um merging

34:32

(Ben Smith) where if people that you're working with are like, "Yeah, we would love (Ben Smith) to have something like that exist as well, maybe as like a two-pointed version of what you guys are working

34:40

(Ben Smith) on." And if you guys became familiar with like what R4 is doing like there was a (Ben Smith) combining efforts. Um is that an achievable thing? What

34:48

(Hopefully Abysmal (Elryan The Explorer)) Well, so it was of my - (Ben Smith) do you think? Or go ahead uh (Hopefully Abysmal (Elryan The Explorer)) understanding that the um SOS platform that they were working on is not something that they were

34:56

(Hopefully Abysmal (Elryan The Explorer)) developing. Um so but I mean I I I would still like to (Hopefully Abysmal (Elryan The Explorer)) reiterate Ben's proposal for any form of code development if there's anything that comes to mind.

35:04

(Hopefully Abysmal (Elryan The Explorer)) Um immediately um like I've been holding out on this (Hopefully Abysmal (Elryan The Explorer)) question um one of the main things that I wanted to cover in this conversation and that can be also - (Ben Smith) Arian

35:12

(Hopefully Abysmal (Elryan The Explorer)) after this conversation topic but um that of like the TAK (Hopefully Abysmal (Elryan The Explorer)) um the TAC stuff. Um, so I just wanted to bring up that

35:20

(Hopefully Abysmal (Elryan The Explorer)) pillar and then but yeah, back back to Ben's question if there's any insights on that and then (Daniel Fountaine) Um, - (Hopefully Abysmal (Elryan The Explorer)) moving forward.

35:28

(Daniel Fountaine) So the the SOS platform I think (Daniel Fountaine) uh Victoria is in 8

35:36

(Daniel Fountaine) arena uh and she's like my main point of contact (Daniel Fountaine) when it comes to the the SOS stuff. I think her profile says she's with

35:44

(Daniel Fountaine) uh Converse Core, but (Daniel Fountaine) um she is working with with the SOS group.

35:52

(Daniel Fountaine) Um SOS help the helper I think was what (Daniel Fountaine) they called that platform. Help the helper. Uh and the

36:00

(Daniel Fountaine) website is like sosconnect.org. Um, (Daniel Fountaine) but she she would be something that I would point y'all towards

36:08

(Daniel Fountaine) because it sounds like there's a good opportunity for some some (Daniel Fountaine) integration there, uh, co-development wise.

36:16

(Daniel Fountaine) Um, and then, you know, I've had several (Daniel Fountaine) conversations with the the CEO over there at SOS, uh, Jonathan,

36:24

(Daniel Fountaine) about working together to help build the platform a little bit more. Uh (Daniel Fountaine) I myself I mean I wouldn't consider myself a developer but I

36:32

(Daniel Fountaine) have worked on a lot of different projects um that (Daniel Fountaine) would maybe position me to to help a little bit in in terms of actually

36:40

(Daniel Fountaine) developing something. Um you know I (Daniel Fountaine) don't I don't I'm all self-taught also like I don't have

36:48

(Daniel Fountaine) a degree in any of this. Uh I'm all selftaught. So, like - (Hopefully Abysmal (Elryan The Explorer)) So am I. (Daniel Fountaine) I I've taught myself uh Python like two years ago and so

36:56

(Daniel Fountaine) like I'm still learning. That's why I'm a little hesitant to throw my name (Daniel Fountaine) into the hat to help, but if I can help, I'm I'm more than willing to

37:04

(Daniel Fountaine) help. Um I have one of one of (Daniel Fountaine) the I worked with this kid uh Micah when I was with CNR.

37:16

(Daniel Fountaine) I think he signed up when he was like 15. (Daniel Fountaine) Um, and of course at at 15 they

37:24

(Daniel Fountaine) can't deploy him to the field. So he was doing a lot of backend IT stuff and (Daniel Fountaine) he's positioned himself to go into uh engineering.

37:32

(Daniel Fountaine) He's in college now. So uh I've worked with him a lot (Daniel Fountaine) at at CNR at Kun Navy Relief for a long time. Um he

37:40

(Daniel Fountaine) has since also parted ways with with Cinjun Navy Relief and (Daniel Fountaine) um you know uh year before last he

37:48

(Daniel Fountaine) interned at Harris County Sheriff's Office. Uh so that's the the (Daniel Fountaine) Houston area Sheriff's Office and then last year he interned at

37:56

(Daniel Fountaine) NASA. Uh I'm not sure if he's continuing his internship at NASA this (Daniel Fountaine) year but uh he's a really smart kid. He knows he

38:04

(Daniel Fountaine) knows a lot and he's also excited to learn. So, if there's an (Daniel Fountaine) area that he needs to to touch up on to be good at something, like he just f******

38:12

(Daniel Fountaine) he dives into it and goes. Um, so (Daniel Fountaine) I've tried to to coordinate him hooking up with the

38:20

(Daniel Fountaine) SOS folks to see if it's something that he's interested in. He and I have (Daniel Fountaine) also in the past worked on something like a dispatch ticketing

38:28

(Daniel Fountaine) system um collaboratively and you know, you (Daniel Fountaine) know, life happens and I had to step away for a little while. So, I haven't seen what what he's done with the project

38:36

(Daniel Fountaine) since then, but we had I'm not going to say most (Daniel Fountaine) of a platform, but we had more than a lot of people have for a

38:44

(Daniel Fountaine) platform for that. Uh, so I would I would also be interested (Daniel Fountaine) in maybe sending Micah your way to see if it's something that, you know,

38:52

(Daniel Fountaine) both y'all and and Micah think that this is something that y'all could work on together. (Daniel Fountaine) Um, like I said, super smart kid. Um,

39:00

(Daniel Fountaine) and has already a passion for developing something for (Daniel Fountaine) the nonprofits. Uh, I think one of

39:08

(Daniel Fountaine) the the bigger drives for him as well is that he wants to make (Daniel Fountaine) this, you know, ticketing and dispatch solution something that

39:16

(Daniel Fountaine) is is free and doesn't cost these nonprofit organizations (Daniel Fountaine) anything to use that allows them to be better at what they're trying to do.

39:24

(Daniel Fountaine) help people who are trying to to help others. (Daniel Fountaine) Uh I think that the so I just stole the SOS tagline,

39:32

(Daniel Fountaine) but um that was kind of his thing is he didn't want it to be like a (Daniel Fountaine) for-profit project. And so he's trying to do this

39:40

(Daniel Fountaine) um while maintaining (Daniel Fountaine) that like freeto use kind of mentality. And

39:48

(Daniel Fountaine) um I think (Daniel Fountaine) there's building something like

39:56

(Daniel Fountaine) this also has like cost associated with it, right? Like you have overhead to (Daniel Fountaine) to pay for the servers and keep things running and stuff like that. Uh unless you're

40:04

(Daniel Fountaine) self-hosting. Um but then your you know your power bill and internet bill (Daniel Fountaine) go up. But um I

40:12

(Daniel Fountaine) I think he's comfortable with, you know, a project that would maybe cover (Daniel Fountaine) the cost to operate

40:20

(Daniel Fountaine) and yeah, it may have taken him a little bit of (Daniel Fountaine) talking him through that that like you you want to cover your cost at the very least. You don't want to

40:28

(Daniel Fountaine) be going into debt to to maintain this. And then that puts (Daniel Fountaine) the project at a in a you know a risky

40:36

(Daniel Fountaine) position to to fail when you know (Daniel Fountaine) anything else costs anything else like like put yourself on the ledge

40:44

(Daniel Fountaine) there. Um but like I said (Daniel Fountaine) and that's kind of what SOS is trying to do too. They're trying to make something that's free

40:52

(Daniel Fountaine) for the nonprofits to use. Um, (Daniel Fountaine) they're I don't want to speak to their goals too much, but from what I

41:00

(Daniel Fountaine) understand, they're also looking at building it so that, you (Daniel Fountaine) know, volunteer fire departments can use it, and most of those are already

41:08

(Daniel Fountaine) set up as a nonprofit. So, I think that's a a really (Daniel Fountaine) interesting uh way to to coordinate these

41:16

(Daniel Fountaine) these NOS's with your your first responding (Daniel Fountaine) agencies, your fire departments. Um, you know, even like county

41:24

(Daniel Fountaine) ESDs would benefit from something like that. in uh (Daniel Fountaine) even like sheriff's office or

41:32

(Daniel Fountaine) or um constable's office like a a way to to (Daniel Fountaine) coordinate and see where everybody's working so that everybody can kind of be on the same

41:40

(Daniel Fountaine) page and I think that is a good spot (Daniel Fountaine) to loop back to the tax stuff um because

41:48

(Daniel Fountaine) a lot of state agencies already use the (Daniel Fountaine) tax stuff for what they do. They use a different version than what

41:56

(Daniel Fountaine) what you could go out and download today. Like if you were to go to the website and (Daniel Fountaine) download TAC, well, I think you have to have a a.gov

42:04

(Daniel Fountaine) login to download it. (Daniel Fountaine) But um yeah, you know what? It might

42:12

(Daniel Fountaine) be I'm having to - (Hopefully Abysmal (Elryan The Explorer)) So I did do some I did some digging. Um the (Hopefully Abysmal (Elryan The Explorer)) seems like the only currently available one for public is

42:20

(Hopefully Abysmal (Elryan The Explorer)) ATAC um and that's just like the Android like mobile phone. So like um (Hopefully Abysmal (Elryan The Explorer)) they also have the server utility up um that you can

42:28

(Hopefully Abysmal (Elryan The Explorer)) potentially deploy yourself. Um but like I like past that I think it is yeah (Hopefully Abysmal (Elryan The Explorer)) like login based um I did make a login um just on the public login

42:36

(Daniel Fountaine) I was I was going to say I I think the the ITAR stuff - (Hopefully Abysmal (Elryan The Explorer)) but wasn't able to get too (Daniel Fountaine) for like the civ version is now in a position where you can

42:44

(Daniel Fountaine) create an account and download it. (Daniel Fountaine) Um it's good to meet - (Hopefully Abysmal (Elryan The Explorer)) much

42:56

(Daniel Fountaine) you. Um, but it is like e export (Daniel Fountaine) controlled software, so you have to be really careful about where you set it up and stuff like that.

43:04

(Daniel Fountaine) Um, I've I've worked with with ATC for a long (Daniel Fountaine) time. Uh, and I think ATC is still the

43:12

(Daniel Fountaine) the classification or the like brand (Daniel Fountaine) name for the military version. They also have like ATC.mill,

43:20

(Daniel Fountaine) which would be the military version. Um - (Hopefully Abysmal (Elryan The Explorer)) Okay. It was just a text div is the one I was referring (Daniel Fountaine) I've Yeah, the So there's um - (Hopefully Abysmal (Elryan The Explorer)) to. But

43:28

(Daniel Fountaine) mail is the military version. Uh gov is like anybody (Daniel Fountaine) else who's not military. And then there's uh CIV, which is

43:36

(Daniel Fountaine) the civilian version. Um (Daniel Fountaine) and technically there's like ITAC, which would work

43:44

(Daniel Fountaine) on an iPhone. Uh and there's wind tac, which works on a desktop, - (Hopefully Abysmal (Elryan The Explorer)) yeah, yeah, it's all right. (Daniel Fountaine) which I actually have and I can show you. - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah.

43:52

(Daniel Fountaine) Um, (Daniel Fountaine) but what is this? Okay, I'll look at that

44:00

(Daniel Fountaine) later. Um, I' I've worked with the the mill, the government, and the (Daniel Fountaine) civ side. So, like I know, you know, like functionality,

44:08

(Daniel Fountaine) what the differences are, and they're not a whole lot. So, like you're you're really (Daniel Fountaine) getting a lot with the civ version. um - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

44:16

(Daniel Fountaine) which I think is even even advertised on the TAC website as like being (Daniel Fountaine) for NOS's and uh first responders and and disaster response

44:24

(Daniel Fountaine) and stuff like that. Um, it it's a pretty solid platform, but (Daniel Fountaine) it's like one of those platforms when it when it first came out and it was just a tech and

44:32

(Daniel Fountaine) it was just for the military. It was it was a really cool platform that (Daniel Fountaine) didn't require a whole lot of like preconfiguring to get it to do what you needed to

44:40

(Daniel Fountaine) do and it just kind of worked to do its job and it was really (Daniel Fountaine) good. Uh, and then as they branched into the gov side because you know the

44:48

(Daniel Fountaine) the alphabet boys want want their cut of whatever the mill guys (Daniel Fountaine) get. um they kind of had to to strip a couple of things

44:56

(Daniel Fountaine) out and uh water water it down a little bit so that you couldn't (Daniel Fountaine) like set targeting packages and and stuff like that. Um, and

45:04

(Daniel Fountaine) then the like state and local guys wanted a version (Daniel Fountaine) and then the fire departments and

45:12

(Daniel Fountaine) local first responders heard about it, saw it, liked it. And so then that's kind of (Daniel Fountaine) where the civ version came from is because you had to make something that

45:20

(Daniel Fountaine) was accessible to volunteer fire departments. And I think that was, if I remember (Daniel Fountaine) correctly, that was like one of the big pushing factors to make this version. There was no

45:28

(Daniel Fountaine) intent to make it a civilian access application. But when you talk about first (Daniel Fountaine) responders and being able to coordinate for large uh incident

45:36

(Daniel Fountaine) response scenarios, uh being able to include your volunteer (Daniel Fountaine) fire department partners is kind of like a critical key. Uh so

45:44

(Daniel Fountaine) they they did push it to the civilian version and that's what you have (Daniel Fountaine) now. Somewhere along the lines between the gov and the civ

45:52

(Daniel Fountaine) version, they started implementing plugins and plugins add (Daniel Fountaine) or uh modify functionality. And with

46:00

(Daniel Fountaine) those plugins and the the (Daniel Fountaine) type of I guess some of the features

46:08

(Daniel Fountaine) that had to be removed in order to make it accessible for the civilian (Daniel Fountaine) version, it got a lot more complicated when it comes

46:16

(Daniel Fountaine) to building out a tech to function for like an an NGO or (Daniel Fountaine) a fire department or whatever. And it I think they didn't get as much

46:24

(Daniel Fountaine) of a of a spin up on the civac that they (Daniel Fountaine) expected, but it has found its uses and it is being leveraged in a lot

46:32

(Daniel Fountaine) of different ways. Um, I can (Daniel Fountaine) show you wind if you wanted to see - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah. Yeah. No, I'd definitely

46:40

(Daniel Fountaine) it. I don't know if - (Hopefully Abysmal (Elryan The Explorer)) be really (Daniel Fountaine) my if - (Hopefully Abysmal (Elryan The Explorer)) intrigued.

46:52

(Daniel Fountaine) my server is up and running. (Daniel Fountaine) I have to look at my VMware because I

47:00

(Daniel Fountaine) think it does not auto boot. (Daniel Fountaine) It is not running. Um so I could show you wine.

47:08

(Daniel Fountaine) Uh, I might even (Daniel Fountaine) my memory resources right now. What

47:16

(Daniel Fountaine) is this guy going to (Daniel Fountaine) take?

47:24

(Daniel Fountaine) Uh, (Daniel Fountaine) oh yeah, I could fire it up without it being a problem.

47:32

(Daniel Fountaine) All right. So, I'll I'll boot up (Daniel Fountaine) my A tech server and see what it looks like.

47:40

(Daniel Fountaine) Uh, it's been off for a little bit, so it might not want to function without (Daniel Fountaine) some - (Hopefully Abysmal (Elryan The Explorer)) Oh no. I

47:48

(Daniel Fountaine) updates. - (Hopefully Abysmal (Elryan The Explorer)) mean, even if it this has to be like an ongoing conversation, I'm not opposed. Um (Hopefully Abysmal (Elryan The Explorer)) like especially if you've got anywhere to like anything to do in the

47:56

(Daniel Fountaine) Yeah, - (Hopefully Abysmal (Elryan The Explorer)) next x amount of time. Don't want to hold you too much. (Daniel Fountaine) I'm I'm pretty

48:04

(Hopefully Abysmal (Elryan The Explorer)) Yeah, I am relatively new to the the tax (Hopefully Abysmal (Elryan The Explorer)) stuff. Um like the the main value proposition that I

48:12

(Hopefully Abysmal (Elryan The Explorer)) um Oh, that was quick. Is it (Daniel Fountaine) flexible.

48:20

(Daniel Fountaine) I told it to open. Oh, there it goes. Um, so this this is the S (Daniel Fountaine) version as you can - (Hopefully Abysmal (Elryan The Explorer)) up? Okay.

48:32

(Daniel Fountaine) tell. (Daniel Fountaine) Uh, Windac is not very fast and it is uh

48:40

(Daniel Fountaine) a little resourceheavy. Um, - (Hopefully Abysmal (Elryan The Explorer)) just a (Daniel Fountaine) but yeah. Um, and I I think - (Hopefully Abysmal (Elryan The Explorer)) little

48:48

(Daniel Fountaine) there's I'm trying to remember accurately. There's some stuff that you can't do in (Daniel Fountaine) WindC. Um, but I - (Hopefully Abysmal (Elryan The Explorer)) bit.

48:56

(Daniel Fountaine) mean this this is uh like Google Earth essentially. Like you've seen - (Hopefully Abysmal (Elryan The Explorer)) Cool. (Daniel Fountaine) what Google Earth looks like. Yeah. See, I can try it, but I - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

49:04

(Daniel Fountaine) don't think it's going to work. (Daniel Fountaine) I think my ATAC server needs

49:12

(Daniel Fountaine) uh I think I missed an update somewhere and it's not going to want to (Daniel Fountaine) connect. Yeah. So, we're not connected right now.

49:20

(Daniel Fountaine) Um and you can customize it and install, you know, plugins. This (Daniel Fountaine) one, this particular version, you see what I mean? It is - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

49:28

(Daniel Fountaine) slow. (Daniel Fountaine) Um, but

49:40

(Daniel Fountaine) um, you know, it it works really well at what it's supposed to do. Show you where your (Daniel Fountaine) teams are and who's moving where. Um, it will also do navigation with

49:48

(Daniel Fountaine) a with a simple plugin. I (Daniel Fountaine) don't think I have many plugins set

49:56

(Daniel Fountaine) up, if (Daniel Fountaine) any, and I honestly Okay, so I

50:12

(Daniel Fountaine) do have uh routes installed, which is like the navigation extension (Daniel Fountaine) or the navigation plugin. Um, and

50:20

(Daniel Fountaine) I have something else (Daniel Fountaine) here. CVAC and TAC

50:28

(Daniel Fountaine) chat. Uh, so there's a couple of plugins here, but not a whole (Daniel Fountaine) lot. Um, but they'll let you put markers on the map and look at stuff.

50:36

(Daniel Fountaine) And, uh, with file overlays, you can put (Daniel Fountaine) like a map of a building over the building, so you can see the

50:44

(Daniel Fountaine) internal map of the building. Um, which makes it a lot - (Hopefully Abysmal (Elryan The Explorer)) Oh, (Daniel Fountaine) easier when you're having, you know, search and rescue teams out there searching for stuff.

50:52

(Daniel Fountaine) You can see where everybody's at in the building. You can kind of give them a direction like you need to go (Daniel Fountaine) towards that window to your left or whatever. - (Hopefully Abysmal (Elryan The Explorer)) yeah.

51:00

(Daniel Fountaine) Um, it does do video, (Daniel Fountaine) but it doesn't do it very well, and it depends on the network setup

51:08

(Daniel Fountaine) that you're using to to back up your your (Daniel Fountaine) ATAC connection. uh in terms

51:16

(Daniel Fountaine) of using it in a disaster (Daniel Fountaine) area. Um like

51:28

(Daniel Fountaine) uh what is the name of those little (Hopefully Abysmal (Elryan The Explorer)) just like basic push and

51:36

(Daniel Fountaine) radios? No, they they have a - (Hopefully Abysmal (Elryan The Explorer)) talk. Um I forget what it's (Hopefully Abysmal (Elryan The Explorer)) called. Is

51:44

(Daniel Fountaine) these little Laura radios that (Daniel Fountaine) will do

51:52

(Daniel Fountaine) data. They let you text and (Daniel Fountaine) drop GPS locations pretty easily.

52:00

(Daniel Fountaine) Um, they don't do a whole lot of (Daniel Fountaine) data. So, it's like really perfect for the the ATC application

52:08

(Daniel Fountaine) because a lot of that stuff is set up when you set up the device. So when you - (Hopefully Abysmal (Elryan The Explorer)) that (Daniel Fountaine) put ATAC on your mobile device, that's

52:16

(Daniel Fountaine) when you configure everything. That's when you load your plugins and load (Daniel Fountaine) your uh maps and stuff like that is right there at the beginning. You try and do

52:24

(Daniel Fountaine) that where you have a network connection. um so that (Daniel Fountaine) you get all that stuff downloaded and preconfigured. And it'll also configure

52:32

(Daniel Fountaine) like um (Daniel Fountaine) your you know encryption keys and radio frequencies and stuff like that if

52:40

(Daniel Fountaine) you're using like one of those little Laura radios. - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) Um so that everybody's on the same page and all

52:48

(Daniel Fountaine) your data is on the same network. So when somebody updates their (Daniel Fountaine) location trying to God dang it's going to stump me now.

52:56

(Daniel Fountaine) I'm going to have to look it (Daniel Fountaine) up.

53:12

(Hopefully Abysmal (Elryan The Explorer)) I don't know. Um the the main draw for (Hopefully Abysmal (Elryan The Explorer)) TAC um not just like on potentially overlaying on

53:20

(Hopefully Abysmal (Elryan The Explorer)) it um but like utilizing the like network (Daniel Fountaine) Meshtastic. What? Yeah. Why I couldn't come up with that? I don't - (Hopefully Abysmal (Elryan The Explorer)) configuration mesh

53:28

(Daniel Fountaine) know. Uh too tired today. Uh so - (Hopefully Abysmal (Elryan The Explorer)) task. Ah, no (Daniel Fountaine) Meshtastic does the the like the mesh network using the the

53:36

(Daniel Fountaine) Laura frequencies. So as long as you have good line of sight, they usually work pretty well. - (Hopefully Abysmal (Elryan The Explorer)) worries. (Daniel Fountaine) Um similar to Gotenna.

53:44

(Daniel Fountaine) Are you familiar with Gotenna? Okay. Gotenna is essentially (Daniel Fountaine) like the the military government version of

53:52

(Daniel Fountaine) Meshtastic. It's like the same or very similar (Daniel Fountaine) frequencies. Um kind of the same concept like they work really well with a

54:00

(Daniel Fountaine) line of sight connection. Um they have (Daniel Fountaine) a a base station that you can get and set

54:08

(Daniel Fountaine) up that gets you like (Daniel Fountaine) greater height so you get better line of sight for for everybody.

54:16

(Daniel Fountaine) Um, and they have a configuration that would be like a payload for a (Daniel Fountaine) drone to get your meshtastic network a wider

54:24

(Daniel Fountaine) umbrella of coverage. (Daniel Fountaine) Um, Gotenna is really expensive. Uh,

54:32

(Daniel Fountaine) but it's really good for what it does. It's it's (Daniel Fountaine) like rechargeable little radios that come in a Pelican case. They have the

54:40

(Daniel Fountaine) ATC controller inside the Pelican case. So when you set this up in the field, it's like - (Hopefully Abysmal (Elryan The Explorer)) Okay. (Daniel Fountaine) everybody's on the same page right away from the beginning and you have like your

54:48

(Daniel Fountaine) your mission control center. You like your your command center in (Daniel Fountaine) the field with that uh ATAC. It's, you know, comes like on

54:56

(Daniel Fountaine) a Samsung tablet or something. So you get a a pretty decent sized screen. You (Daniel Fountaine) can see everybody if you're, you know, that, - (Hopefully Abysmal (Elryan The Explorer)) Cool.

55:04

(Daniel Fountaine) you know, commanding that team, you can see everybody. You can see when somebody drops off. (Daniel Fountaine) Uh and like I said, they they mesh. So, you

55:12

(Daniel Fountaine) know, somebody doesn't necessarily have to have line of sight (Daniel Fountaine) to where your command is, uh, as long as

55:20

(Daniel Fountaine) there's you can hop to it. - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yep. Line side to the (Daniel Fountaine) Um, and they have a way to

55:28

(Daniel Fountaine) tie it in with like an edge node, an attack (Daniel Fountaine) edge node. So you can have your edge node - (Hopefully Abysmal (Elryan The Explorer)) line.

55:36

(Daniel Fountaine) like in a a vehicle that's responding. Maybe your your Starlink (Daniel Fountaine) equipped vehicle and then your dispatchers on the back end can see everybody

55:44

(Daniel Fountaine) in near real time um all the way out in the field. (Daniel Fountaine) So a tech is a really good solution. Uh it's very complicated because it's

55:52

(Daniel Fountaine) so customizable to do so many different things. Um (Daniel Fountaine) you know which happened along the way of development. It went from being like a really

56:00

(Daniel Fountaine) strictly mission focused thing to being something that's a little bit more widespread and a little bit more (Daniel Fountaine) widespread. So, it has all these customizations that you can build out.

56:08

(Daniel Fountaine) Um, but when configured and built out correctly, it is (Daniel Fountaine) a super useful tool to use in the field.

56:16

(Daniel Fountaine) Um, as you know, speaking from somebody who's been the incident commander for some (Daniel Fountaine) pretty, you know, hairy deployments where we had people out in the field running

56:24

(Daniel Fountaine) chainsaws and, uh, a house that was ready to collapse and (Daniel Fountaine) a house that had already collapsed and

56:32

(Daniel Fountaine) monitoring and and commanding these teams and and doing all of that stuff. (Daniel Fountaine) Um, would have been way easier had

56:40

(Daniel Fountaine) I set up a tech to take care of what we needed. (Daniel Fountaine) Um, but I've

56:48

(Daniel Fountaine) I don't know. I like it. I hate having to sit here and configure it and build it (Daniel Fountaine) out and then uh you have to remember to - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

56:56

(Daniel Fountaine) export that configuration and take it with you or (Daniel Fountaine) um there's a lot of easy ways to trip

57:04

(Daniel Fountaine) up and make it more of a problem than a tool. (Daniel Fountaine) Um and that's just I guess native to the how customizable it

57:12

(Daniel Fountaine) is. - (Hopefully Abysmal (Elryan The Explorer)) Fair enough. Um, no. Yeah. Um, (Hopefully Abysmal (Elryan The Explorer)) I am super intrigued by it. Like kind of almost more of a like a case study. Um,

57:20

(Hopefully Abysmal (Elryan The Explorer)) but I was also intrigued by like the way that y'all do, not y'all, but (Hopefully Abysmal (Elryan The Explorer)) the way that TAC does like the networks and stuff. Um, and the affformentioned that

57:28

(Hopefully Abysmal (Elryan The Explorer)) like there's already TAC servers up like pretty much (Hopefully Abysmal (Elryan The Explorer)) across the nation, right? Um, so one thing that I was quite curious

57:36

(Hopefully Abysmal (Elryan The Explorer)) is like um do you think it would be within the realm of possibility to (Hopefully Abysmal (Elryan The Explorer)) like figure out some way to have some form of like handshake

57:44

(Hopefully Abysmal (Elryan The Explorer)) um such that like in a disaster scenario um we have like our (Hopefully Abysmal (Elryan The Explorer)) game servers and stuff but like if there needs to be any offline functionality and

57:52

(Hopefully Abysmal (Elryan The Explorer)) like pure syncing um like the edge nodes in particular being (Hopefully Abysmal (Elryan The Explorer)) like the local intranets of like

58:00

(Hopefully Abysmal (Elryan The Explorer)) whatever like wherever people are that like would (Hopefully Abysmal (Elryan The Explorer)) potentially have their internet access go down. Um

58:08

(Hopefully Abysmal (Elryan The Explorer)) like figure out some way that um we could use the same kind of back (Hopefully Abysmal (Elryan The Explorer)) end as like a fallback was something I was toying

58:24

(Daniel Fountaine) Um, in terms - (Hopefully Abysmal (Elryan The Explorer)) with (Daniel Fountaine) of So

58:36

(Daniel Fountaine) are you are you talking are you the scenario that you're describing are you talking about somebody has like (Daniel Fountaine) a a attack server setup that they use for like mil

58:44

(Daniel Fountaine) stem airsoft being converted to a disaster response type of server. (Hopefully Abysmal (Elryan The Explorer)) Why not? Um I

58:52

(Hopefully Abysmal (Elryan The Explorer)) mean like on the side of like server configuration, yes, that could be as easy (Daniel Fountaine) Huh? - (Hopefully Abysmal (Elryan The Explorer)) as just like having some way to like have some easily

59:00

(Hopefully Abysmal (Elryan The Explorer)) deployable utility that does some form of conversion. But um what I was even thinking (Hopefully Abysmal (Elryan The Explorer)) is like so whatever we build out could serve as kind of a new front

59:08

(Hopefully Abysmal (Elryan The Explorer)) end um for like specific use cases (Hopefully Abysmal (Elryan The Explorer)) um but like still work on the same back end. Like we're just building this to

59:16

(Hopefully Abysmal (Elryan The Explorer)) be as interoperable with current systems as possible is like what we're I'm trying (Hopefully Abysmal (Elryan The Explorer)) to like go about this. Um,

59:32

(Hopefully Abysmal (Elryan The Explorer)) yeah. I don't know. I I could be potentially just be mistaken in my understanding and (Hopefully Abysmal (Elryan The Explorer)) the the way that it's set up as well. Um, but I'm

59:40

(Daniel Fountaine) So - (Hopefully Abysmal (Elryan The Explorer)) just quite (Daniel Fountaine) for for a civac

59:48

(Daniel Fountaine) server to be utilized in in that kind of - (Hopefully Abysmal (Elryan The Explorer)) intrigued. (Daniel Fountaine) way, it would require

59:56

(Daniel Fountaine) you I mean you could (Daniel Fountaine) theoretically build a a plugin to do all this but you it would require

1:00:04

(Daniel Fountaine) a way for somebody who doesn't (Daniel Fountaine) have that network configuration that uh you know server

1:00:12

(Daniel Fountaine) config to be able to connect to it. Um, and if you had a (Daniel Fountaine) plugin that would connect to

1:00:20

(Daniel Fountaine) like a bridge, um, that would (Daniel Fountaine) essentially share Yeah. - (Hopefully Abysmal (Elryan The Explorer)) cyber security

1:00:28

(Daniel Fountaine) See, that that's what I'm trying to think through. It's like you you would have to - (Hopefully Abysmal (Elryan The Explorer)) issue. (Daniel Fountaine) have I'm sure it can be done, but it would not be

1:00:40

(Daniel Fountaine) a very simple solution. Um, so for example, like - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) I have my my tax server here that lives in my lab. - (Hopefully Abysmal (Elryan The Explorer)) No.

1:00:48

(Daniel Fountaine) Um, if there was a disaster nearby and need (Daniel Fountaine) it needed to be leveraged as a disaster response

1:00:56

(Daniel Fountaine) solution, there would need to be a handshake (Daniel Fountaine) between, you know, the tech units in the field and the

1:01:04

(Daniel Fountaine) server. And that's why I'm thinking like if you had a - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah. (Daniel Fountaine) bridge that would say, you know, my my personal attack server

1:01:12

(Daniel Fountaine) can be used for disaster response if (Daniel Fountaine) needed and then add that config to like a a

1:01:20

(Daniel Fountaine) backend checklist. Um, and then so a disaster (Daniel Fountaine) happens nearby, you know, a local responding

1:01:28

(Daniel Fountaine) agency goes to that plugin and says, "Hey, I need to find the local tax (Daniel Fountaine) server." And it finds my server. And they click on it. then it just takes care

1:01:36

(Daniel Fountaine) of that credentiing on the back end (Daniel Fountaine) that yeah I mean that that could be

1:01:44

(Daniel Fountaine) a plugin and that could do it. Um and then you (Daniel Fountaine) could as part of the plugin add

1:01:52

(Daniel Fountaine) an overlay that would put whatever ticketing data that you you (Daniel Fountaine) have on your side onto the ATAC map.

1:02:00

(Daniel Fountaine) Um that could work. I I (Daniel Fountaine) would be a little concerned about the level of adoption that you

1:02:08

(Daniel Fountaine) would see in in public. Um I don't think (Daniel Fountaine) that, you know, if if you have like an airsoft milim

1:02:16

(Daniel Fountaine) guy that is techsavvy enough to set up his own tax (Daniel Fountaine) server for his team, I don't think that that type of individual would be like the kind

1:02:24

(Daniel Fountaine) of personality that would clash with the idea of opening his - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Heat. (Daniel Fountaine) server up to be used for disaster response. Those are

1:02:32

(Daniel Fountaine) usually pretty chill people in my book. (Daniel Fountaine) Um

1:02:40

(Daniel Fountaine) the I think one of the limitations that you'll you'll run into is (Daniel Fountaine) when you

1:02:48

(Daniel Fountaine) have maybe uh a state agency that is kind of doing the same thing and (Daniel Fountaine) leveraging that plugin. I don't think that they would adopt something like that at

1:02:56

(Daniel Fountaine) all. Um and that's That's (Daniel Fountaine) that's based on conversations I've had with the the state of Texas. Um

1:03:04

(Daniel Fountaine) our DPS or state troopers (Daniel Fountaine) leverage a tax system. Um and we I've I've

1:03:12

(Daniel Fountaine) had some conversations. I went to like a AWS conference and sat down with like one of their (Daniel Fountaine) their super nerdy IT tech guys and we had this

1:03:20

(Daniel Fountaine) conversation about like they really want to but I think it's (Daniel Fountaine) because they're on the gov version they cannot do something like that.

1:03:28

(Daniel Fountaine) Um they so the Texas - (Hopefully Abysmal (Elryan The Explorer)) Oh, (Daniel Fountaine) DPS I don't I don't know what state you live in u but the state - (Hopefully Abysmal (Elryan The Explorer)) interesting. Yeah, that's

1:03:36

(Daniel Fountaine) troopers really wanted to like he he was like man we've been - (Hopefully Abysmal (Elryan The Explorer)) us. (Daniel Fountaine) talking about doing something like this for years where we could coordinate with you guys and and I was

1:03:44

(Daniel Fountaine) there representing Cajun Navy Relief and he was like we really want to have (Daniel Fountaine) a way to interconnect with you guys so that we're not going to

1:03:52

(Daniel Fountaine) the same tickets that you're working even if we have a 911 call for it and we see that your (Daniel Fountaine) team is in route then we not go to it and trust that you guys are going to

1:04:00

(Daniel Fountaine) handle it. So there's already a a level of trust and (Daniel Fountaine) respect between us and what we do and how we operate that they they were willing

1:04:08

(Daniel Fountaine) to set up this interconnectivity (Daniel Fountaine) um with our tax server and their tax server so that we could

1:04:16

(Daniel Fountaine) see each other and essentially not double run tickets, you know, not (Daniel Fountaine) run double double run calls for assistance and and stuff like

1:04:24

(Daniel Fountaine) that. Um, I'd have (Daniel Fountaine) to and I'd have to see if I still

1:04:32

(Daniel Fountaine) have his - (Hopefully Abysmal (Elryan The Explorer)) I mean, at that point though, it it it doesn't seem to be a technical (Hopefully Abysmal (Elryan The Explorer)) infeasibility more than it is a bureaucratic infeasibility.

1:04:40

(Hopefully Abysmal (Elryan The Explorer)) Um, so like that would potentially be a really hard (Hopefully Abysmal (Elryan The Explorer)) conversation that we'd have to have a lot of times. I guess I don't know. But it's just my

1:04:48

(Daniel Fountaine) email - (Hopefully Abysmal (Elryan The Explorer)) my thing is is like costbenefit analysis between that (Hopefully Abysmal (Elryan The Explorer)) or getting our own like server utility that basically mimics the

1:04:56

(Hopefully Abysmal (Elryan The Explorer)) functionality of like TAC like tech stack. (Hopefully Abysmal (Elryan The Explorer)) um like like the the adoption curve of

1:05:04

(Hopefully Abysmal (Elryan The Explorer)) just like figuring out some way to get the plugin versus having to have our own (Hopefully Abysmal (Elryan The Explorer)) servers be built out like across the nation, you know.

1:05:12

(Hopefully Abysmal (Elryan The Explorer)) Um, and it's just like also a cost thing (Daniel Fountaine) So, one of one of the the headaches that that I've

1:05:20

(Daniel Fountaine) ran into with trying to implement um a (Daniel Fountaine) tech for disaster response

1:05:32

(Daniel Fountaine) is that interconnection between your dispatch who may live in in like Kansas (Daniel Fountaine) or Kentucky or Tennessee when you're responding to something in in

1:05:40

(Daniel Fountaine) Texas um is that - (Hopefully Abysmal (Elryan The Explorer)) too. (Daniel Fountaine) it even if you build out everything and configure everything,

1:05:48

(Daniel Fountaine) your local TAC units like your your your (Daniel Fountaine) squad in the field can see each other and communicate with each other

1:05:56

(Daniel Fountaine) and and work together on the TAC platform just (Daniel Fountaine) because they're on Meshtastic or uh goenna or something like

1:06:04

(Daniel Fountaine) that even without cellular they can work together - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) but getting that information back to the back end so that they can

1:06:12

(Daniel Fountaine) see what everybody's doing that's been the problem. (Daniel Fountaine) Um

1:06:20

(Daniel Fountaine) now a tech has made the the (Daniel Fountaine) edge server um config or or

1:06:28

(Daniel Fountaine) build or image or whatever they they have an edge server (Daniel Fountaine) that you can run like at a at a vehicle. So like your mobile

1:06:36

(Daniel Fountaine) command center or something like that. Uh CNR's mobile command center was big enough and - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) powerful enough that it it could have its own server period. But if you put - (Hopefully Abysmal (Elryan The Explorer)) Yeah,

1:06:44

(Daniel Fountaine) like a a micro uh form (Daniel Fountaine) factor computer in a vehicle, you know, that could be your

1:06:52

(Daniel Fountaine) edge server. Um, and then, you know, - (Hopefully Abysmal (Elryan The Explorer)) nice. (Daniel Fountaine) backhaul that with Starlink, which is like a new - (Hopefully Abysmal (Elryan The Explorer)) Yep.

1:07:00

(Daniel Fountaine) acquisition for Rancher Navy. Uh, we just got ours this year, so (Daniel Fountaine) being able to to back haul that, that would potentially

1:07:08

(Daniel Fountaine) fix the problem. Uh, thanks, Jared. (Daniel Fountaine) uh that would potentially, you know, fix

1:07:16

(Daniel Fountaine) that that drop in communication and bring that data from (Daniel Fountaine) your guys in the field on your meshtastic

1:07:24

(Daniel Fountaine) goenna network uh back to the dispatcher sitting (Daniel Fountaine) in, you know, Oklahoma, Kansas, Kentucky, whatever.

1:07:32

(Daniel Fountaine) Um, and that's kind - (Hopefully Abysmal (Elryan The Explorer)) Yeah. But at (Daniel Fountaine) of that's kind of why I set out to build this uh a tech - (Hopefully Abysmal (Elryan The Explorer)) the at

1:07:40

(Daniel Fountaine) server here is to to start to build that process and work (Daniel Fountaine) through that and get a tech to a functional place. And then

1:07:48

(Daniel Fountaine) I wanted to start diving into maybe what plug-in (Daniel Fountaine) development looks like to make something for a tech that - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:07:56

(Daniel Fountaine) would be more beneficial than what already (Daniel Fountaine) exists to disaster response.

1:08:04

(Daniel Fountaine) Um, I have very (Daniel Fountaine) loosely had a conversation with some contacts about and they they

1:08:12

(Daniel Fountaine) operate at like a state and (Daniel Fountaine) and federal level about using

1:08:20

(Daniel Fountaine) other ATAC servers to to help bridge that gap. So these - (Hopefully Abysmal (Elryan The Explorer)) Nobody. (Daniel Fountaine) conversations are already taking place on how to how to

1:08:28

(Daniel Fountaine) leverage other ATA tech servers that are operated maybe (Daniel Fountaine) by trusted NOS to do

1:08:36

(Daniel Fountaine) disaster response work. Um (Daniel Fountaine) those conversations are ongoing and they're a little bit longer because you know

1:08:44

(Daniel Fountaine) they're they're going back to the state level. They're going back to the federal level on how (Daniel Fountaine) to coordinate using civac

1:08:52

(Daniel Fountaine) alongside govtac. (Daniel Fountaine) Um, so they're they're, you know, they may come up with a solution

1:09:00

(Daniel Fountaine) that's a lot more robust and and more in-depth and more secure than what (Daniel Fountaine) what I've kind of laid out for your scenario is is having that plugin that

1:09:08

(Daniel Fountaine) kind of bridges. Um, and I think (Daniel Fountaine) if that does take take off and it does appear to have pretty good

1:09:16

(Daniel Fountaine) traction, um, cuz like I said, they we've had a couple of conversations (Daniel Fountaine) and then they've taken things back to their their state and local or state

1:09:24

(Daniel Fountaine) and federal agencies to kind of see if we can make it happen. And that (Daniel Fountaine) is um, you know, these

1:09:32

(Daniel Fountaine) conversations started in the Helen response. So this is something that like (Daniel Fountaine) other people are thinking about and like how how do

1:09:40

(Daniel Fountaine) we how do we connect these um and I think (Daniel Fountaine) that's that would be really awesome

1:09:48

(Daniel Fountaine) if we could see that like take place and make that (Daniel Fountaine) happen quickly. uh you know it's too late to say before this hurricane season or

1:09:56

(Daniel Fountaine) whatever because we're 3 days into it - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah. Oh my (Daniel Fountaine) now

1:10:04

(Daniel Fountaine) but I think a tech is a really cool platform it's it's - (Hopefully Abysmal (Elryan The Explorer)) gosh. Yeah. Yeah. (Daniel Fountaine) difficult to build to configure for your organization and what - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:10:12

(Daniel Fountaine) you're doing and your nature of response (Daniel Fountaine) um but it it's like I said

1:10:20

(Daniel Fountaine) it it works with the goenant and meshtastic stuff which makes it more (Daniel Fountaine) functional in the field than Google Maps or like literally anything else unless you

1:10:28

(Daniel Fountaine) have like a nons smart (Daniel Fountaine) GPS device. Uh but then you're you're just

1:10:36

(Daniel Fountaine) limited to GPS location. Like you can track where you are, but you can't track where your buddy is (Daniel Fountaine) or you know your squad commander can't can - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah.

1:10:44

(Daniel Fountaine) track where anybody else - (Hopefully Abysmal (Elryan The Explorer)) So, so on our (Daniel Fountaine) is. - (Hopefully Abysmal (Elryan The Explorer)) end for like short term potentially like look for interoperability with the

1:10:52

(Hopefully Abysmal (Elryan The Explorer)) meshtastic and the go I forgot what it was go something (Daniel Fountaine) Go. Tenna. It's like antenna - (Hopefully Abysmal (Elryan The Explorer)) what was it

1:11:00

(Daniel Fountaine) but go instead of - (Hopefully Abysmal (Elryan The Explorer)) goenna. Yeah. But like potentially looking for interoperability between (Hopefully Abysmal (Elryan The Explorer)) those systems instead of like the tax system and then potentially like later on

1:11:08

(Hopefully Abysmal (Elryan The Explorer)) once if we have like a audience that uses the platform. (Daniel Fountaine) an - (Hopefully Abysmal (Elryan The Explorer)) Um build out this plugin and like are like working to

1:11:16

(Hopefully Abysmal (Elryan The Explorer)) have something like that adopted um like lobby (Hopefully Abysmal (Elryan The Explorer)) for some form of like civ gov

1:11:24

(Hopefully Abysmal (Elryan The Explorer)) interaction. Um and then from there maybe have that be the course of (Daniel Fountaine) So if you if you're looking at just the civ - (Hopefully Abysmal (Elryan The Explorer)) action.

1:11:32

(Daniel Fountaine) side, I think that the inner connection stuff is a lot (Daniel Fountaine) easier

1:11:40

(Daniel Fountaine) um than the the civ to gov. (Daniel Fountaine) um you know there's a for you know for security reasons and stuff

1:11:48

(Daniel Fountaine) like that like uh - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah. Yeah. (Daniel Fountaine) um like I said I think a tech is a really good platform and it's built to do

1:11:56

(Daniel Fountaine) a lot of the same stuff like in like the military application is (Daniel Fountaine) not that far off from the disaster response application.

1:12:04

(Daniel Fountaine) So - (Hopefully Abysmal (Elryan The Explorer)) Yeah, just like more locked down, I'd bet. (Daniel Fountaine) there's well I mean in the the mill version you can do stuff like

1:12:12

(Daniel Fountaine) like designate a target and stuff like that like that (Daniel Fountaine) functionality. Um doesn't exist on the civ and gov - (Hopefully Abysmal (Elryan The Explorer)) But

1:12:20

(Daniel Fountaine) side. Um but it and there there's other like (Daniel Fountaine) gov only plugins and stuff like that that kind of add some more

1:12:28

(Daniel Fountaine) functionality to it. Um, you can like set drone surveillance paths (Daniel Fountaine) and stuff like that and um, you know, that kind of stuff that you don't need on the - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:12:36

(Daniel Fountaine) civ - (Hopefully Abysmal (Elryan The Explorer)) Crazy. You could use the drones in a disaster relief (Daniel Fountaine) side. Um, you definitely can with - (Hopefully Abysmal (Elryan The Explorer)) situation, could you not?

1:12:44

(Daniel Fountaine) the right authorization because a lot of times they put up uh, no fly (Daniel Fountaine) zones in in disaster areas. Uh, Helen was interesting - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Oh, yeah. I bet.

1:12:52

(Daniel Fountaine) because they didn't and that allowed for for helicopter work to take - (Hopefully Abysmal (Elryan The Explorer)) Oh my (Daniel Fountaine) place um by by civilians. - (Hopefully Abysmal (Elryan The Explorer)) goodness. Oh,

1:13:00

(Daniel Fountaine) There was lots of helicopter traffic for - (Hopefully Abysmal (Elryan The Explorer)) cool. Heck yeah. (Daniel Fountaine) sure. Uh, - (Hopefully Abysmal (Elryan The Explorer)) Oh. Uh, yeah. Pros and

1:13:08

(Daniel Fountaine) yeah. And and they, like I said, they usually shut down (Daniel Fountaine) drone operations. Uh, so you you would have to be partnered with a local - (Hopefully Abysmal (Elryan The Explorer)) cons.

1:13:16

(Daniel Fountaine) agency to to get a drone in the air in situations like that. I - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah. (Daniel Fountaine) think uh they're even pushing to further

1:13:24

(Daniel Fountaine) the penalties for that because somebody crashed a drone into (Daniel Fountaine) the air tankers in the California - (Hopefully Abysmal (Elryan The Explorer)) Oh

1:13:32

(Daniel Fountaine) wildfires. So, but you know, (Daniel Fountaine) partnering with with a local agency is not that difficult and you can usually get what you

1:13:40

(Daniel Fountaine) want, especially when you're you're bringing something to the table. - (Hopefully Abysmal (Elryan The Explorer)) no. Okay. (Daniel Fountaine) Um, and that reminds me, there was something that was said

1:13:48

(Daniel Fountaine) about tracking tasks and completion and stuff like (Daniel Fountaine) that. Um, there - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:13:56

(Daniel Fountaine) is, and this is something that I've brought up to SOS and I believe they are working on (Daniel Fountaine) a way to integrate it, but there is a FEMA IC

1:14:04

(Daniel Fountaine) form that also tracks - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) activity in tasks completed and and stuff like that.

1:14:12

(Daniel Fountaine) Um, and as an NGO (Daniel Fountaine) responding to an area, if you can

1:14:20

(Daniel Fountaine) say to to the agency that that's, you know, the local (Daniel Fountaine) agency, you're you're trying to make entry and contact and do work. If you

1:14:28

(Daniel Fountaine) can say that, hey, I'll provide you with this IC form 106 um (Daniel Fountaine) that tracks our activity and work,

1:14:36

(Daniel Fountaine) um they are going to be significantly more likely to work with (Daniel Fountaine) you because after everything is said and done, if your agency or

1:14:44

(Daniel Fountaine) organization revs up their their operations and you can hand like the county (Daniel Fountaine) EMA that FEMA form that tracks all your activity and

1:14:52

(Daniel Fountaine) everything you've done, that makes it easier for them to (Daniel Fountaine) file for reimbursement. from FEMA. So, they get a little bit of

1:15:00

(Daniel Fountaine) credit back saying, "Hey, you had volunteers out here doing all this. We know that, you (Daniel Fountaine) know, it it allows them to get a little makes things - (Hopefully Abysmal (Elryan The Explorer)) interesting.

1:15:08

(Daniel Fountaine) a little bit easier for them to get their FEMA reimbursement for the work that was done. Um, (Daniel Fountaine) and you know, as a as a nonprofit, like we don't we don't charge anything. We don't

1:15:16

(Daniel Fountaine) do like bill for anything or anything like that, but being able to to bring that (Daniel Fountaine) value ad to the EMA and say, "Hey, when when we wrap up, like

1:15:24

(Daniel Fountaine) I'll be able to give you that FEMA IC (Daniel Fountaine) form." Um, it's it's like a huge attractor. And I've - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:15:32

(Daniel Fountaine) I've gotten had that conversation with quite a - (Hopefully Abysmal (Elryan The Explorer)) Oh yeah. (Daniel Fountaine) few EMAs across a couple of different states about like if we can give you this

1:15:40

(Daniel Fountaine) form, does that make you more inclined to work with us? And they're like 100% yep, (Daniel Fountaine) absolutely. If you if you come to me and say, "Hey, uh, we want to come do

1:15:48

(Daniel Fountaine) some work in your community. We understand there's a need and we can give you this (Daniel Fountaine) FEMA form that shows everything that we've done." Um,

1:15:56

(Daniel Fountaine) like they're like, "You're top of the list." Like, "You're you're in. Come on, get in (Daniel Fountaine) here." Um, - (Hopefully Abysmal (Elryan The Explorer)) Okay. You said ICS form 106 and that's from

1:16:04

(Daniel Fountaine) I I I made that up. I don't know what the actual - (Hopefully Abysmal (Elryan The Explorer)) FEMA as an FEMA. (Daniel Fountaine) form is, but it is a it's an IC - (Hopefully Abysmal (Elryan The Explorer)) Oh, sorry.

1:16:12

(Daniel Fountaine) form. (Hopefully Abysmal (Elryan The Explorer)) Because potentially it could be just

1:16:20

(Hopefully Abysmal (Elryan The Explorer)) like we have like this log of tasks that have been completed and just use (Hopefully Abysmal (Elryan The Explorer)) an LLM to fill out the form, have a human verify it, and then like

1:16:28

(Hopefully Abysmal (Elryan The Explorer)) it's just a conversion utility from whatever we're tracking to (Hopefully Abysmal (Elryan The Explorer)) whatever they need on the form. Could be a value

1:16:36

(Daniel Fountaine) Uh yeah. Yeah. Uh SOS is working on a way to do most of the (Daniel Fountaine) FEMA forms. Um what what we have - (Hopefully Abysmal (Elryan The Explorer)) proposition. Interesting.

1:16:44

(Daniel Fountaine) found is that using the same (Daniel Fountaine) training and language and forms that

1:16:52

(Daniel Fountaine) the you know state, local and federal (Daniel Fountaine) agencies use uh allows us to be kind of on the

1:17:00

(Daniel Fountaine) same page when we're talking about stuff. So So we - (Hopefully Abysmal (Elryan The Explorer)) Cool. Yeah. (Daniel Fountaine) tend to use the the FEMA forms and we use FEMA training

1:17:08

(Daniel Fountaine) for some of the stuff. um like our organization and (Daniel Fountaine) even Kinjun Navy Relief had the the same requirement

1:17:16

(Daniel Fountaine) um is that you take your your FEMA ICS 100, (Daniel Fountaine) 200, 700 and 800 and that's the basic incident command

1:17:24

(Daniel Fountaine) structure in a you know next level incident command structure (Daniel Fountaine) and uh NIMS which is the national emergency

1:17:32

(Daniel Fountaine) response um or emergency management or something like that. (Daniel Fountaine) It's the national version of the almost the same thing. it just gets a little bit

1:17:40

(Daniel Fountaine) bigger. Um, that that will help you have (Daniel Fountaine) a better understanding of what is taking place in

1:17:48

(Daniel Fountaine) uh a disaster or an incident response and allow you to (Daniel Fountaine) communicate the same language with emergency - (Hopefully Abysmal (Elryan The Explorer)) His

1:17:56

(Daniel Fountaine) responders and emergency management agencies and stuff like that, those EMAs. (Hopefully Abysmal (Elryan The Explorer)) Shoot. Maybe I need to take

1:18:04

(Daniel Fountaine) Um, I 100% if you're going to be in the space, I would highly recommend it. They're (Daniel Fountaine) they're really easy. Um they just take time really.

1:18:12

(Daniel Fountaine) Uh nope. It's - (Hopefully Abysmal (Elryan The Explorer)) those. Okay. Is there a cost associated or I can I can get (Daniel Fountaine) 100% free. - (Hopefully Abysmal (Elryan The Explorer)) funding here. Sweet. And you said IC 100,

1:18:20

(Daniel Fountaine) You uh so the - (Hopefully Abysmal (Elryan The Explorer)) 200, 700, and 800. And then Nims (Daniel Fountaine) ICS 100 and 200 cover the incident command structure and then

1:18:28

(Daniel Fountaine) uh 700 and 800 cover - (Hopefully Abysmal (Elryan The Explorer)) what? (Daniel Fountaine) NIMS. They're they're all like ICS stands for like - (Hopefully Abysmal (Elryan The Explorer)) Oh, okay.

1:18:36

(Daniel Fountaine) independent course of study or something like that. Uh or (Daniel Fountaine) independent may maybe it's uh maybe I'm using the

1:18:44

(Daniel Fountaine) wrong abbreviation there. I think it's IC 100 - (Hopefully Abysmal (Elryan The Explorer)) Okay. Okay. (Daniel Fountaine) 200. But if you search IC 100 200 you're going to end up on the right

1:18:52

(Daniel Fountaine) page. uh you have to create uh a (Daniel Fountaine) FEMA uh student account or whatever uh which is

1:19:00

(Daniel Fountaine) again free and it gives you a a student ID number and you need to (Daniel Fountaine) track that and keep track of that for sure because that's how you're going to

1:19:08

(Daniel Fountaine) be able to claim credit for all the courses. - (Hopefully Abysmal (Elryan The Explorer)) True. Cool. (Daniel Fountaine) Um, no, but so those uh those are kind of like

1:19:16

(Daniel Fountaine) the basic um and that that'll go over some (Daniel Fountaine) of the forms that you'll use. And then the ICS forms

1:19:24

(Daniel Fountaine) um that you're you fill out as a responding (Daniel Fountaine) agency cover like the the type of incident and like

1:19:32

(Daniel Fountaine) the nature of the environment and like what what (Daniel Fountaine) the incident is and what the response to the incident will

1:19:40

(Daniel Fountaine) be. And then as you plan and change like you just rewrite (Daniel Fountaine) those forms and if you use that uh incident

1:19:48

(Daniel Fountaine) command structure uh which is you know basically chain of (Daniel Fountaine) command you know who's in charge and who's next in charge and that kind of thing.

1:19:56

(Daniel Fountaine) Um and breaks it down into different areas of (Daniel Fountaine) response. So like logistics and supplies and

1:20:04

(Daniel Fountaine) uh you know regular operations and stuff like that (Daniel Fountaine) like like rescue or or you know delivering food or

1:20:12

(Daniel Fountaine) whatever that would be your operations side of things. And so each of those departments will have (Daniel Fountaine) their own set of paperwork that they fill out and as everybody

1:20:20

(Daniel Fountaine) wraps up the day essentially they give their paperwork to the incident commander. the incident commander reviews (Daniel Fountaine) the paperwork and kind of signs off on it like yeah this is what we talked about and agreed

1:20:28

(Daniel Fountaine) and you know as the incident commander signs off on things (Daniel Fountaine) that's essentially validating that you know what

1:20:36

(Daniel Fountaine) was done was authorized and approved and covered (Daniel Fountaine) by your organization or your agency and

1:20:44

(Daniel Fountaine) um you know that covers everything from you know requesting (Daniel Fountaine) a box of pencils to requesting a firetruck and a crew to run the firetruck

1:20:52

(Daniel Fountaine) and um familiarizing yourself with at least the forms, even if (Daniel Fountaine) you're not like a responding person or individual or

1:21:00

(Daniel Fountaine) agency. Understanding the forms and what happens (Daniel Fountaine) in in a disaster response is incredibly

1:21:08

(Daniel Fountaine) helpful with understanding how to track some of this (Daniel Fountaine) stuff. Um the correct IC form

1:21:16

(Daniel Fountaine) is IC form 214. 214 (Daniel Fountaine) is essentially like an activity log and each

1:21:24

(Daniel Fountaine) department that is part of a response will have a (Daniel Fountaine) 214 and then those are essentially like stapled together and that's

1:21:32

(Daniel Fountaine) your your organization's (Daniel Fountaine) 214.

1:21:40

(Daniel Fountaine) Um, I have had some pretty really in-depth conversations (Daniel Fountaine) with SOS on how to

1:21:48

(Daniel Fountaine) use like their generic application that they're (Daniel Fountaine) building type of forms and layout to gather the information that

1:21:56

(Daniel Fountaine) goes into the IC form and then just autopop populated into the form. Like all of these forms (Daniel Fountaine) are a PDF that you can download for free online and being able - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:22:04

(Daniel Fountaine) to gather that information in a way (Daniel Fountaine) that doesn't look like a FEMA form is incredibly

1:22:12

(Daniel Fountaine) helpful. And you're like 10,000% more likely to get somebody to fill it out (Daniel Fountaine) if it's an app or if it's a a you know a website drop down or - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:22:20

(Daniel Fountaine) something. Uh and then some of that information doesn't change (Daniel Fountaine) from one form to another form for the whole - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:22:28

(Daniel Fountaine) incident. So it's like the top header of the form is almost exactly the same the (Daniel Fountaine) whole time. So being able to

1:22:36

(Daniel Fountaine) mark which ones are consistent and persistent (Daniel Fountaine) across all the forms um makes it a lot easier. And so they're working on

1:22:44

(Daniel Fountaine) on that side of things as well. And then (Daniel Fountaine) also at the beginning of setting up like an incident where it starts to gather all

1:22:52

(Daniel Fountaine) this information you would mark what forms you need to fill out. (Daniel Fountaine) So, you know, as a NGO, we don't need all of the forms, but

1:23:00

(Daniel Fountaine) having some of them is beneficial not only to us to keep track of (Daniel Fountaine) what we're doing as as a response, but also, you know, to the

1:23:08

(Daniel Fountaine) EMAs when we can say, "Hey, we can hand over our FEMA forms when we're done and you'll have a copy." (Daniel Fountaine) Um,

1:23:16

(Daniel Fountaine) and I think we've spent probably about six, seven (Daniel Fountaine) hours like going through all the forms and figuring out what's what and and

1:23:24

(Daniel Fountaine) helping SOS get that squared away so (Daniel Fountaine) that they will have like the FEMA forms as a value ad when

1:23:32

(Daniel Fountaine) they start to market their product to to other NOS's and nonprofits to (Daniel Fountaine) to be able to help pull some of that

1:23:40

(Daniel Fountaine) audience over there. Um, if (Daniel Fountaine) that sounds like something that y'all are looking for on - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:23:48

(Daniel Fountaine) your project, again, I'm I'm happy to provide that information and walk (Daniel Fountaine) through it and show you the ins and outs of FEMA

1:23:56

(Hopefully Abysmal (Elryan The Explorer)) I'd say it definitely cannot hurt. Um, I do (Daniel Fountaine) forms. - (Hopefully Abysmal (Elryan The Explorer)) think we're going to be probably pushing more for like civilian sided

1:24:04

(Hopefully Abysmal (Elryan The Explorer)) usage. um not just the NOS's themselves but having the (Hopefully Abysmal (Elryan The Explorer)) interoperability with the NOS's and having this be like the R4

1:24:12

(Hopefully Abysmal (Elryan The Explorer)) dash type thing um be usable by these NOS's (Hopefully Abysmal (Elryan The Explorer)) for some extra value ad um definitely would not

1:24:20

(Hopefully Abysmal (Elryan The Explorer)) hurt um the more and more I hear you talking about SOS I got to just have a meeting (Hopefully Abysmal (Elryan The Explorer)) with these people they seem to be like right in line with what we're trying to do we just might be able

1:24:28

(Daniel Fountaine) Hey. - (Hopefully Abysmal (Elryan The Explorer)) to just like just branch it a bit or something I don't (Daniel Fountaine) Um, I I'll get on Adrenina here in a little bit

1:24:36

(Daniel Fountaine) and maybe maybe do an introduction and get y'all y'all talking and see if there's something we can - (Hopefully Abysmal (Elryan The Explorer)) That would be much (Daniel Fountaine) all work on together. Um, - (Hopefully Abysmal (Elryan The Explorer)) appreciated. Hell

1:24:44

(Daniel Fountaine) The there was something I was going to add there. (Daniel Fountaine) Oh, I think a way to - (Hopefully Abysmal (Elryan The Explorer)) yeah.

1:24:52

(Daniel Fountaine) capture more people and get them involved in in your platform is (Daniel Fountaine) probably maybe a little bit of targeting towards those NOS's because if you

1:25:00

(Daniel Fountaine) get an organization like like CNR or (Daniel Fountaine) Rancher Navy or um you know I also work with

1:25:08

(Daniel Fountaine) with animal if you get like the organization involved and added to (Daniel Fountaine) their platform in a way that they can leverage - (Hopefully Abysmal (Elryan The Explorer)) Okay.

1:25:16

(Daniel Fountaine) it then you get their their entire org as like a - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) bonus. Like that's if you bring the NGO on, you will get their - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:25:24

(Daniel Fountaine) their volunteer base on. So, you know, - (Hopefully Abysmal (Elryan The Explorer)) Yeah, fair (Daniel Fountaine) for CNR, that's probably a lot less now,

1:25:32

(Daniel Fountaine) but like, you know, two two to 6K maybe - (Hopefully Abysmal (Elryan The Explorer)) enough. (Daniel Fountaine) uh right away. Uh so, I probably wouldn't target that one - (Hopefully Abysmal (Elryan The Explorer)) Dang.

1:25:40

(Daniel Fountaine) first while you're still testing and developing. But like for for rancher (Daniel Fountaine) navy our our core group is like seven people. So that's - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Okay.

1:25:48

(Daniel Fountaine) like board of directors and then higher leadership and then (Daniel Fountaine) we are onboarding volunteers and have ironed out our process

1:25:56

(Daniel Fountaine) pretty well already. So as we continue to grow that would (Daniel Fountaine) be a good way. I'm I'm using Rancher Navy as an example. - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:26:04

(Daniel Fountaine) I'm not trying to imply or say anything, but capturing that (Daniel Fountaine) organization and their their base members and then as they grow that gives you the ability

1:26:12

(Daniel Fountaine) to test and development while scaling for (Daniel Fountaine) that organization. So you can see what growth looks like for your

1:26:20

(Daniel Fountaine) platform, what it looks like for for resource demand and stuff like (Daniel Fountaine) that, but - (Hopefully Abysmal (Elryan The Explorer)) That sounds like that's what we're going to do. Like to be honest,

1:26:32

(Hopefully Abysmal (Elryan The Explorer)) like (Daniel Fountaine) We've I've looked at a lot of different tools in terms of

1:26:40

(Daniel Fountaine) of doing this disaster response stuff and - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) and you know dispatching and coordinating and you

1:26:48

(Daniel Fountaine) know have a need and trying to get like rescuers or (Daniel Fountaine) supplies to that need. And it has

1:26:56

(Daniel Fountaine) always been either a super huge price tag because it's geared (Daniel Fountaine) toward like you know, funded

1:27:04

(Daniel Fountaine) agencies like like you know, police departments or emergency - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) response agencies um that get funding in grants from,

1:27:12

(Daniel Fountaine) you know, taxes and and all over the place. (Daniel Fountaine) Um so there's, you know, they they market that with a price tag that

1:27:20

(Daniel Fountaine) makes sense for them and their audience. uh those (Daniel Fountaine) applications would be amazing for NOS's who operate

1:27:28

(Daniel Fountaine) in a very similar space if not the exact same space in terms of d disaster (Daniel Fountaine) response but the issue is you

1:27:36

(Daniel Fountaine) know your your nonprofit organization your NGOs's can't afford that price tag (Daniel Fountaine) and there's no like real price break on

1:27:44

(Daniel Fountaine) a lot of that even having a lot of (Daniel Fountaine) these conversations with a lot of different you know companies that have these

1:27:52

(Daniel Fountaine) platforms and these programs programs. They offer a price break, but (Daniel Fountaine) it doesn't bring it within the realm of possibility for for

1:28:00

(Daniel Fountaine) NOS's and nonprofits. (Daniel Fountaine) Um, and - (Hopefully Abysmal (Elryan The Explorer)) Yeah. No, we are operating under a nonprofit by the way. Um, so

1:28:08

(Hopefully Abysmal (Elryan The Explorer)) like the way that this would probably go out is it covers the overhead um and (Hopefully Abysmal (Elryan The Explorer)) paying staff, but past that ideally it would be

1:28:16

(Daniel Fountaine) then - (Hopefully Abysmal (Elryan The Explorer)) like not doing that. (Daniel Fountaine) the The other aspect is of

1:28:24

(Daniel Fountaine) it is is there's a lot of open source stuff that you could also leverage - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) in the same way but but the problem with a lot of that - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:28:32

(Daniel Fountaine) is is it's not maintained. - (Hopefully Abysmal (Elryan The Explorer)) 100%. (Daniel Fountaine) Uh so there's like a a dispatch and mapping

1:28:40

(Daniel Fountaine) solution out there that that I've looked at before and it hasn't been (Daniel Fountaine) updated in probably eight years. So like I'm not going to pick - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:28:48

(Daniel Fountaine) that to go with because that just that's inheriting (Daniel Fountaine) security risk like um

1:28:56

(Daniel Fountaine) and then there there are some solutions that are relatively inexpensive but then they're (Daniel Fountaine) not geared towards nonprofits and NOS's

1:29:04

(Daniel Fountaine) in our type of response. So, it's like a a police dispatching software - (Hopefully Abysmal (Elryan The Explorer)) Yep. (Daniel Fountaine) that's like again relatively inexpensive for what it brings to the table,

1:29:12

(Daniel Fountaine) but it doesn't (Daniel Fountaine) offer the a level of customization where we can configure it to do

1:29:20

(Daniel Fountaine) what we need to do or it uses a lot of uh (Daniel Fountaine) vernacular that's not disaster response related and more

1:29:28

(Daniel Fountaine) like police operations related and investigations related and it's (Daniel Fountaine) not really it's not really a good fit. like it's a good platform and

1:29:36

(Daniel Fountaine) it looks really good and it functions for what we need to do. Like I could (Daniel Fountaine) 100% take that platform and use it. Uh but that means that

1:29:44

(Daniel Fountaine) like there's a field that that talks about, you know, suspect. Like I'm not going to (Daniel Fountaine) use a field that talks about a suspect because we don't have a suspect. Like there's a lot of

1:29:52

(Daniel Fountaine) stuff that doesn't make sense. (Daniel Fountaine) Um and then

1:30:00

(Daniel Fountaine) like that's pretty much it. Like that's that's the the slices of the pie that's available (Daniel Fountaine) for doing stuff like this is it's like a really high price tag uh

1:30:08

(Daniel Fountaine) super outdated open source or something - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) that you know it's like a square square peg in a round hole. like

1:30:16

(Daniel Fountaine) it it can work, but it's not going to (Daniel Fountaine) be like you're going to have to develop your own training to teach people like we don't

1:30:24

(Daniel Fountaine) use this field or this field means something else to (Daniel Fountaine) us. Uh to repurpose something that's not really designed for it into what we

1:30:32

(Daniel Fountaine) need. Um, which I think is again part of (Daniel Fountaine) what sparked Micah to go off and try and build his own thing

1:30:40

(Daniel Fountaine) and started us working on that is like we need something (Daniel Fountaine) that works for disaster response that's not,

1:30:48

(Daniel Fountaine) you know, 12K or (Daniel Fountaine) uh, you know, has baked in security

1:30:56

(Daniel Fountaine) issues and stuff like that. - (Hopefully Abysmal (Elryan The Explorer)) Yeah. One one thing that was brought up that is kind (Hopefully Abysmal (Elryan The Explorer)) of interesting to me though is so like with the different fields

1:31:04

(Hopefully Abysmal (Elryan The Explorer)) um like usually the reason for that is like there's different database (Hopefully Abysmal (Elryan The Explorer)) schema for the way things are stored, right? um because like each each

1:31:12

(Hopefully Abysmal (Elryan The Explorer)) thing needs to be stored a specific way. Um apparently it's (Hopefully Abysmal (Elryan The Explorer)) a ongoing thing to be building out some form of

1:31:20

(Hopefully Abysmal (Elryan The Explorer)) like open standard for um like (Hopefully Abysmal (Elryan The Explorer)) databasing of like needs um and like the the kind of

1:31:28

(Hopefully Abysmal (Elryan The Explorer)) the kind of ticketing system. Um, one thing that I was kind of curious on (Hopefully Abysmal (Elryan The Explorer)) is um, like what are your thoughts on like how would

1:31:36

(Hopefully Abysmal (Elryan The Explorer)) we build out something that would be more universally (Hopefully Abysmal (Elryan The Explorer)) applicable or would we have to figure out way to just um, be more

1:31:44

(Hopefully Abysmal (Elryan The Explorer)) interoperable between the different types of relief? Um, you know, because (Hopefully Abysmal (Elryan The Explorer)) like as stated, like y'all don't have like a a field for subject, a

1:31:52

(Hopefully Abysmal (Elryan The Explorer)) suspect, but I bet like whatever forms that the like police (Hopefully Abysmal (Elryan The Explorer)) department has to fill out, like that is something that's like mandatory, is it

1:32:00

(Daniel Fountaine) for for police operations. Yeah. But for - (Hopefully Abysmal (Elryan The Explorer)) not? (Daniel Fountaine) what we do, it would not necessarily be the same

1:32:08

(Daniel Fountaine) form. um e even even in - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah. (Daniel Fountaine) like disaster response mode like the forms that the - (Hopefully Abysmal (Elryan The Explorer)) I Yeah.

1:32:16

(Daniel Fountaine) police department fills out doesn't necessarily or easily translate to like (Daniel Fountaine) a FEMA form that would be something that we would have to fill out. So even though like that

1:32:24

(Daniel Fountaine) one platform had really good reporting tools and being able (Daniel Fountaine) to to manage particular

1:32:32

(Daniel Fountaine) tickets in a in a a really in-depth way. A (Daniel Fountaine) lot of that doesn't necessarily apply or work well

1:32:40

(Daniel Fountaine) with the disaster response stuff or translate to like a FEMA form that you (Daniel Fountaine) could be like, "Okay, well, I'm going to take this report and just write

1:32:48

(Daniel Fountaine) FEMA form da da d d d d d d at the top and now it's a FEMA form." (Daniel Fountaine) Uh, and one of the one of the other

1:32:56

(Daniel Fountaine) issues like I covered these different categories of of problems (Daniel Fountaine) when finding a software solution. There

1:33:04

(Daniel Fountaine) are emergency (Daniel Fountaine) management or emergency response software packages that are

1:33:12

(Daniel Fountaine) out there that are customizable (Daniel Fountaine) and you could build it out to do whatever you want it to do whether that's you

1:33:20

(Daniel Fountaine) know ticketing dispatch or that's uh you know (Daniel Fountaine) weather monitoring or flood monitoring or all these different

1:33:28

(Daniel Fountaine) things but that in itself is the problem for that platform. It (Daniel Fountaine) is way too customizable for

1:33:36

(Daniel Fountaine) a nonprofit and NGO to turn around and configure that to fit our (Daniel Fountaine) needs because we don't have, you know, somebody who's putting

1:33:44

(Daniel Fountaine) in 40 hours a week. We have somebody who has like four hours a day that wants (Daniel Fountaine) to volunteer their time and then you have to have somebody who's

1:33:52

(Daniel Fountaine) techsavvy enough to understand all of this stuff and how to (Daniel Fountaine) build it. And so it takes an enormous amount of

1:34:00

(Daniel Fountaine) volunteer time to take that platform and then build it to what you (Daniel Fountaine) need. And then by by then, you know,

1:34:08

(Daniel Fountaine) it's it creates its own headaches. We had there's there's a (Daniel Fountaine) program called uh

1:34:16

(Daniel Fountaine) oh s***, this is going to be another one that escapes me and it's going to bug me until I figure out what - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) it was. There there was a uh an emergency response emergency - (Hopefully Abysmal (Elryan The Explorer)) Oh.

1:34:24

(Daniel Fountaine) management platform that was built out to kind of like that huge (Daniel Fountaine) customizable monster uh that can work for

1:34:32

(Daniel Fountaine) fire, police, EMS, um regular emergency (Daniel Fountaine) management. Like it's its original development path was emergency management and then it kind of added

1:34:40

(Daniel Fountaine) all these other things. Um, and it, you know, (Daniel Fountaine) in a demo it looks really nice and really focused towards what we want

1:34:48

(Daniel Fountaine) and could do and they were willing to donate the the cost of the (Daniel Fountaine) platform to our organization. Um,

1:34:56

(Daniel Fountaine) and I wasn't part of the organization when they made that decision and they they said, (Daniel Fountaine) "Yeah, give me that platform for free." And they said, "Okay, here's your credentials. Good

1:35:04

(Daniel Fountaine) luck." Uh, and so then we had this huge monster - (Hopefully Abysmal (Elryan The Explorer)) Good (Daniel Fountaine) that nobody knew anything about. And like they had

1:35:12

(Daniel Fountaine) also donated like uh I want to say it (Daniel Fountaine) was like $2,500 worth of like training credits

1:35:20

(Daniel Fountaine) that you could turn around and go and take the training course. Uh well - (Hopefully Abysmal (Elryan The Explorer)) luck. (Daniel Fountaine) like four or five people took the training courses and went through and learned all the ins

1:35:28

(Daniel Fountaine) and outs of the program and then like you know two months later left the (Daniel Fountaine) org. Uh so then all the credits were used and nobody knows how to configure the - (Hopefully Abysmal (Elryan The Explorer)) Oh

1:35:36

(Daniel Fountaine) platform and uh it's this (Daniel Fountaine) huge super configurable customizable monster that nobody knows how to

1:35:44

(Daniel Fountaine) tame. Um and luckily - (Hopefully Abysmal (Elryan The Explorer)) man. Yep. (Daniel Fountaine) through the training they kind of built some of it out so it wasn't like

1:35:52

(Daniel Fountaine) completely and totally useless right off the bat. So those couple of folks that went through (Daniel Fountaine) it kind of toyed around with it like as part of the training

1:36:00

(Daniel Fountaine) exercise and built the platform a little bit. (Daniel Fountaine) Uh but it was essentially useless. I mean we

1:36:08

(Daniel Fountaine) we leveraged that tool for (Daniel Fountaine) much longer than we should have. Uh and then we went and talked with - (Hopefully Abysmal (Elryan The Explorer)) Okay.

1:36:16

(Daniel Fountaine) the company again who donated it and said, "Hey, uh (Daniel Fountaine) this isn't really working for us. like could we pay you something to build it for

1:36:24

(Daniel Fountaine) us? Uh and you know we had the money to do so. And their answer (Daniel Fountaine) was m I don't know we're about

1:36:32

(Daniel Fountaine) to launch version two of this platform so how about we just give (Daniel Fountaine) you version two of the platform for free. And then we were right in

1:36:40

(Daniel Fountaine) the same boat. Like they didn't include training credits this time. - (Hopefully Abysmal (Elryan The Explorer)) Uh, yep. (Daniel Fountaine) Uh so we were in my opinion more screwed than we were - (Hopefully Abysmal (Elryan The Explorer)) Oh,

1:36:48

(Daniel Fountaine) originally. And then they they deprecated the old platform. So all the - (Hopefully Abysmal (Elryan The Explorer)) yep. (Daniel Fountaine) data had to be migrated off of it so that we would just have records of - (Hopefully Abysmal (Elryan The Explorer)) Yep.

1:36:56

(Daniel Fountaine) everything. Uh but we had no place to import it into the new platform (Daniel Fountaine) or like there wasn't a way to export the configuration from the old

1:37:04

(Daniel Fountaine) platform and import it into the new platform. So we couldn't (Daniel Fountaine) even use version two to the same capacity we were on in version one.

1:37:12

(Daniel Fountaine) It was it was really expensive software and it (Daniel Fountaine) was really nice uh in terms of what it could do

1:37:20

(Daniel Fountaine) but it was more of a headache than (Daniel Fountaine) a solution to the problem. - (Hopefully Abysmal (Elryan The Explorer)) sounds like

1:37:28

(Daniel Fountaine) And I think those (Daniel Fountaine) are the main categories of issues that we find with just about any other platform

1:37:36

(Daniel Fountaine) you look at whether it's like web EOC or (Daniel Fountaine) um you know there's uh 108 - (Hopefully Abysmal (Elryan The Explorer)) it.

1:37:44

(Daniel Fountaine) systems and stuff like that. There's there's a lot of different platforms out there for this but none (Daniel Fountaine) of them are really built

1:37:52

(Daniel Fountaine) or focused for disaster response. And I think that's problematic. (Daniel Fountaine) I mean that so that platform that huge platform that's customizable uh Red

1:38:00

(Daniel Fountaine) Cross uses that platform so like it's a good platform and it can be built to - (Hopefully Abysmal (Elryan The Explorer)) That's (Daniel Fountaine) do disaster response but it takes like you know uh

1:38:08

(Daniel Fountaine) it 10,000 hours or you know $5,000 (Daniel Fountaine) to to build it and it's just - (Hopefully Abysmal (Elryan The Explorer)) good. Yeah. No, I

1:38:16

(Hopefully Abysmal (Elryan The Explorer)) get you. I don't know. Um, it's a lot to (Daniel Fountaine) problematic. - (Hopefully Abysmal (Elryan The Explorer)) think about. Um, it's also a lot to think about on like terms of scope. Um, we'll

1:38:24

(Hopefully Abysmal (Elryan The Explorer)) we'll definitely be figuring out like what specifically we're trying to bring value proposition (Hopefully Abysmal (Elryan The Explorer)) wise. Um, I mean, I'm actively looking to be like

1:38:32

(Hopefully Abysmal (Elryan The Explorer)) interoperable with pre-existing systems. Um, because like (Hopefully Abysmal (Elryan The Explorer)) we don't want to reinvent any wheels. Um, but at the same time, if there's

1:38:40

(Hopefully Abysmal (Elryan The Explorer)) any wheels that really need to be reinvented just to also help with the price (Hopefully Abysmal (Elryan The Explorer)) tag, it's not the end of the world. Um, we've got some time, we got some

1:38:48

(Hopefully Abysmal (Elryan The Explorer)) funding. Um but (Daniel Fountaine) What are - (Hopefully Abysmal (Elryan The Explorer)) yeah um I would love to keep chatting. What's

1:38:56

(Daniel Fountaine) y'all doing right now for for development? Where are (Hopefully Abysmal (Elryan The Explorer)) up? So currently um the R4 group um

1:39:04

(Hopefully Abysmal (Elryan The Explorer)) so I'm I'm new to the R4 group. Um I just do like full (Daniel Fountaine) y'all? - (Hopefully Abysmal (Elryan The Explorer)) stack dev um and I'm also self-eing backend

1:39:12

(Hopefully Abysmal (Elryan The Explorer)) dev. Um like learning under one of their backend devs. (Hopefully Abysmal (Elryan The Explorer)) Um they've got a like the WNC

1:39:20

(Hopefully Abysmal (Elryan The Explorer)) supply sites um website up. Um during Hurricane Helen, (Hopefully Abysmal (Elryan The Explorer)) they like had a need for getting distribution done

1:39:28

(Hopefully Abysmal (Elryan The Explorer)) between um distribution centers, supply centers, (Hopefully Abysmal (Elryan The Explorer)) um and the general public. So like they built out a

1:39:36

(Hopefully Abysmal (Elryan The Explorer)) like volunteer portal for drivers to (Hopefully Abysmal (Elryan The Explorer)) volunteer to do like driving supplies. Um, and that was

1:39:44

(Hopefully Abysmal (Elryan The Explorer)) basically the like the the whole entire thick of it. Um, (Hopefully Abysmal (Elryan The Explorer)) but I mean, as I said in the video, it's like I I thought

1:39:52

(Hopefully Abysmal (Elryan The Explorer)) that, okay, so we've got all of this logistical like (Hopefully Abysmal (Elryan The Explorer)) setup for supplies, but potentially like having some form

1:40:00

(Hopefully Abysmal (Elryan The Explorer)) of logistical side of like people um (Hopefully Abysmal (Elryan The Explorer)) because like there's plenty of people who are willing to do the volunteering

1:40:08

(Hopefully Abysmal (Elryan The Explorer)) um but it's just like nobody really knows where to do what. (Hopefully Abysmal (Elryan The Explorer)) Um, so like more on the civilian sides, not necessarily on those who are like

1:40:16

(Hopefully Abysmal (Elryan The Explorer)) actively skilled in disaster relief, um, but just general volunteering (Hopefully Abysmal (Elryan The Explorer)) even. Um, like trying to build out some form of portal.

1:40:24

(Hopefully Abysmal (Elryan The Explorer)) Um, you're asking specifically about like the development though. Um, I'm still figuring (Hopefully Abysmal (Elryan The Explorer)) out like my way around their current

1:40:32

(Hopefully Abysmal (Elryan The Explorer)) system. Um, definitely considering like building out kind of from (Hopefully Abysmal (Elryan The Explorer)) scratch. um because a lot of the things that they've gotten built um it's

1:40:40

(Hopefully Abysmal (Elryan The Explorer)) built on Java with um like (Hopefully Abysmal (Elryan The Explorer)) self-hosted let's just say it was built by a experienced back-end

1:40:48

(Hopefully Abysmal (Elryan The Explorer)) developer um so like me coming in from a more like (Hopefully Abysmal (Elryan The Explorer)) intermediate level and more like front-end focused um it's it's

1:40:56

(Hopefully Abysmal (Elryan The Explorer)) a lot to take in all at once um and I definitely think (Hopefully Abysmal (Elryan The Explorer)) we'll probably be just transitioning over to like easier back-end services like

1:41:04

(Hopefully Abysmal (Elryan The Explorer)) switching over to like superbase for database management or like just at a (Hopefully Abysmal (Elryan The Explorer)) AWS um instead of going like the whole self-hosted route because

1:41:12

(Hopefully Abysmal (Elryan The Explorer)) there's like a whole side of that that he was really into that I'm just like it (Hopefully Abysmal (Elryan The Explorer)) seems like so much more of a hassle. I kind of want to just get a product out there, you know.

1:41:20

(Hopefully Abysmal (Elryan The Explorer)) Um yeah, and also um speed and (Hopefully Abysmal (Elryan The Explorer)) scalability. Uh definitely would not be scalable like self-hosted unless we get the money

1:41:28

(Hopefully Abysmal (Elryan The Explorer)) for it. Um but (Hopefully Abysmal (Elryan The Explorer)) yeah, I don't know. Uh was there any specific questions I could try and answer? I kind of

1:41:36

(Daniel Fountaine) No, I I think you covered - (Hopefully Abysmal (Elryan The Explorer)) am just rambling. (Daniel Fountaine) what I was what I was asking about. Uh, Noggin OCA

1:41:44

(Daniel Fountaine) is the platform that was like this huge platform that was just - (Hopefully Abysmal (Elryan The Explorer)) Um, how do you (Daniel Fountaine) like Yeah. If you go to - (Hopefully Abysmal (Elryan The Explorer)) spell that? N O G I

1:41:52

(Daniel Fountaine) uh - (Hopefully Abysmal (Elryan The Explorer)) N. Okay. (Daniel Fountaine) noggin.io, you'll end up at the at their website.

1:42:00

(Daniel Fountaine) Uh and they they got bought by Motorola, I think (Daniel Fountaine) last year. Uh and what's even

1:42:08

(Daniel Fountaine) more comical is so like Noggin was a Australia based (Daniel Fountaine) company. Um my my brother

1:42:16

(Daniel Fountaine) and my wife both work at Motorola. So like they bought this - (Hopefully Abysmal (Elryan The Explorer)) Huh? Oh, (Daniel Fountaine) this platform that like quit using and I was like oh that's kind of - (Hopefully Abysmal (Elryan The Explorer)) nice.

1:42:24

(Hopefully Abysmal (Elryan The Explorer)) Yeah. Sorry, I got a ice cream (Daniel Fountaine) cool that well noise cancelling - (Hopefully Abysmal (Elryan The Explorer)) truck driving past.

1:42:32

(Daniel Fountaine) is doing a good job. I can't hear it. - (Hopefully Abysmal (Elryan The Explorer)) Is it really? Okay, (Daniel Fountaine) Yep. Right. Right there at the end of when you when you speak I can - (Hopefully Abysmal (Elryan The Explorer)) good. So

1:42:40

(Daniel Fountaine) hear like a little bit of the tune outside. (Hopefully Abysmal (Elryan The Explorer)) annoying. Yeah, I'm looking through their stuff. That is

1:42:48

(Daniel Fountaine) I - (Hopefully Abysmal (Elryan The Explorer)) crazy. Um, interesting. (Daniel Fountaine) said really nice platform. It's really

1:42:56

(Daniel Fountaine) cool. Uh and it you know theoretically does all the (Daniel Fountaine) things but you know effectively it's

1:43:04

(Daniel Fountaine) too too big to build out (Daniel Fountaine) for

1:43:12

(Daniel Fountaine) disaster response (Daniel Fountaine) like five 600 - (Hopefully Abysmal (Elryan The Explorer)) Yeah. I think your audio cut

1:43:20

(Daniel Fountaine) people. Can you hear - (Hopefully Abysmal (Elryan The Explorer)) out. Yes. (Daniel Fountaine) me? Okay. I was saying that it's just - (Hopefully Abysmal (Elryan The Explorer)) Yes.

1:43:28

(Daniel Fountaine) like too customizable to be effective for like a nonprofit (Daniel Fountaine) or an NGO or disaster response organization just because even

1:43:36

(Daniel Fountaine) with uh Kinjun Navy Relief being, you know, 5 6 (Daniel Fountaine) thousand plus volunteers. It was like there was four of us that

1:43:44

(Daniel Fountaine) were tech people and like all of (Daniel Fountaine) us collectively don't know s*** about Noggin. So it was like - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:43:52

(Daniel Fountaine) we were having to go in and like play with it (Daniel Fountaine) and learn the configuration and learn how to customize and

1:44:00

(Daniel Fountaine) learn how to build. Uh and you know (Daniel Fountaine) I'm really good at self-eing myself like how to how to do something

1:44:08

(Daniel Fountaine) like I figure out I want to do this thing and then I go figure out how to do it. Um (Daniel Fountaine) but you know not everybody's like that. Not everybody has that drive to go out there and push

1:44:16

(Daniel Fountaine) themselves to learn something else. And so we had, like I said, four or five (Daniel Fountaine) people and by the end of it, it was two of us just hammering away on it, trying to make

1:44:24

(Daniel Fountaine) it work. Uh, like I said, it was semifunctional when (Daniel Fountaine) I came on and it was slightly more functional

1:44:32

(Daniel Fountaine) uh when we just sat down and looked like (Daniel Fountaine) had that real conversation. Is it worth spending all

1:44:40

(Daniel Fountaine) this time to configure and build this or should we just start shopping (Daniel Fountaine) for new software? And that's when we started looking at all the other options

1:44:48

(Daniel Fountaine) that were were on the market. (Daniel Fountaine) Um, and you know, that's when you run into the other issues. It's like everything

1:44:56

(Daniel Fountaine) is either not built for this or (Daniel Fountaine) way outside of our our budget and price range. It's like

1:45:04

(Daniel Fountaine) we I don't know kind of (Daniel Fountaine) burned out on the whole dispatch software and voted that if we

1:45:12

(Daniel Fountaine) didn't have a solution by a certain date, we were just going to turn around and use the noggin again for (Daniel Fountaine) another year and re-evaluate after the end of the hurricane

1:45:20

(Daniel Fountaine) season. - (Hopefully Abysmal (Elryan The Explorer)) Fair enough. I don't (Daniel Fountaine) But there's lots of good stuff out there. There's a yeah

1:45:28

(Daniel Fountaine) there's a platform called Salamander which (Daniel Fountaine) does like inventory management - (Hopefully Abysmal (Elryan The Explorer)) know.

1:45:36

(Daniel Fountaine) of like any type of inventory uh all the way from (Daniel Fountaine) like you know a box of pencils to you know

1:45:44

(Daniel Fountaine) a fire truck and does the maintenance for vehicles like keeps (Daniel Fountaine) track of all those logs does all that stuff and it keeps track of

1:45:52

(Daniel Fountaine) volunteers and it keeps track of staff and it keeps track of who's (Daniel Fountaine) activated for a disaster. And it does like ID and badging and

1:46:00

(Daniel Fountaine) it does um you know personnel management. It does (Daniel Fountaine) incident response management, autofills all your your FEMA

1:46:08

(Daniel Fountaine) IC forms and stuff like that. And it does all these things, but you know (Daniel Fountaine) it's again another $17,000 price tag. Like I - (Hopefully Abysmal (Elryan The Explorer)) Interesting.

1:46:16

(Daniel Fountaine) think um the first year is more expensive because you're - (Hopefully Abysmal (Elryan The Explorer)) Yes. (Daniel Fountaine) getting um hardware and supplies and stuff like

1:46:24

(Daniel Fountaine) that. Like that would include that would have included uh (Daniel Fountaine) Tyveac labels for assets. So everything would have an asset

1:46:32

(Daniel Fountaine) tag and then it's a Tyvekac asset tag. So like it'll last for (Daniel Fountaine) a good long time. Like good luck messing that one up.

1:46:40

(Daniel Fountaine) Um and it came with uh - (Hopefully Abysmal (Elryan The Explorer)) Huh? (Daniel Fountaine) wristbands with ID QR code generating software to go

1:46:48

(Daniel Fountaine) with volunteers like spontaneous volunteers. Um, so (Daniel Fountaine) I mean it had a way to manage regular volunteers, staff,

1:46:56

(Daniel Fountaine) which would be anybody who's like in the leadership position, and then (Daniel Fountaine) also spontaneous volunteers. So they walk up, sign up, or you could

1:47:04

(Daniel Fountaine) scan or swipe their driver's license, and it'll import their data, and then (Daniel Fountaine) you print them a wristband right there. So that includes that printer that prints those - (Hopefully Abysmal (Elryan The Explorer)) Oh,

1:47:12

(Daniel Fountaine) wristbands. Um, and then it would also do like (Daniel Fountaine) regular ID badges for - (Hopefully Abysmal (Elryan The Explorer)) nice.

1:47:20

(Daniel Fountaine) your regular volunteers and your regular staff. And it came with (Daniel Fountaine) a a back-end system to validate uh active

1:47:28

(Daniel Fountaine) users. So, if somebody showed up with an ID badge and (Daniel Fountaine) oh god, about snap that thing. uh an ID

1:47:36

(Daniel Fountaine) badge, you could scan the the QR code on the back of it (Daniel Fountaine) and it would show their active or inactive status. Uh and it would also

1:47:44

(Daniel Fountaine) show like more up-to-date credentials. So, if somebody (Daniel Fountaine) um didn't have like an EMT license when they got their

1:47:52

(Daniel Fountaine) badge, which would normally be denoted on the front of the badge, (Daniel Fountaine) um you could scan that QR code and validate, oh yeah, you are

1:48:00

(Daniel Fountaine) active and I see you you're now a licensed EMT. Cool. Uh (Daniel Fountaine) so it would do like credential verification and stuff - (Hopefully Abysmal (Elryan The Explorer)) Yep.

1:48:08

(Daniel Fountaine) like that. And a lot of agencies in Texas, whether (Daniel Fountaine) that's local and state level, they use a similar system that's

1:48:16

(Daniel Fountaine) compatible uh or they use salamander. So (Daniel Fountaine) there's a way to there's a little bit of interoperability there. So you could say so and so

1:48:24

(Daniel Fountaine) is working with this agency and then it would show like what task forces (Daniel Fountaine) or task groups that were from that agency and then you could mark that they're - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:48:32

(Daniel Fountaine) working with that agency on that task group. Um and (Daniel Fountaine) it it's a really good platform. Like I love it. If I had the opportunity to buy it, I

1:48:40

(Daniel Fountaine) would probably buy it. And it also includes like the the badge making (Daniel Fountaine) machine that would make like these. Um this one I can't show you a whole lot

1:48:48

(Daniel Fountaine) of it, but this is a a state ID for disaster response. (Daniel Fountaine) Um, and this is like a - (Hopefully Abysmal (Elryan The Explorer)) Like it's got chip reader and stuff too. That's

1:48:56

(Daniel Fountaine) real what? Oh, yeah. So, that this is - (Hopefully Abysmal (Elryan The Explorer)) cool. It's got like the chip or (Daniel Fountaine) a that's a a smart chip, so you can use it to access - (Hopefully Abysmal (Elryan The Explorer)) tap.

1:49:04

(Daniel Fountaine) computers that require it. It also has RFID in it. - (Hopefully Abysmal (Elryan The Explorer)) Yeah. All (Daniel Fountaine) And it has uh I believe this one still has the magstripe. They might have got rid of the

1:49:12

(Daniel Fountaine) magstripe because that's kind of old. Uh yeah, they did get rid of the magstripe. - (Hopefully Abysmal (Elryan The Explorer)) right. (Daniel Fountaine) Uh but this would work in like a stateisssued computer. I could put

1:49:20

(Daniel Fountaine) this in and put in my PIN code and log into a stateisssued computer. (Daniel Fountaine) Um, it it makes those same kinds of badges that

1:49:28

(Daniel Fountaine) look very similar. There is uh obviously some key differences (Daniel Fountaine) between a a local and NGO and a government or a like - (Hopefully Abysmal (Elryan The Explorer)) Cool.

1:49:36

(Daniel Fountaine) state or federal government. Um, but it's a (Daniel Fountaine) very similar badging system. So, it's very familiar looking.

1:49:44

(Daniel Fountaine) when you show up to respond to something, you can show, you know, the (Daniel Fountaine) official, the local EMA, like you are who you say you are. Here's my

1:49:52

(Daniel Fountaine) ID. And it's, like I said, right on par with (Daniel Fountaine) what a lot of county, local, and

1:50:00

(Daniel Fountaine) state agencies in Texas use. And (Daniel Fountaine) a lot of other states, like all of Oklahoma is on there. Uh something like - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:50:08

(Daniel Fountaine) uh 86% of Texas is on that (Daniel Fountaine) platform. Um, all of Missouri is on there now

1:50:16

(Daniel Fountaine) and some of Louisiana is on that. It's probably like (Daniel Fountaine) 45 46% something like that. Um, so and

1:50:24

(Daniel Fountaine) there are or other states. It's like the whole state. I just memorized the ones that were (Daniel Fountaine) local to me because I was trying to to get C and Navy to pay for it for us

1:50:32

(Daniel Fountaine) to use that for asset management and stuff like that, but they were like, "No, we got Air (Hopefully Abysmal (Elryan The Explorer)) Yeah,

1:50:40

(Daniel Fountaine) Table." I I I swear if I ever (Daniel Fountaine) meet the person who said that we needed Air Table in - (Hopefully Abysmal (Elryan The Explorer)) bro.

1:50:48

(Daniel Fountaine) person, it's on site. Like I'm I'm fighting that guy. Uh because that was just (Daniel Fountaine) dumb. Um and the board didn't even

1:50:56

(Daniel Fountaine) like want to listen to me. I I went (Daniel Fountaine) and I'm not going to say I filed a complaint, but I I filed a request for a board meeting

1:51:04

(Daniel Fountaine) on that topic to talk to the board about this. And I was like, "Look, (Daniel Fountaine) here's why Air Table is bad." like Air Table does a lot of cool stuff and it looks really

1:51:12

(Daniel Fountaine) cool and it's really good if you're like a small NGO uh you (Daniel Fountaine) know because you can customize it and build it to what you need and and it works great for that. Uh but

1:51:20

(Daniel Fountaine) we're a little bit outside of that scale and uh Air (Daniel Fountaine) Table also has like an issue with

1:51:28

(Daniel Fountaine) failing. Uh your your database gets so big that it starts crashing (Daniel Fountaine) out. Uh there's I mean you could - (Hopefully Abysmal (Elryan The Explorer)) Oh

1:51:36

(Daniel Fountaine) Google it issues with Air Table or something like that. There's a a car rental company that was (Daniel Fountaine) using Air Table for a lot of their stuff and it actually just

1:51:44

(Daniel Fountaine) like completely started deleting records as they were adding more (Daniel Fountaine) data. Um I have I - (Hopefully Abysmal (Elryan The Explorer)) s***. Two.

1:51:52

(Daniel Fountaine) don't remember if it's that same article but there's another article that was talking about like they (Daniel Fountaine) were submitting forms like so it's an air

1:52:00

(Daniel Fountaine) table form. They were submitting forms and only a (Daniel Fountaine) portion of the data would be imported. So you would have incomplete

1:52:08

(Daniel Fountaine) data and you wouldn't have enough data to make like a functional ticket out of (Daniel Fountaine) it and it started doing it

1:52:16

(Daniel Fountaine) um at at a at a scale that (Daniel Fountaine) as you know cage navy relief we were already at in our other - (Hopefully Abysmal (Elryan The Explorer)) Oh.

1:52:24

(Daniel Fountaine) platform. So in noggin we already had that many (Daniel Fountaine) records. So we couldn't even like directly import it

1:52:32

(Daniel Fountaine) into air table. Everything had to be like recustomized and reconfigured and stuff like that. (Daniel Fountaine) Like right off the bat, we had issues with - (Hopefully Abysmal (Elryan The Explorer)) If they knew of the if they knew of the issue, then

1:52:40

(Hopefully Abysmal (Elryan The Explorer)) at that point they'd just be like, "Okay, s***. Maybe we shouldn't go to (Daniel Fountaine) it. They - (Hopefully Abysmal (Elryan The Explorer)) this." I don't

1:52:48

(Daniel Fountaine) they didn't want to listen to me. They didn't want to hear - (Hopefully Abysmal (Elryan The Explorer)) know. (Daniel Fountaine) me. They're like, "We we've kind of already made the decision. We're going to go with Air

1:52:56

(Daniel Fountaine) Table." Like, um, all right. I don't want (Daniel Fountaine) to I I think uh on that meeting I I made a statement some

1:53:04

(Daniel Fountaine) something along the lines of if if you as (Daniel Fountaine) if we as an organization choose to move forward with air

1:53:12

(Daniel Fountaine) table I as the IT director will (Daniel Fountaine) only and you know representative of the rest of the department we will

1:53:20

(Daniel Fountaine) only support basic login and logout functions. I'm not going to go (Daniel Fountaine) into building air table. I'm not going to go into all the other

1:53:28

(Daniel Fountaine) integrations and plugins and um you (Daniel Fountaine) whatnot. Like I'm not I'm not going into all that. Like here, I'll

1:53:36

(Daniel Fountaine) reset a password. All right, that's what I'll do. And (Daniel Fountaine) they were like, "Well, if that's what you choose to do, that's what you choose to do." And I was like, "I mean, you you

1:53:44

(Daniel Fountaine) going to fire me? You going to take away my paycheck or something? Like, (Daniel Fountaine) I'm a volunteer. Like, you can't." - (Hopefully Abysmal (Elryan The Explorer)) Yep. All

1:53:52

(Daniel Fountaine) Anyway, it was uh it was dumb. Uh, I - (Hopefully Abysmal (Elryan The Explorer)) right. (Daniel Fountaine) have a strong distaste for Air - (Hopefully Abysmal (Elryan The Explorer)) I'm with you

1:54:00

(Hopefully Abysmal (Elryan The Explorer)) there. We're we're working to get past it. Um I do got a jet. I have (Hopefully Abysmal (Elryan The Explorer)) not eaten dinner yet and I'm quite hungry. Uh but it

1:54:08

(Hopefully Abysmal (Elryan The Explorer)) was really good chatting with you. Um and I'm I'm going to (Hopefully Abysmal (Elryan The Explorer)) I'll send you the recording and then um like condensed

1:54:16

(Daniel Fountaine) Table. - (Hopefully Abysmal (Elryan The Explorer)) notes um and keep you posted on what we're building. (Daniel Fountaine) Yep. And again, if there's any way that I can help or or plug in and work on

1:54:24

(Daniel Fountaine) something, let me know. Or if we need to to talk ICS - (Hopefully Abysmal (Elryan The Explorer)) Sounds (Daniel Fountaine) forms or - (Hopefully Abysmal (Elryan The Explorer)) great. Hell yeah. No, I'm definitely going to go take those uh

1:54:32

(Daniel Fountaine) whatever, - (Hopefully Abysmal (Elryan The Explorer)) courses real quick. I say real quick, but (Daniel Fountaine) they're they're they're like two hours a course. Uh, and that's if you - (Hopefully Abysmal (Elryan The Explorer)) uh Okay.

1:54:40

(Daniel Fountaine) if you speed through it. If you speed through it, they're like two hours a course. - (Hopefully Abysmal (Elryan The Explorer)) Horrible. (Daniel Fountaine) Um, but like I said, it's it's a good base - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Okay.

1:54:48

(Daniel Fountaine) of knowledge to to grab and have an understanding of of (Daniel Fountaine) what everybody else in that disaster response

1:54:56

(Daniel Fountaine) is looking at and what they're talking about. And (Daniel Fountaine) a lot of other stuff will start to click, too, because you'll hear you'll hear stuff and you'll be like, I

1:55:04

(Daniel Fountaine) know what that is. - (Hopefully Abysmal (Elryan The Explorer)) Yeah. Yeah. We shall (Hopefully Abysmal (Elryan The Explorer)) see. I hope so because I do need to get all the lingo as

1:55:12

(Hopefully Abysmal (Elryan The Explorer)) well. I It's just like baptism by fire at this (Daniel Fountaine) Yeah, like I said, I' I've been at it for almost a decade now. So, like I'm I'm pretty - (Hopefully Abysmal (Elryan The Explorer)) point.

1:55:20

(Daniel Fountaine) familiar not only with a lot of different organizations, but a lot of different aspects of it. (Daniel Fountaine) Like I've worked everything from, you know, dispatch and onboarding

1:55:28

(Daniel Fountaine) to, you know, in the field operations. I've been the incident commander. I've been the the (Daniel Fountaine) guy in the field, you know, running the chainsaw. I've done I'm not going

1:55:36

(Daniel Fountaine) to say all of it, but probably all of it. Uh, I've done a lot of (Daniel Fountaine) it. So, if there's ever anything that

1:55:44

(Daniel Fountaine) you think like my perspective would be useful for, I'm (Daniel Fountaine) I'm happy to provide feedback. And like I said, I'm

1:55:52

(Daniel Fountaine) excited and willing to to help wherever I - (Hopefully Abysmal (Elryan The Explorer)) Hell (Hopefully Abysmal (Elryan The Explorer)) yeah. I appreciate it. Um I do definitely want to get

1:56:00

(Hopefully Abysmal (Elryan The Explorer)) the um SOS connect if you would be willing. Um and then I (Daniel Fountaine) can. - (Hopefully Abysmal (Elryan The Explorer)) definitely foresee us like reaching out to you for like testing on the um the

1:56:08

(Hopefully Abysmal (Elryan The Explorer)) very first point the is this going to be too distracting from the actual functionality. (Daniel Fountaine) Yeah. Yeah. Any of it. Any - (Hopefully Abysmal (Elryan The Explorer)) Right. But yeah, at the bare minimum.

1:56:16

(Daniel Fountaine) of it I'm I'm willing to help - (Hopefully Abysmal (Elryan The Explorer)) Hell yeah. Appreciate it. Um I can (Hopefully Abysmal (Elryan The Explorer)) send you a Discord invite if needed. Um I think

1:56:24

(Daniel Fountaine) with. - (Hopefully Abysmal (Elryan The Explorer)) we're going to be trying to do a lot of the development in the technology channel within 8 (Hopefully Abysmal (Elryan The Explorer)) arena. Um as much as we can. Um but

1:56:32

(Daniel Fountaine) Do y'all need or have a (Daniel Fountaine) separate channel for - (Hopefully Abysmal (Elryan The Explorer)) yeah um I think Donesy will be

1:56:40

(Hopefully Abysmal (Elryan The Explorer)) like he he offered that he'll make one for us if it comes to it. (Hopefully Abysmal (Elryan The Explorer)) Um, or are you like an admin in the Adrenina chat or

1:56:48

(Daniel Fountaine) it? Um, I was in the light version which they just - (Hopefully Abysmal (Elryan The Explorer)) something? (Daniel Fountaine) like turned off. Um, I don't know if I am in this - (Hopefully Abysmal (Elryan The Explorer)) Or Oh,

1:56:56

(Daniel Fountaine) one. Uh, let me see. (Daniel Fountaine) It does not look like I have admin access. Uh, so I'm not in this one, but - (Hopefully Abysmal (Elryan The Explorer)) no.

1:57:04

(Daniel Fountaine) I know quite a few people who are. Um, and like I - (Hopefully Abysmal (Elryan The Explorer)) Yeah. (Daniel Fountaine) said, I was in the other one, so I could probably get it over here as well. - (Hopefully Abysmal (Elryan The Explorer)) Yeah.

1:57:12

(Daniel Fountaine) Um, but if we need a channel, I mean, if you have (Daniel Fountaine) somebody that is already capable of doing it, cool. If you need help with

1:57:20

(Daniel Fountaine) that, let me know. Um, and - (Hopefully Abysmal (Elryan The Explorer)) We'll (Daniel Fountaine) uh

1:57:28

(Daniel Fountaine) you said something about a Discord. Are y'all currently working in Discord - (Hopefully Abysmal (Elryan The Explorer)) do. Yeah. (Hopefully Abysmal (Elryan The Explorer)) Yeah. Our our u Dan, the backend guy, the guy who built the

1:57:36

(Hopefully Abysmal (Elryan The Explorer)) first platform is just on Discord. I don't think he's got (Daniel Fountaine) or - (Hopefully Abysmal (Elryan The Explorer)) uh Slack, but Yeah. Um, and then they just got like an

1:57:44

(Daniel Fountaine) uh I was going to - (Hopefully Abysmal (Elryan The Explorer)) R4 Discord. I can just send you the invite real (Daniel Fountaine) say I could get you my Discord thing, but Discord decided it's time to do

1:57:52

(Daniel Fountaine) updates, so maybe not. - (Hopefully Abysmal (Elryan The Explorer)) quick. No, you're good. Uh, you (Hopefully Abysmal (Elryan The Explorer)) know where to reach me. I am quite famished. Um, I do got a jet, but yeah, I

1:58:00

(Daniel Fountaine) All righty. Oh, did you send it over - (Hopefully Abysmal (Elryan The Explorer)) appreciate it. (Daniel Fountaine) here? Yeah. Okay. I was going to say because this will disappear and - (Hopefully Abysmal (Elryan The Explorer)) Uh, yeah, I can send it over in Slack as

1:58:08

(Daniel Fountaine) I won't be able to see it - (Hopefully Abysmal (Elryan The Explorer)) well. Yeah, apologies. All (Daniel Fountaine) again later. - (Hopefully Abysmal (Elryan The Explorer)) right. Peace out.