---
Date Created: 2025-06-03 14:32
Last Updated: 2025-06-03 14:32
tags:
  - Resource
Index: 
Topic: 
Link:
  - https://youtu.be/VkmZCC55giA?si=laCwz1lVUV46UY_J
Status: Unweathered
Published: true
---
---
# Summary:


# Key Terms:
* 

# Reflection:

## Misc. Notes
- I enjoy the manifest links
- driver license number for verification of identity
- lots of steps to get someone ready to make a delivery
- dropoff location notification +++
- Airtable mainly kanban view; shows cards for each delivery to be made.
	- Grid view for showing profiles of the drivers
- Chronological Workflow as is:
	- Supply site registers
		- Set ID info
			- site address
			- site contact info
				- set site managers
			- site hours and recieving
				- max supply load size
				- receiving notes / instructions
			- site status
				- accepting from the public?
				- distributing supplies to the public?
				- site type: Distribution Center vs Supply Warehouse
				- publically visable?
				- Site active?
		- Supply site inputs what they have oversupplied and what they need
			- based on set taxonomy of items
			- search (seems not to be fuzzysearch...)  
				- tag based filters
			- toggle item and set item status (urgently needed, needed, available, and oversupply)
			- can also add new items
		- sets site status to accepting donations
		- sets whitelist of users that can log in via their phone numbers
	- Driver registers
		- jotform
		- Info (address, license plate, availability, comments)
		- driver portal -> can change the above and also deactivate profile
		- Once up, browse routes is enabled
			- This is where I think the logic really shines through; batch process routes and build out this side of things to potentially allow for further ease of volunteering (the driver likely would want to be able to put in a current address and desired address, filter such that only by set threshold of de-routing show what routes would be along the way for them to pick up small items perhaps?)
				- Additionally show this graphically, highlight main route and alternative routes with addon times (could potentially use google API for this or find FOSS alternative)
		- Alternatively (not shown in video), [volunteer form: delivery](https://wnc-supply-sites.com/volunteer/delivery) 
			- pick site you are coming from? or perhaps going to?, input contact info, select items (idk if this is items you are donating from your site to the other site or taking from the site to another; believe it is actually just items you are donating and "your site" refers to the site you are donating to? if the case then change the form to a donation form...)
		- TLDR: driver accepts a route at undisclosed date?
	- Dispatch of site connected to the route (starting location not destination) has to approve this delivery and set a date to have the driver pick up the items
		- In Airtable:
			- Kanban view "create/track delivery"
				- shows categories: uncategorized, driver volunteered, creating dispatch, 
				- under driver volunteered:
					- dispatcher approves the delivery, sets date, and adds notes as needed. This sends confirmation?
			- Grid view of the drivers
				- shows name, current location (ideally), vehicle type, phone number, and availability
			- Needs matching (grid view)
				- shows Site name, county/state/city, quantity of items needed, autodirect button to route browser with their location, autodirect button for needs matcher for that site, 
		- Back on WNC-supply-sites (or socal but yeah)
		- 
## Curiosities
- 
## Ideas
- 
## Questions
- Add all eligable items logic on server side or airtable?

# GPT Refinement: 

# Transcript Analysis
Here are **key timestamps** from the walkthrough of the current site (R4 D2) that highlight **functionality worth maintaining or evolving** for **R4Dash** (disaster logistics) and **R4Go** (civic gamification):

---

### 🟢 **Core Public-Facing Features (keep & polish)**

- **0:05 – 0:46**  
    **Public search UI** with:
    
    - Filter by county, item category, supply status (Urgent / Needed / Available / Oversupply)
        
    - Filter by site type (Distribution vs. Warehouse)
        
    - 🔄 _Maintain for R4Dash; Extend filters for R4Go roles & quests_
        
- **0:51 – 1:30**  
    **Grid view** of supply sites with status indicators
    
    - Quick-glance format for matching needs to surplus
        
    - 🔄 _Use this interface for R4Dash; could become map/quest view in R4Go_
        
- **1:37 – 2:25**  
    **"Contact Us" & login flow** for new supply sites
    
    - Whitelist via phone number, then set password
        
    - 🔄 _Keep low-friction onboarding; add badge invite for R4Go_
        

---

### 🟡 **Site Manager Portal (priority for usability & trust layering)**

- **2:30 – 4:49**  
    **Site inventory management**
    
    - Search/filter/add items by category
        
    - Mark items as "Needed" or "Available"
        
    - 🔄 _Keep for R4Dash; track item history or gamify accuracy in R4Go_
        
- **4:54 – 6:12**  
    **Site info + manager delegation**
    
    - Add secondary data entry roles
        
    - Max load capacity prevents truck mismatches
        
    - Site visibility & active/inactive toggle
        
    - 🔄 _Maintain; extend with trust tiers or performance badges in R4Go_
        

---

### 🚐 **Driver Portal + Dispatch Flow (mission-critical, improve UX)**

- **6:26 – 7:22**  
    **Driver sign-up form + availability editor**
    
    - Volunteer onboarding + deactivate flow
        
    - 🔄 _Streamline with badge unlocks or SMS onboarding for R4Go_
        
- **7:22 – 8:04**  
    **Auto-generated delivery route matching**
    
    - Based on site needs + distance
        
    - 🔄 _Maintain this for R4Dash; for R4Go, repurpose as “quest routing”_
        
- **8:04 – 9:00**  
    **Dispatcher view**
    
    - Accept or reject volunteer drivers, set pickup time
        
    - Grid of drivers with location, vehicle, availability
        
    - 🔄 _Keep core; enable dispatcher badges & heatmap overview in R4Go_
        
- **9:00 – 13:00**  
    **Delivery creation + confirmation process**
    
    - Auto-filled manifests, driver assignment, text confirmations
        
    - Site-specific manifests with address, contacts, license plate checks
        
    - 🔄 _Keep intact; R4Go can add completion streaks, delivery reputation, optional photo uploads_
        
- **13:00 – 15:10**  
    **Driver-side live progress**
    
    - Button flow: start → en route → arrived pickup → leaving pickup → arrived dropoff → complete
        
    - Triggers real-time SMS to stakeholders
        
    - 🔄 _Excellent for R4Dash; R4Go might add celebratory moments, driver trust score, real-time quest chain_
        

---

### 🔧 **Back-End Improvements to Prioritize**

- Needs Matching UI (timestamp: **8:42 – 9:00**)
    
- Dispatcher tools (timestamp: **8:04 – 9:00**, **13:00 – 15:10**)
    
- Whitelisting & access control (timestamp: **1:54 – 2:22**)
    
- Item taxonomy unification (timestamp: **3:15 – 4:20**) — some inconsistency in labels/search logic
    

---

### Suggested Categories for MVP Upgrades

|Area|Keep|Improve|Gamify (R4Go)|
|---|---|---|---|
|Public search UI|✅|Filter UX, responsiveness|“Needs Explorer” badge|
|Site manager portal|✅|UI, item entry|Trust tier, collaborative data logs|
|Driver signup & routing|✅|Streamlined SMS/Self-serve|Driver tiers, medals|
|Dispatcher flow|✅|Simplify routing logic UI|“Master Coordinator” path|
|Confirmations & SMS|✅|Logs/alerts dashboard|Confirmation streaks|
|Visibility toggles|✅|Simplify per-role access|Unlockable zone visibility|

Let me know if you want a visual version or a GitHub issue batch for each area!


# Transcript:

0:03

all right I'm going to start with the

0:05

front end of R4 D2 that is publicly

0:08

available so this is what is visible to

0:11

people who are the public and not logged

0:14

in so you've got SoCal Supply sites and

0:18

you can go to search sites and

0:21

supplies now this will have um actual

0:26

information in it once we

0:28

launch and you're able to filter and see

0:31

donation sites and by the county and the

0:35

items and you're able to mark and only

0:38

see urgently needed needed available or

0:40

over Supply um and filter accepting

0:43

donations or not accepting donations and

0:46

the type of site it is so Distribution

0:48

Center or Supply

0:49

Warehouse when you scroll down a little

0:51

bit you get a grid view of the sites so

0:57

um like this one is a test and this and

1:00

they're not showing anything as a needed

1:02

Supply but they're showing an over over

1:04

supply of over thec counter meds down

1:07

here you've got another test um location

1:12

because we don't have live data in here

1:14

yet of um urgently needed over the

1:18

counter meds so

1:20

[Music]

1:21

um when you look at these things it's

1:24

easy to tell um In This Very condensed

1:27

version of what is available and what is

1:30

needed so you can match

1:33

them so that's for the public then

1:37

you're also able to contact us through

1:41

here and then it's just um asking for

1:44

information giving some feedback Supply

1:47

sites that want to join are able to

1:49

contact us there because they don't have

1:51

a login you can hit login for Supply

1:54

sites we do our logins by phone numbers

1:58

so all of the sites that that are that

2:00

you're currently working with and are

2:03

sorry all of the supply sites that

2:05

you're currently working with and you

2:08

want to go ahead and what we call

2:12

whitelist them um you can give us their

2:14

phone numbers we can go ahead and plug

2:16

that in on the back end and then all

2:18

they'll have to do is hit this account

2:20

set setup button right here and it will

2:22

let them um assign a password to

2:25

themselves so once they log in they will

2:29

be able

2:30

to see more sites that would have

2:33

otherwise been not visible to the public

2:36

if they click there they also will be

2:40

able to go into the manager

2:42

portal and when you are a site manager

2:47

you are only able to see the one site

2:49

that you are able to that you were

2:53

assigned so here I am like in the Dove

2:57

side so I'm able to see them all and in

3:00

California we only have the test sites

3:02

cuz we haven't launched yet but I would

3:05

be able to go in and manage the selected

3:09

site

3:11

and you can manage site

3:15

inventory and we have tons and tons of

3:18

items in here because we actually went

3:20

ahead and gave La access to everything

3:23

that Western North Carolina has utilized

3:26

um but they're able to be filtered so

3:29

you can go in here and let's say we are

3:32

looking

3:34

for sanitation and we're looking for

3:37

cleaning supplies so let's say I want to

3:39

mark that as

3:41

needed um the Al and you can filter here

3:44

so your site is your thing is a lot

3:48

shorter your list the other thing you

3:51

can do is type it so let's say I need

3:53

trash

3:55

bags and I'm able to go through and

4:00

should be able to search for trash

4:04

bags um maybe that's not in there maybe

4:08

their garbage

4:12

bags

4:14

H let's see

4:18

here trash bags there they are I had a

4:20

filter

4:21

on so I can mark that as

4:25

available and um if there what you were

4:29

looking for is not in there you can add

4:31

a new item um on the same note if I want

4:34

to go back here and manage my

4:36

inventory I can look at the things that

4:39

I have and take uncheck that and then

4:43

that would take it off of my list

4:49

completely so I'm also able to manage

4:54

my um information for my site the site

4:58

name street address

5:00

all of these

5:02

details and then the contact information

5:05

this is really important because I'm

5:08

able to add a site manager so if your

5:10

site manager um that is over everything

5:14

is actually super busy and doesn't have

5:16

time to do this you can add like a data

5:17

entry person to manage

5:20

it um we do hours in receiving

5:23

instructions this Max Supply load is

5:25

super important it protect prevents

5:27

people from sending transfer trucks of

5:30

goods when all you can handle is a

5:32

pickup

5:33

truck and then site status so on the

5:36

site status you can note whether you're

5:38

accepting supplies from the public

5:40

whether you're Distributing supplies to

5:42

the public your distribution site type

5:45

if you're a warehouse or a distribution

5:47

center um basically being are you taking

5:50

in a lot of excess and then sending to

5:52

the the supply sites or are you

5:56

Distributing to the public and holding

5:58

smaller quantities of goods and then

6:01

down here at the bottom you're able to

6:03

determine if you're publicly visible on

6:04

SoCal Supply sites and if your site is

6:07

active so if you were getting ready to

6:09

shut down or if you're ready to shut

6:10

down you would select no and then it

6:12

would take you off of the um

6:15

availability for dispatches and

6:22

stuff so when we go back um we have a

6:26

driver portal so there's a job form

6:28

where people can sign up as drivers

6:30

and they automatically get put in here

6:32

as a driver into the portal and they can

6:35

use this to update their information for

6:37

their availability and any comments they

6:40

may have um as well as go inactive if

6:43

they no longer want to be a driver or

6:45

receive information about

6:49

driving um drivers have another special

6:52

Button as long as they're logged in

6:55

they're able

6:57

to um look at

7:00

routes that are predetermined there's

7:02

nobody in the background setting this up

7:04

it is all um done based on available and

7:09

needed and it creates matches and then

7:12

drivers are able to come in here and

7:14

volunteer and it tells them how far

7:17

apart they are and how long

7:19

approximately the drive should

7:22

be so once they volunteer it will notify

7:26

the dispatchers

7:31

all right so I'm going to leave this

7:33

logged in and I'm going to take you to

7:35

the back end so in the

7:38

dispatchers um if a driver volunteers

7:41

they will show up right here in the

7:42

driver volunteered section and a

7:45

dispatcher would have the ability to

7:48

look over everything

7:50

here and they'll be able to say yes or

7:54

no that that's good and put a time in

7:57

here or a date and then they can make

7:59

any notes that they would like to make

8:02

and then they can send the confirmation

8:04

to approve it and we'll talk about

8:06

confirmations in just a

8:10

minute so over here you have a grid view

8:15

of the drivers so you're able to see

8:17

right now we just have one driver and

8:19

it's somebody that we have that's

8:20

running tests um our Dove guy um and you

8:24

can see what type of vehicle they're

8:26

driving you can get a location um they

8:28

should be putting a location for where

8:30

they're at and then what their

8:31

availability is so the grid view is

8:34

super helpful when you have multiple

8:35

drivers

8:36

available um the other thing that's

8:40

important is the needs

8:42

matching so all the sites will show up

8:45

here and you can see how many items they

8:47

need and where they're located and then

8:50

you're able to hit needs matching and it

8:54

will take you back to SoCal Supply sites

8:56

as long as you're logged in it will

8:58

automatically pop populate the needs

9:00

matching down here and it says that this

9:03

site which is one of our test sites

9:05

needs air mattresses and cleaning

9:07

supplies and that it has trash bags

9:10

available so there is another test site

9:13

that's set up with an air mattress

9:15

available and it's 7.8 mil away or 22

9:20

minutes so for the sake of this

9:22

demonstration I am going to set up that

9:27

um that dispatch

9:30

so zus CA warehouse and it is going to

9:35

zus

9:36

ca so to set up a delivery I'm going to

9:40

go to create I'm going to hit the plus

9:43

sign up

9:44

here and we're going to say that I want

9:46

this to happen

9:49

tomorrow and I want the Z

9:53

test

9:57

Warehouse CA

10:00

okay and I wanted to go

10:04

to zest Warehouse I think I remembered

10:07

that right we'll see in a minute I'm

10:09

going to assign the

10:11

driver which was

10:14

Alex and we are working on cleaning some

10:17

of this up still launch is not planned

10:20

for another several hours so we've still

10:22

got some filtering to do so bear with

10:25

us um and then the dispatcher is me

10:28

Jesse

10:31

so then I can close this

10:34

out double click it and you get a

10:37

different view

10:40

here um when you scroll down I'm

10:43

actually going to change this driver to

10:45

be myself that way I get the text

10:48

messages um so that's just

10:53

for um not pestering people that are on

10:56

my team because it's pretty late here

10:59

and you've got the what would be the

11:02

address the phone number and all the

11:04

details of the supply sites drop off and

11:06

pickup and the driver this would

11:09

normally be a license plate right here

11:11

but of course we're not giving our

11:13

personal license plates out as the

11:15

testers um because we're not actually

11:17

driving to

11:18

locations and then phone number of the

11:21

dispatcher and then it creates a public

11:23

manifest now if I've done this right

11:25

I'll be able to hit the add all all

11:27

eligible items button

11:30

and it will populate

11:33

them we'll see how good my memory is

11:37

because not a very good

11:40

memory so I'm going to guess that I've

11:43

probably got them backwards

11:48

here I think these are mine and they

11:51

have something available to do that with

11:54

and they have my number so I'm going to

11:56

swap that out real quick and see if that

11:58

works

12:07

we have multiple people doing testing

12:09

here so our needs and our halves are

12:11

kind of all over the place right now on

12:13

our tests there it is so we got adile

12:15

eligible items and the adult over the

12:17

counter meds popped in so that's the

12:20

want and the need or the need and the

12:22

have that are already there I can click

12:26

the send confirmation button and and it

12:29

is going to give me the option to click

12:31

to confirm after I check all of this

12:34

information um you'll notice I changed

12:36

all that so that my phone number is in

12:38

there and then you get the items and you

12:40

get the map down here at the bottom so

12:43

when I click the confirm button it will

12:45

actually send a text message um to the

12:50

pickup site the drop off site the driver

12:52

and the dispatcher to confirm the

12:55

route so when you come back over here

13:00

I'm going to close that out and we are

13:04

in the confirming

13:07

process and it just populated down

13:12

here and so now that I've sent that

13:14

confirm confirmation link you can see

13:18

everyone got their own link right here

13:21

and it's a link to a

13:24

manifest so they have the option to

13:26

confirm or cancel so this one we're

13:29

going to click confirm for the drop off

13:32

site I'm going to go back to the pickup

13:35

site I'm going to click confirm for the

13:38

pickup site and as you can see they can

13:39

see all of the same information everyone

13:42

can and they have the license plate

13:44

number in here too to be able to confirm

13:46

that the person showing up saying there

13:48

with R4 D2 is the person or is driving

13:52

the car that INF fact

13:54

matches so then the driver is able to

13:56

confirm as well so once the driver

14:00

confirms he's going to have or they're

14:02

going to have the same manifest here but

14:05

then they get a new Option so when they

14:07

are ready to leave and go to the pickup

14:11

site they'll be able to open this and

14:14

hit start delivery that will trigger a

14:16

text message to the pickup site that

14:18

says a driver is on the way that way

14:21

they know that they need to have this

14:23

ready once they've arrived at pickup it

14:27

closes that piece out and it shows that

14:29

the pickup is that the delivery is in

14:30

progress and when they hit leaving

14:33

pickup it will actually trigger a text

14:36

message to the dropoff location with an

14:39

ETA that gives the drop off location a

14:41

chance to contact the driver if they're

14:43

closing or if something may be wrong so

14:47

when they when they hit arrive at the

14:49

drop off then it actually shows us the

14:51

delivery

14:52

completed and this delivery will show

14:56

all the way over here in the delivery

14:59

very completed

15:01

portion so here is the one that we were

15:04

just working on and it shows that it's

15:06

arrived it drop off and it's

15:11

complete so I believe that is a pretty

15:14

good overview of what our software does

15:16

thank you very much I'm Jesse with R4

15:19

and I'm representing R4 D2