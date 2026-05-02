# Background

Hearing loss impacts people of all ages, but only a fraction are diagnosed and treated. Of the 30 million adults in the U.S. who have hearing loss, only ~15% use hearing assistive devices. Furthermore, 2-3 per 1000 babies are born with hearing loss each year. It can be difficult for some individuals to receive a hearing screening and many are "lost to follow-up". 

Community Health Workers (CHWs) are trusted community-based individuals who provide basic healthcare assistance, health education, advocacy, and connections to appropriate resources, and could therefore be a valuable resource to bridging the gap in untreated hearing loss, particularly in underserved regions. The goal of this project is to create an easy-to-administer, web-based hearing testing application that anyone can run from a smartphone or tablet, coupled to a pair of headphones. Additionally, this product should be accessible to those in rural areas who may not always have WiFi access. The test itself should be automated and not require specialized knowledge on the part of the user.

## Scope

The web-based hearing testing system should include:

1. **Ease of use**: The system should be administrable by anyone - no specialized training in audiology should be needed. The UI/UX should be user-friendly and easy to understand.
2. **Hearing test:** A hearing test, not just a screening, should be developed. The test should play multiple frequencies (500Hz, 1000Hz, 2000Hz, 4000Hz, 8000Hz) in both ears and be able to record whether a user hears the sound.
3. **Data schema:** Relevant data will need to be collected about the tester and participant (e.g., participant name, tester name, date of birth, address, test results, referrals made).
4. **Data storage:** Secure, easily queryable, cloud-based storage should be used.
5. **Data query & retrieval:** It should be possible to gather statistics about stored hearing tests (e.g., number of tests administered, number of passing screenings, number of referrals, number of referral follow ups).
6. **Plot the audiogram:** An audiogram should be drawn on the screen upon completion of a test.
7. **Public access:** The website should be publicly hosted on a dedicated website.


## Sponsors

1. **Bonita Sharif:** Associate Professor, Primary Sponsor
2. **Michelle Hughes:** Professor, Director of Cochlear Implant Research lab at UNL 
3. **Hanna Ditmars:** Associate Professor of Practice
4. **Kayle Byrd:** AuD Student
5. **Isabella Sanner:** AuD Student


## Stakeholders

### Core Stakeholders

1. **Development Team:** The Senior Design team who designs, implements, tests, and deploys the system.

2. **Course Instructors/Leads:** Instructors and leads evaluate the system against the UNL senior design academic requirements. Their expectations influence scope, documentation, and deliverable deadlines.

3. **Community Health Workers (CHWs):** These users are responsible for administering hearing tests to patients using the application. They interact directly with the system to log in, perform tests, record results, and search for test results. The system must be easy to use for CHWs, which makes them a primary driver of usability requirements.

4. **Test Participants:** These users are the individuals whose hearing is being tested. While they do not interact with the system on their own, they respond to audio prompts and their information is collected during testing. Their experience directly influences safety, clarity of instructions, and tone accuracy requirements.

### Supporting Stakeholders

1. **System Administrators:** Administrators create and manage CHW accounts, as well as manage test data. They are responsible for maintaining system integrity and overseeing data access, making them key stakeholders for security, authentication, and reporting requirements.

2. **Research & Lab Staff:** Other researchers and lab staff may use the test data to evaluate trends, referral outcomes, and the overall feasibility of the testing approach. Their needs influence data schema design, data search, and reporting capabilities.

### External Stakeholders

1. **Healthcare Providers & Clinics:** Users are recommended to these stakeholders by the app. They do not interact with the system, but ensuring that users have accurate test results affects their ability to provide appropriate follow-up care.

2. **Regulatory Bodies:** These groups ensure ethical and legal compliance in handling sensitive patient data. Their influence drives requirements related to HIPAA compliance, data security, and privacy controls.

3. **Technology Providers:** These providers supply the infrastructure for hosting, data storage, and secure data management. While not interacting with app, they influence architectural decisions and influence reliability and availability requirements.
