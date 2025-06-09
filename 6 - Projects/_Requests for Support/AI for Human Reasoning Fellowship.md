# Questions:

- 1) What is something you’ve created or helped create that you’re particularly proud of? (guide: 50-200 words)
	- One project I’m proud of is JARVIS, a document intelligence and retrieval system I co-developed to support engineering teams at a major medical device company (NDA) for my Senior Capstone at Texas A&M University. Built on top of the open-source Paperless-ngx system, JARVIS addressed the bottlenecks in document access across regulatory, R&D, and quality workflows. My team integrated semantic search, OCR, and vector-based question-answering to allow engineers to instantly surface critical information (even from handwritten or poorly indexed documents). JARVIS wasn’t just a backend improvement; it was a practical example of what human-centered AI can look like in enterprise contexts. It helped reframe how technical professionals interacted with information: not just by keyword, but by intent and relevance. The project sharpened my systems thinking and deepened my belief that tools should serve comprehension, not just efficiency. That belief carries forward into my current work: building interfaces that augment reasoning, not replace it.
- 2) What do you think are the most crucial challenges in the AI for Human Reasoning space? Why? (guide: 50-200 words)
	- I think the biggest challenge is value opacity both within systems and users. We’re surrounded by LLMs that appear helpful, but often reinforce unexamined assumptions, generate sycophantic responses, or lack internal consistency. The problem isn’t just “hallucination,” but epistemic murkiness: we can’t easily tell what assumptions went into a model’s response, which framework it implicitly used, or how much weight it gave competing values. This opacity affects human decision-making too. People often apply conflicting frameworks (deontology in principle, utilitarianism in exception for example) without realizing it. What’s missing is tooling that helps people see the frameworks they're using, how they align with others, and where contradictions arise. My fellowship proposal is rooted in this challenge: simulating decisions across frameworks to clarify tradeoffs, detect collapse (via falsifiability), and ultimately foster reflective pluralism. We need systems that don't merely assist decision-making, but help humans understand why they decide the way they do and when those reasons need refinement.
- 3) What might you be interested in working on during this fellowship? (guide: 50-200 words)
	- I’d like to prototype an ethical simulation engine that helps people explore moral decisions through multiple philosophical frameworks in parallel. It would allow users to input a scenario (personal, political, hypothetical) and simulate how different moral systems (e.g., utilitarianism, deontology, care ethics) would evaluate it, including likely outcomes and underlying principles. The tool would function as a decision-making co-pilot and sanity-checker. It could flag when a proposed decision violates universalizability constraints (a la Kant), generates disproportionate harm (utilitarian), contradicts endorsed values over time (virtue ethics), and more. I’d also like to experiment with a module for epistemic virtue benchmarking: scoring AI explanations on clarity, source citation, and humility; key traits that foster trust and coherence in complex reasoning environments. My aim is not to encode “correct” morality, but to offer a pluralist interface to help users reflect on their values, see their blind spots, and refine their reasoning with clarity. Think of it as WolframAlpha meets Socrates: less about answers, more about better questions and better mirrors.


- 4) Who (or where) did you hear about this from?
	- Joel Chan (MetaGov Slack)
- 5) Start Date: The fellowship is designed to begin on July 14th, 2025. If you anticipate any challenges with starting on this date, please indicate your earliest possible start date.
	- Yes, can start on July 14th
- 6) Where will you be based for the duration of the fellowship? (please note we cannot sponsor visas)
	- Undecided, likely Colorado if remote but am open to relocation
- 7) Are you applying with any collaborators? If so, please list them
	- N/A but would love to join a team if any fall in line with my desired work

# **Proposal for FLF Fellowship: Ethical Simulation Engines for Human Reasoning Augmentation**

**Applicant:** Landon Dahle (aka Elryan The Explorer)

---

### **Project Title**

**"Plurality Machines: Ethical Simulation Engines for Navigating Moral Complexity"**

---

### **Summary**

We propose a modular AI system that simulates moral decisions across multiple philosophical frameworks in parallel, analyzes convergence/divergence patterns in outcomes, and constructs a meta-index for ethical fit and falsifiability. This "Plurality Machine" is not intended to dictate right answers but to surface moral tradeoffs and edge cases—making pluralistic reasoning visible and navigable.

This toolset will serve as:

- A **decision-making co-pilot**
    
- A **reflective scaffolding agent** for personal and collective ethics
    
- A **teaching instrument** for moral philosophy and emotional logic
    
- A **testing ground** for stress-testing universalizability claims à la Kant, while simulating outcomes à la Mill
    

At its core: simulation replaces prescription. Ethics becomes cartography.

---

### **Why This Matters Now**

Humanity faces decision-making overload. Framework lock-in (e.g., strict utilitarianism) can lead to inhumane outcomes, but pure relativism leads to inaction. Meanwhile, LLMs now _can_ simulate and explain diverse philosophical positions—if we give them structured ways to test and compare those models across contexts.

By building a tool that **tests moral systems, not just within themselves but against each other**, we move closer to:

- Navigating disagreement with clarity
    
- Creating AI that respects human plurality
    
- Avoiding value-collapse or ethical monoculture
    

---

### **Core Features and Innovations**

#### 🧠 1. **Moral Decision Engine**

- Simulates actions across ethical frameworks (utilitarianism, deontology, virtue ethics, care ethics, etc.)
    
- Outputs expected outcomes, principles invoked, and virtue trajectories
    
- Embeds explanatory LLMs for digestible narrative summaries
    

#### 🧪 2. **Thought Experiment Library**

- Encodes canonical thought experiments as callable logic functions
    
- Tags by moral stressor type, agent count, time pressure, etc.
    
- Used to stress-test user scenarios and moral logic paths
    

#### 🧭 3. **Framework Falsifiability Layer**

- Inspired by Popper: actions or systems that collapse under universalization are filtered
    
- Prevents framework abuse or self-defeating logic
    

#### 📊 4. **Decision Matrix Builder**

- Index of action-context-framework-consequence matches
    
- Users can explore how decisions land across moral domains
    
- Potential for real-time ranking of fit based on personal or institutional goals
    

#### ❤️ 5. **Emotional Logic Integration**

- Optional modules using BCI/emotion inference (e.g. journaling, physiological data)
    
- Maps emotional states into decision history and growth tracking
    
- Anchors ethics in lived human experience
    

---

### **Example Use Cases**

- A **policy designer** compares refugee law proposals across frameworks
    
- A **philosophy student** explores what happens if everyone lied to get out of fines
    
- A **therapist** uses it with clients to explore the logic behind internal moral conflicts
    
- An **LLM auditor** stress-tests AI outputs for ethical contradiction or collapse
    

---

### **Why Me**

- Background in **biomedical engineering, entrepreneurship, governance, and philosophy**, aimed at innovating in academic and philosophical systems
    
- Obsessive about epistemology, pluralism, simulation logic, and system dynamics
    
- Conversant in philosophical traditions, neuro-emotional modeling, and code-level prototyping
    

I'm primed to build thought tools that scaffold meaning—not dictate it.

---

### **Roadmap (Fellowship Timeline)**

**Week 1–2**: Design spec, ontology for frameworks, base actions, and prototype architecture  
**Week 3–4**: Build simulation engine and logic path renderer  
**Week 5–6**: Integrate framework mapping layer + early falsifiability filter  
**Week 7–9**: Build index from historical scenarios and thought experiments  
**Week 10–11**: UX layer, explainability, and feedback scaffolding  
**Week 12**: Demo moral sandbox tool + project roadmap for next stage

---

### **Beyond the Fellowship**

- **Moral Sandbox Platform**: make the simulation accessible to educators, ethicists, policy makers
    
- **Constitutional AI Tooling**: audit AI models for pluralist ethical coherence
    
- **Philosophy Engine Plugin**: integrate with GPT agents for live moral reasoning checks
    

---

### **Closing**

This is not about telling people how to be good.  
This is about giving them a compass that shows the different meanings of "good"—and the tradeoffs each demands.

A mirror, a map, a moral instrument panel.

Let’s build it.