### Initial idea:

Having worked on enhancing engineering documentation accessibility with AI for my senior design project, I found a need for more advanced tools to analyze documentation; specifically in the medical device field (Biomedical Engineering). With the vast regulatory bodies and standards becoming incomprehensible to someone without decades of experience, the barrier to entry to the field stands as one of the highest among engineering colleges. To bridge this gap, I propose to utilize advanced machine learning tools to perform gap analysis in a way that teaches the user how to become (or stay) regulatory complaint. Aside from the beginner, this tool could be utilized even by seasoned employees; as regulations are often updated, ensuring that one's device stays up to regulation becomes a job in and of itself. The automation of this task ensures that medical device companies can stay up to date on the stringent requirements of these regulations, all the while bettering their product and consequentially their patient outcomes. With this automation we can progress past the occurrence of unnecessary regulatory violations, and hopefully make noncompliance a thing of the past.


### GPT Outline:

1. **Introduction: The Problem Statement**
    
    - Complexity of regulatory requirements in the medical device field.
    - High barriers to entry due to incomprehensibility of standards.
    - Need for continuous updates to maintain compliance.
2. **Proposed Solution**
    
    - Leverage advanced machine learning tools to:
        - Perform **gap analysis** on documentation.
        - Educate users on becoming or staying compliant.
    - Provide a tool that caters to:
        - Beginners entering the field.
        - Seasoned professionals navigating updates.
3. **Key Features of the Tool**
    
    - Intuitive interface for gap analysis.
    - Real-time updates for new or evolving regulations.
    - Interactive feedback to explain gaps and how to address them.
    - Scenario-based simulations to teach compliance strategies.
4. **Impact and Benefits**
    
    - **For Beginners**: Lowers barriers to entry, fostering new talent in biomedical engineering.
    - **For Professionals**: Reduces manual effort in compliance tracking.
    - **For Companies**: Improves regulatory adherence, reduces penalties, and enhances product quality.
    - **For Patients**: Ensures safer, higher-quality medical devices.
5. **Vision for the Future**
    
    - Automation minimizes human error in compliance processes.
    - Creation of a knowledge repository to guide continual improvements.
    - A goal to make noncompliance a relic of the past.

### GPT Expansion

In the medical device industry, staying compliant with the myriad of regulations from organizations like the FDA, ISO, and EU MDR is an ongoing challenge. These regulations are vital to ensure patient safety and device efficacy but are often labyrinthine in complexity, posing a formidable barrier to entry for newcomers. Even for experienced professionals, keeping up with the frequent updates and nuanced requirements is a time-intensive endeavor, prone to human error.

To address these challenges, I propose the development of an advanced machine learning-powered tool designed to assist in regulatory gap analysis. This tool would serve dual purposes: empowering beginners by breaking down complex standards into digestible insights and assisting seasoned professionals by automating compliance checks against the latest regulations.

The core functionality of the tool lies in its ability to perform document-based gap analysis. By analyzing engineering documentation against the required standards, it identifies discrepancies, offers actionable recommendations, and educates users on why and how to address these gaps. This interactive learning process ensures that even those new to the field can gain the foundational knowledge necessary to navigate compliance requirements confidently.

For professionals, the tool becomes an indispensable ally, tracking updates to regulations in real-time and seamlessly integrating these changes into ongoing projects. This reduces the burden of manually sifting through dense regulatory documents, freeing engineers to focus on innovation and improving patient outcomes.

Beyond individual users, the tool has the potential to revolutionize medical device companies' compliance strategies. By ensuring that products adhere to regulations proactively, organizations can avoid costly penalties, reduce time-to-market, and, most importantly, ensure their devices consistently meet the highest safety and quality standards.

The broader vision for this initiative is to automate regulatory compliance to such a degree that noncompliance becomes a thing of the past. By creating a smarter, more accessible pathway to understanding and adhering to regulations, we not only lower barriers but also elevate the overall standard of medical devices, benefiting companies, engineers, and patients alike.


### "Humanized" Version

In the medical device industry, maintaining compliance with the numerous regulations from organizations like the FDA, ISO, and EU MDR presents a continuous challenge. These regulations are crucial for ensuring patient safety and device effectiveness, yet their complexity can be overwhelming, especially for newcomers. Even seasoned professionals find it time-consuming to keep up with frequent updates and intricate requirements, which can lead to human error. To tackle these issues, I would like to propose the creation and utilization of a machine learning tool aimed at facilitating regulatory gap analysis. This tool would serve two main functions: helping beginners by simplifying complex standards into understandable insights and aiding experienced professionals by automating compliance checks against the latest regulations. The primary feature of the tool would be its capability to conduct document-based gap analysis. By examining engineering documentation against the required standards, its goal would be to pinpoint discrepancies, provide actionable recommendations, and educate users on the reasons and methods for addressing these gaps (mitigating the risk of AI hallucination via the train of thought methodology in addition to allowing the user to still intervene). This interactive learning approach ensures that even those new to the field can acquire the essential knowledge needed to navigate compliance requirements with confidence. For professionals, the tool becomes a vital resource, monitoring regulatory updates in real-time and seamlessly incorporating these changes into ongoing projects. This alleviates the burden of manually reviewing dense regulatory documents, allowing engineers to concentrate on innovation and enhancing patient outcomes. Moreover, the tool has the potential to transform the compliance strategies of medical device companies. By ensuring that products meet regulations proactively, organizations can avoid costly penalties, shorten time-to-market, and, most importantly, guarantee that their devices consistently uphold the highest safety and quality standards. The broader vision for this initiative is to automate regulatory compliance to such a degree that noncompliance becomes a thing of the past. By creating a smarter, more accessible pathway to understanding and adhering to regulations, we not only lower barriers but also elevate the overall standard of medical devices, benefiting companies, engineers, and patients alike.

### Next Steps

While I do have experience in this, I would need to purchase applicable standards for testing (get permission to utilize the standards already purchased by the department and go from there), create the model itself (perhaps in a webapp with a document databasing tool like paperless.ngx), and flush out server backend and user interfacing for a usable speed.

#### Phase 1: Research and Feasibility Study

1. **Accessing Standards**
    
    - Secure access to regulatory standards:
        - Obtain permission from your department to use already purchased standards.
        - Identify additional standards to purchase if gaps exist.
    - Prioritize key standards (e.g., FDA CFR, ISO 13485, EU MDR) for initial testing.
2. **Define Scope and Use Cases**
    
    - Focus initial efforts on a manageable subset of regulatory requirements.
    - Define primary use cases: gap analysis for new devices, updates for existing devices, or compliance training for users.
3. **Competitor Analysis**
    
    - Identify existing tools in the market and assess gaps in their capabilities.
    - Highlight features your innovation will uniquely address.

#### Phase 2: Prototype Development

1. **Model Creation**
    
    - Select machine learning techniques tailored to text-heavy, regulation-based analysis:
        - Use **Natural Language Processing (NLP)** for regulatory text parsing and comparison.
        - Explore **knowledge graphs** to model relationships between requirements and device documentation.
2. **Build the Database Framework**
    
    - Integrate a document management system (like **Paperless-ngx**) to store, retrieve, and version control standards and user documents.
    - Implement metadata tagging to enhance searchability and relevance ranking.
3. **Develop Initial Backend**
    
    - Build a Django-based server for:
        - Uploading and processing documentation.
        - Running gap analysis against stored standards.
    - Ensure the backend handles regulatory updates dynamically.
4. **Basic User Interface**
    
    - Create a web app prototype with Angular for initial testing.
    - Focus on intuitive file upload, progress tracking, and gap analysis visualization.

#### Phase 3: Validation and Testing

1. **Testing on Real Documentation**
    
    - Use anonymized or department-approved documents to validate the model's accuracy and effectiveness.
    - Benchmark speed and scalability on varying document sizes.
2. **Iterate on Feedback**
    
    - Collect feedback from users (e.g., peers, professionals) on interface and performance.
    - Address pain points and refine model outputs.
3. **Performance Optimization**
    
    - Enhance backend efficiency for faster gap analysis and document indexing.
    - Optimize web app performance for responsiveness.

#### Phase 4: Advanced Features and Deployment

1. **Add Advanced Capabilities**
    
    - Implement real-time updates for new or modified standards.
    - Create guided learning modules for new users, such as tutorials and compliance simulations.
2. **Security and Privacy Enhancements**
    
    - Integrate robust data encryption and access controls.
    - Ensure compliance with data protection regulations like GDPR or HIPAA.
3. **Pilot Testing**
    
    - Launch the tool for departmental use or with a small group of beta users.
    - Collect usage metrics to assess the tool's real-world utility.

### Milestones:

1. **Short Term (0–3 months)**
    - Secure access to standards and define project scope.
    - Set up document database with regulatory texts and user-uploaded files.
    - Develop a functional prototype for gap analysis with basic NLP capabilities.
2. **Medium Term (4–6 months)**
    - Optimize backend and database for speed and scalability.
    - Test and refine the tool with real-world documents and user feedback.
    - Expand NLP capabilities to cover edge cases and complex regulations.
3. **Long Term (6+ months)**
    - Deploy the tool for broader use (e.g., university, industry partnerships).
    - Add advanced features like real-time updates and training simulations.
    - Explore commercialization opportunities or publish findings on the tool's development.

### Purchases
As stated I would need to purchase any relevant standards for testing if I cannot obtain permission to use the standards already purchased (specifically the ISO and ASTM standards for medical device development). Once an MVP is made and I am on to testing I would likely utilize a Kubernates instance on AWS for testing as I do not have my own server. Additionally I would want to dedicate more of my time to this so any help is much appreciated.

#### Standards: 
FDA - Free (will likely be what I start with)

PMC Research Paper Database - Also free but less relevant, can use if need to fine-tune models to medical terminology

ASTM Standard Library - $703.00
[ASTM Volume 13.01: Medical And Surgical Materials And Devices (I): E667–F2503](https://www.astm.org/astm-bos-13.01.html)  
[ASTM Volume 13.02: Medical And Surgical Materials And Devices (II): F2504–Latest; Emergency Medical Services; Search And Rescue](https://www.astm.org/astm-bos-13.02.html)

ISO # 13485:2016 - 173 EUR -> ~$200

#### Server Costs
AWS K8 Instance - $0.10 per hour for each Amazon EKS cluster (excluding $0.50 per hour for support as I might forgo it for cost reasons and lack of security requirements) -> $300 monthly? Depends on usage

#### Time
Ideally I could quit (or at least decrease hours at) my part time job to pursue this, making ~$1000 per month but can live on less as needed. I am aware that the initial amount would not be enough to do that, but by getting things up and running I can look into strategic partnerships / other methods of funding myself.