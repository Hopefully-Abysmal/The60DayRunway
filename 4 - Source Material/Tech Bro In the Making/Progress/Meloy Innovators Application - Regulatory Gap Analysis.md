## Initial idea:
In the medical device industry, maintaining compliance with the numerous regulations from organizations like the FDA, ISO, and EU MDR presents a continuous challenge. These regulations are crucial for ensuring patient safety and device effectiveness, yet their complexity can be overwhelming, especially for newcomers. Even seasoned professionals find it time-consuming to keep up with frequent updates and intricate requirements, which can lead to human error. 
To tackle these issues, I would like to propose the creation and utilization of a machine learning tool aimed at facilitating regulatory gap analysis. This tool would serve two main functions: helping beginners by simplifying complex standards into understandable insights and aiding experienced professionals by automating compliance checks against the latest regulations. The primary feature of the tool would be its capability to conduct document-based gap analysis. By examining engineering documentation against the required standards, its goal would be to pinpoint discrepancies, provide actionable recommendations, and educate users on the reasons and methods for addressing these gaps (mitigating the risk of AI hallucination via the train of thought methodology in addition to allowing the user to still intervene). 
This interactive learning approach ensures that even those new to the field can acquire the essential knowledge needed to navigate compliance requirements with confidence. For professionals, the tool becomes a vital resource, monitoring regulatory updates in real-time and seamlessly incorporating these changes into ongoing projects. This alleviates the burden of manually reviewing dense regulatory documents, allowing engineers to concentrate on innovation and enhancing patient outcomes. Moreover, the tool has the potential to transform the compliance strategies of medical device companies. 
By ensuring that products meet regulations proactively, organizations can avoid costly penalties, shorten time-to-market, and, most importantly, guarantee that their devices consistently uphold the highest safety and quality standards. The broader vision for this initiative is to automate regulatory compliance to such a degree that noncompliance becomes a thing of the past. By creating a smarter, more accessible pathway to understanding and adhering to regulations, we not only lower barriers but also elevate the overall standard of medical devices, benefiting companies, engineers, and patients alike.

## Next Steps

While I do have experience in similar endeavors through my senior design project (under NDA though this would not interfere), I would need to purchase applicable standards for testing (get permission to utilize the standards already purchased by the department and go from there), create the model itself (perhaps in a webapp with a document databasing tool like [paperless.ngx](https://github.com/paperless-ngx/paperless-ngx/) ), and flush out server backend and user interfacing for a usable speed.
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

## Purchases
As stated I would need to purchase any relevant standards for testing if I cannot obtain permission to use the standards already purchased (specifically the ISO and ASTM standards for medical device development). Once an MVP is made and I am on to testing I would likely utilize a Kubernates instance on AWS for testing as I do not have my own server. (https://github.com/paperless-ngx/paperless-ngx/discussions/3797) Additionally I would want to dedicate more of my time to this so any help is much appreciated.

#### Standards: 
FDA - Free (will likely be what I start with)
https://www.fda.gov/regulatory-information/search-fda-guidance-documents
^ no direct download is available, need to figure out some sort of scraper (if legal to do so)

PMC Research Paper Database - Also free but less relevant, can use if need to fine-tune models to medical terminology
https://pmc.ncbi.nlm.nih.gov/tools/openftlist/

ASTM Standard Library - $703.00
[ASTM Volume 13.01: Medical And Surgical Materials And Devices (I): E667–F2503](https://www.astm.org/astm-bos-13.01.html)  
[ASTM Volume 13.02: Medical And Surgical Materials And Devices (II): F2504–Latest; Emergency Medical Services; Search And Rescue](https://www.astm.org/astm-bos-13.02.html)

ISO # 13485:2016 - 173 EUR -> ~$200
https://www.iso.org/standard/59752.html

#### Server Costs
AWS K8 Instance - $0.10 per hour for each Amazon EKS cluster (excluding $0.50 per hour for support as I might forgo it for cost reasons and lack of security requirements) -> $300 monthly? Depends on usage
https://aws.amazon.com/eks/pricing/

#### Time
Ideally I could quit (or at least decrease hours at) my part time job to pursue this, making ~$1000 per month but can live on less as needed. I am aware that the initial amount would not be enough to do that, but by getting things up and running I can look into strategic partnerships / other methods of funding myself.

