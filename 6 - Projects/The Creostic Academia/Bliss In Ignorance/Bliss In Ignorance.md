---
Date: 2024-12-14 22:41
tags:
  - Business
Paths: 
Status: Processing
---
---
## Phrases 
To throw up on the main page like minecraft does :)

Bii the future (bee logo / bee emoji)

For the people who love free speech but ...
	want the choice of what to listen to
	love ignoring everyone more
		and love ignoring everything even more
	dont give a fuck (DGAF)
		dont care what uncle tommy believes in
		dont care about * insert very specific goofy anecdote *
		dont care about eveyone's favorite sports team
		dont care what everyone thinks
		dont need self help tips from people without their own life figured out
	dont want to be forcefed garbage
		hate that companies get free speech too
		forget that means everyone gets to speak their mind
		love the firehose of information a lot less
		aren't so fond of nonconsensual advertisements
			The sheer quantity of shitty advertisements disguised as conversation
		aren't a big fan of AI generated slop
	dont mind missing out on whatever the fuck (tf) is happening today
		dont mind hearing about it from a friend
		dont mind being late on the trend
		dont mind staying up to date on literally everything
		dont mind 

---

## Intro
See [[Corporation Blocker]] for main ideas and needs behind this concept.

Use [Advanced Profanity Filter](https://github.com/FrostCo/AdvancedProfanityFilter)  as backbone, curate lists of corporations to block

Basically add a subscription (as in following filter lists, not charging a subscription) service for filters
	on charging a subscription, not wanted but will if needed 
		or make marketplace for the filter lists and let people profit off of their use.
			can make it crypto or internal currencty to push people to add to the filter list
				amount of all possible crypto is the amount of websites out there?
					Scales infinitely thin
				amount of all possible crypto is the amount of websites left to block?
					Scales infinitely thin as well yes, but is combatted by the blocking erroneous sites. 
				Can combat scaling by making bots that go through the internet to clean it up
					(users would lose opportunity to make money off token if the bots do their job for them)
					Do this regardless of if taking crypto route
					host competitions for people to make bots to automate the process of blacklisting shit sites
						human interference checking the sites ofc, but scaling is the goal
							can also have whitelist, ability to request push to public list (democratic filter subscription)
						also if doing crypto do competitions along with letting the 


Democratic whitelist vs blacklist voting (upvote to bring attention to sites that need to be blacklisted / put on as by default disabled but enable-able)

Combo with dns services like [Control D](https://controld.com/blog/what-is-web-filtering/) as backup for protection from malicious websites

Combo with [uBlacklist](https://github.com/iorate/uBlacklist)

Combo with [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/)

---

## Fog of war / Machete Mechanic
Parse the user's search / search history (with consent ofc) to a model that auto-whitelists content they want to see (subscriptions in a sense)

Allows for this not to be used as censorship from a central command; rather a tool for self-censorship.

"This search has returned over % websites with blocked content, would you like to enable this content?"

i.e. if someone wants to look up a specific political candidate they can, doing so disables the politician blacklist and they can enable it themselves; can specifically whitelist specific politicians as well.


---

## Content Blacklist

### Sources
https://en.wikipedia.org/wiki/Lists_of_companies - convert to string/json list? whatever is needed

https://www.uspto.gov/trademarks/search - maybe can scrape something from here
	https://branddb.wipo.int/en/similarname?sort=score%20desc&start=0&rows=30&asStructure=%7B%22boolean%22:%22AND%22,%22bricks%22:%5B%5D%7D&_=1734238678005
		^ RANDOM ALTERNATIVE

Once word list is made, create crawler that reads site content and flags if it has banned content; show percentage on browser
	Hide websites based on percentage threshold
	Put this behind paywall so it can be self funded (crawlers cost money)

Let users make their own lists and share them for free (only brings more use to site)
	both websites and words

Put on github with changes to advanced profanity filter.

### **Block Lists**
#### **Organizations and Entities**
##### **Companies**: 
- ALL Large conglomerates (e.g., Amazon, Meta, ExxonMobil).
	- Fortune 500 and beyond
- **Ethical Consumption Filters**: Companies or products with poor environmental, labor, or ethical records.
- **Products**: Specific product lines or items (e.g., iPhones, Coca-Cola).
	- Product Boycotts or Bans (e.g., specific products from controversial companies).
- **Trademarked Phrases**: Branded slogans or taglines (e.g., "Just Do It," "I’m Lovin’ It").
- **Influencers/Personalities**: Public figures, celebrities, or internet personalities.
	- Public Figures (e.g., celebrities, internet personalities).
	- Controversial Figures (e.g., individuals embroiled in scandals).
	- Industry Leaders (e.g., tech innovators, philanthropists).
- **Media Sources**: News outlets, blogs, or sites known for biased reporting.
	- News Outlets (e.g., biased or sensationalist reporting sources).
	- Propaganda and Misinformation (e.g., state-sponsored or extremist media).
- **Scams/Spam**: Known fraudulent websites, phishing sites, or predatory services.
##### **Governments and Political Entities**
- Current and former world leaders (e.g., presidents, prime ministers, monarchs).
- Political candidates for elections (local, state, or international).
- Political parties and their associated platforms.
- Policies
- National Governments
##### **Religions**
- Major world religions (e.g., Christianity, Islam, Hinduism, Buddhism).
- Denominations or sects within religions (e.g., Sunni, Catholicism, Orthodox).
- Religious movements and leaders.
- Religious Doctrines
	- Common phrases / teachings
- Philosophical Movements (e.g., Stoicism, Nihilism).
#### **Content**
##### **Disasters**
- Natural disasters (e.g., earthquakes, hurricanes, wildfires).
- Man-made disasters (e.g., oil spills, nuclear accidents, industrial disasters).
- Historical events associated with disasters.
##### **Controversial Topics**
- Social Debates (e.g., abortion, gun control, LGBTQ+ rights, Immigration policies, climate change, Economic inequality, and Social justice debates).
- Cultural Norms and Sensitivities (e.g., practices seen as oppressive or exploitative).
- Historical and Revisionist Narratives (e.g., reinterpretation of colonization).
- Scientific/Technological Ethics (e.g., AI bias, biotech patents).
##### **Hater Talk**
- Hate speech (e.g., racist, sexist, homophobic content).
	- Group-Based Hatred (e.g., racism, xenophobia).
	- Cyberbullying and Harassment.
	- Radicalization Content (e.g., extremist recruitment material).
- Targeted harassment or cyberbullying.
- Groups or organizations promoting hate.
##### More
- **Explicit Content**: Adult or inappropriate websites based on user-defined preferences.

- **Regions or Languages**: Blocking sites originating from specific countries or in particular languages.
	- Subcategories: Language Preferences, Regional Filters, and Cultural Sensitivities.

- **Self-Help and Lifestyle Overload**
	- Overgeneralized Advice (e.g., "10 steps to happiness").
	- Unverified Wellness Tips (e.g., "miracle cures").
	- Subcategories:
		- Unwanted Financial Advice (e.g., get-rich-quick schemes).
		- healthcare
			- alternative medicine mlm's

- Specific topic of disinterest
	* Hobbies or Topics (e.g., certain video games, sports, hobbies).
	* 

- **Manipulative or Addictive Designs**
	- Dark UX Patterns (e.g., forced subscriptions).
	- Addictive Designs (e.g., excessive gamification).
	- FOMO Triggers (e.g., "limited-time offers").
		- price when not in shopping mode

- **Cross-Cutting Issues:** Many topics overlap (e.g., a corporation involved in a historical controversy, or a political entity embroiled in a disaster response). A tagging or matrix system could enable more nuanced filtering.





---

# GPT Reformatting:

## Introduction
Bii the Future aims to create an advanced, customizable internet filter system that empowers users to curate their web experiences. By building on the foundation of the [Advanced Profanity Filter](https://github.com/FrostCo/AdvancedProfanityFilter), the project will introduce a subscription model (not monetarily based unless necessary) for sharing and following filter lists. The initiative will also explore blockchain-based incentives, community-driven curation, and advanced automation to enhance scalability.

---

## Key Features

## Subscription-Based Filter Lists
1. **Filter Curation**:
   - Users can follow curated filter lists tailored to specific interests or goals (e.g., blocking corporations, political content, malicious websites).
   - Filters can be customized and combined for unique user needs.

2. **Filter List Marketplace**:
   - Optional marketplace allowing users to sell or trade filter lists.
   - Introduce internal currency or cryptocurrency incentives to encourage contributions.

3. **Crypto Integration** (Optional):
   - Tie the internal currency/token supply to the number of websites being blacklisted.
   - Rewards for contributors who identify and verify blacklist-worthy sites.
   - Challenges:
     - Scaling issues with infinite token thinning.
     - Mitigation through bot-based automation for blacklisting and whitelisting.

4. **Democratic Filtering**:
   - Users can vote on whitelist/blacklist entries to maintain a balanced, community-driven approach.
   - Options to upvote/downvote for democratic inclusion in default filter settings.

---

## Combining Forces

## Integration with Existing Tools
1. **DNS Services**:
   - Leverage services like [Control D](https://controld.com/blog/what-is-web-filtering/) for additional malicious website protection.

2. **Browser Extensions**:
   - Enhance functionality by integrating with tools like [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) and [uBlacklist](https://github.com/iorate/uBlacklist).

3. **Content Parsing and AI Models**:
   - Analyze user search history (with consent) to auto-adjust whitelists and filter preferences.
   - Provide prompts like: “This search returned X websites with blocked content. Would you like to enable this content?”

---

## Self-Censorship Tools

## Fog of War / Machete Mechanic
1. **Personalized Filters**:
   - Users can tailor filters to their preferences without central oversight.
   - Auto-whitelisting for content based on user subscriptions and interests.

2. **Adjustable Transparency**:
   - Enable or disable specific filters dynamically (e.g., viewing political content while maintaining broader blocks).
   - Allow granular control, such as enabling specific sites or topics temporarily.

---

## Content Blacklist Development

## Sources for Blacklist Data
1. **Existing Databases**:
   - [Lists of Companies](https://en.wikipedia.org/wiki/Lists_of_companies): Parse into JSON or relevant formats.
   - [USPTO Trademarks](https://www.uspto.gov/trademarks/search): Scrape or utilize trademark datasets.

2. **Crawler Automation**:
   - Build crawlers to scan website content for blacklisted keywords or patterns.
   - Assign a “blocked content percentage” to websites and hide based on user-defined thresholds.

## User Contributions
1. **Custom Lists**:
   - Users can create, share, and distribute custom filter lists freely.
   - Encourages community participation and enhances usability.

2. **Public GitHub Repository**:
   - Host project on GitHub to allow transparency and community contributions.
   - Provide tools for list creation, crawler configuration, and filter sharing.

---

## Scaling and Incentives

## Automation with Bots
1. **Scalable Filtering**:
   - Develop bots to crawl and classify websites for blacklist/whitelist inclusion.
   - Host competitions to encourage bot development and optimization.

2. **Human Verification**:
   - Retain manual review processes for ensuring bot accuracy.
   - Users can contest and vote on bot classifications.

## Gamification and Rewards
1. **Competitions**:
   - Reward developers for building efficient and accurate filtering bots.
   - Incentivize community engagement through leaderboard rankings and prizes.

2. **Tokenized Rewards**:
   - Award contributors with internal currency or cryptocurrency for verified site classifications.
   - Encourage participation while mitigating the risk of token devaluation.

---

## Conclusion
Bii the Future seeks to empower individuals with tools for internet self-censorship, free from central oversight or agendas. By combining advanced filtering technologies, democratic principles, and scalable automation, this project promises to redefine how we curate and control our digital experiences. Whether through community-driven lists, gamified incentives, or seamless integration with existing tools, Bii the Future aims to foster a safer, more personalized web for all.

