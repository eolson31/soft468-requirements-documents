# Goals

The system is structured around the following primary goals:

- **G1:** Enable Hearing Test Administration  
- **G2:** Manage Users & Access  
- **G3:** Store & Manage Data  
- **G4:** Generate Audiograms  
- **G5:** Provide Reporting & Analytics  
- **G6:** Deploy & Maintain System  
- **G7:** Calibration & Setup  


## Functional Requirements

### FR1 – Hearing Test Initialization (G1)
The system shall allow an approved tester to start a new hearing test session.

**Fit Criteria:**
- Tester clicks “Start Test” -> a new test session is created.
- System initializes left and right ear testing sequence.
- Test session is uniquely identified and stored.

### FR2 – Multi-Frequency Tone Generation (G1)
The system shall generate tones at specified frequencies.

**Fit Criteria:**
- When a test runs -> tones at 500, 1000, 2000, 4000, and 8000 Hz are played.
- Each frequency is presented at least once per ear.
- Tone playback occurs without system error.

### FR3 – Bilateral Ear Testing (G1)
The system shall test both ears independently.

**Fit Criteria:**
- System presents tones separately for left and right ears.
- User responses are recorded per ear.
- Data clearly distinguishes left vs right ear results.

### FR4 – User Response Capture (G1)
The system shall allow participants to indicate whether a tone is heard.

**Fit Criteria:**
- User selects “Heard” or “Not Heard” -> response is recorded.
- System associates response with correct frequency and ear.
- Each tone presentation results in a recorded response.

### FR5 – Threshold Recording (G1, G3)
The system shall record hearing thresholds for each ear-frequency combination.

**Fit Criteria:**
- After test completion -> threshold values exist for all tested frequencies.
- Each threshold is stored with corresponding ear and session.
- Stored data matches user responses exactly.

### FR6 – User Registration and Authentication (G2)
The system shall allow users to register, authenticate, and access the system based on roles.

**Fit Criteria:**
- A user submits a registration form with a valid email -> a registration request is stored.
- An administrator approves a request -> the user is able to log in successfully.
- An unapproved user attempts login -> access is denied.
- A logged-in user accesses a protected page -> access is granted only if authenticated.

### FR7 – Admin Approval Workflow (G2)
The system shall allow administrators to manage tester accounts.

**Fit Criteria:**
- Admin selects a pending user -> system marks user as approved or denied.
- Approved user logs in -> access to testing features is enabled.
- Denied user attempts login -> access is denied.
- System records approval/denial decisions.

### FR8 – Data Storage (G3)
The system shall store all test-related data.

**Fit Criteria:**
- After test completion -> test data is written to the database.
- Stored data includes participant, tester, thresholds, referrals, and timestamps.
- Retrieving stored data returns identical values to what was recorded.


### FR9 – Offline Data Handling (G3)
The system shall support offline data collection and later synchronization.

**Fit Criteria:**
- When offline -> test data is stored locally.
- When connection is restored -> local data is uploaded to server.
- No stored test data is lost during sync.

### FR10 – Audiogram Generation (G4)
The system shall generate a visual audiogram after test completion.

**Fit Criteria:**
- Test completes -> audiogram is displayed on screen.
- Audiogram contains plotted values for all five frequencies.
- Left and right ear data are visually distinguishable.

### FR11 – Reporting and Statistics (G5)
The system shall provide aggregated test statistics.

**Fit Criteria:**
- User requests report -> system displays total tests, pass/fail counts, referrals.
- Displayed statistics match stored data values.
- Reports update when new data is added.

### FR12 – Data Querying (G5)
The system shall allow users to query stored data.

**Fit Criteria:**
- User submits query -> system returns matching dataset.
- Returned dataset corresponds to query parameters.
- No unauthorized data is returned.

### FR13 – System Deployment (G6)
The system shall be accessible via web browsers.

**Fit Criteria:**
- User accesses system via browser -> application loads successfully.
- System is reachable via deployed domain.
- Core features function on supported devices.

### FR14 – Cross-Device Compatibility (G6)
The system shall operate on mobile and tablet devices.

**Fit Criteria:**
- User accesses system on mobile/tablet -> UI renders correctly.
- User completes full test workflow on device without failure.

### FR15 – Calibration and Setup (G7)
The system shall provide calibration functionality before testing.

**Fit Criteria:**
- User initiates calibration -> calibration tone is played.
- User adjusts volume -> system proceeds only after confirmation.
- Calibration step completes before test begins.

### FR16 – Setup Guidance (G7)
The system shall provide instructions for proper test setup.

**Fit Criteria:**
- Before testing -> instructions are displayed.
- User acknowledges instructions -> test proceeds.
- Instructions include headphone usage and environment guidance.


## Quality Requirements

### QR1 – Usability
The system shall be usable by non-experts.

**Fit Criteria:**
- ≥ 90% of users complete a test without assistance.
- First-time users complete test in under 10 minutes.

### QR2 – Security & Privacy
The system shall protect sensitive data.

**Fit Criteria:**
- 100% of data transmissions use HTTPS encryption.
- Unauthorized data access occurs in < 0.0001% of cases.

### QR3 – Reliability
The system shall reliably store and preserve data.

**Fit Criteria:**
- ≥ 99.9% of test sessions are stored without data loss.
- System recovers data after interruption in ≥ 99% of cases.

### QR4 – Performance Efficiency
The system shall respond quickly.

**Fit Criteria:**
- Audiogram appears within 2 seconds after test completion.
- UI interactions respond within 1 second.

### QR5 – Functional Accuracy
The system shall correctly perform hearing test operations.

**Fit Criteria:**
- 100% of recorded thresholds match user input.
- All five frequencies are tested for both ears in every session.

### QR6 – Data Accessibility
The system shall provide timely access to data.

**Fit Criteria:**
- Queries return results within 2 seconds.
- ≥ 95% of queries return correct data.

### QR7 – Compatibility
The system shall function across environments.

**Fit Criteria:**
- ≥ 95% of tested devices successfully run the system.
- No critical errors occur on supported browsers.


## Domain Assumptions

- CHWs have access to a compatible device (smartphone or tablet).
- CHWs have access to functional headphones.
- Users can follow on-screen instructions.
- Internet access is available at least intermittently.
- CHWs have valid email accounts.
- Participants can respond to audio prompts.
- Testing environments are reasonably quiet.
- CHWs will complete follow-up data entry when required.


## Goal Refinement
Here is the full goal refinement graph:
![Goal Refinement Graph](./images/fullGoalGraph.png)

Due to how large it is, it's barely readable. So I've split it into the individual goals for easier access. We will start with the Main Tree, showing Goal 0.

Goal 0 Tree:
![Goal 0](./images/mainTree.png)

Goal 1 Tree:
![Goal 1](./images/goal1.png)

Goal 2 Tree:
![Goal 2](./images/goal2.png)

Goal 3 Tree:
![Goal 3](./images/goal3.png)

Goal 4 Tree:
![Goal 4](./images/goal4.png)

Goal 5 Tree:
![Goal 5](./images/goal5.png)

Goal 6 Tree:
![Goal 6](./images/goal6.png)

Goal 7 Tree:
![Goal 7](./images/goal7.png)

## Sequence Diagrams

Sequence diagram showing the process of administering a hearing screening/test:
![Sequence Diagram 1](./images/sequenceDiagram1.png)

Sequence diagram showing the process of entering patient follow up information
![Sequence Diagram 2](./images/sequenceDiagram2.png)

Sequence diagram showing the process of saving patient data collected offline
![Sequence Diagram 3](./images/sequenceDiagram3.png)


---

| [⬅️](users.md) | [⬆️](README.md) | [➡️](glossary.md) |
|:---------------:|:----------------------------:|:--------------------------------------------:|
| [Interviews & Users](users.md) | [Front Matter](README.md) | [Glossary](glossary.md) |

