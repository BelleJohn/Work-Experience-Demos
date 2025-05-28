## 📌  Master Thesis: Development and Testing of a Virtual Environment for the Study of Kinesthetic Feedback Restoration

### 📚 Description
This research aims to evaluate the potential of using vibration-induced proprioceptive/vibrotactile feedback in upper limb prosthetics through a non-invasive, closed-loop system. By integrating a virtual robotic hand with EMG input and sensory feedback, the study explores how such feedback can enhance user interaction during daily grasping tasks—laying the groundwork for future improvements and potential real-world applications for amputees. 

### 🛠 Methodology
This study includes two experiments: the **Mapping Experiment** and the **Proprioception Experiment**.

1. Mapping Experiment – Personalized Feedback Mapping
- Goal: Customize proprioceptive/vibrotactile feedback for each user by identifying matching sensory illusions.
- Components:
  - Vibrotactile feedback system including stimulus controller (Raspberry Pi)
  - Evaluation interface (C#) for recording perceived vibration effects
- Procedure:
  - Vibrators are placed based on palpation
  - Subjects report sensations/illusions during stimulation (e.g., perceived movement)
  - Data logged on perceived motion (elicited time, location, direction, vividness, naturalness, speed, etc.)

2. Proprioception Experiment – Grasping Task Evaluation
- Goal: Evaluate the usability and effectiveness of a non-invasive, closed-loop vibrotactile feedback system for prosthetic hand control, tested in a virtual environment with healthy subjects to simulate hand preshaping and assess its potential to convey meaningful information to amputees.
- Setup:
  - Virtual robotic hand using MuJoCo HAPTIX
  - Control via non-invasive EMG signals or keyboard
  - Four vibrotactile cues mapped to: pronation, supination, hand opening, hand closing
- Test Conditions:
  
  | Condition | Control Type | Feedback     | Visual Feedback           |
  | --------- | ------------ | ------------ | ------------------------- |
  | KWO       | Keyboard     | None         | No                        |
  | EWO       | EMG          | None         | No                        |
  | EW        | EMG          | Vibrotactile | No                        |
  | VKWO      | Keyboard     | None         | Yes *(Control condition)* |

- Procedure:
  - Subjects operate a virtual hand in different grasping scenarios
  - Feedback is provided or withheld depending on the condition
  - Hand visibility toggled to simulate sensory reliance
- Data Collected:
  - Joint/motor positions, task duration, grasp timing, Success scores per trial
  - Synchronized video and sensor recordings for post-hoc analysis

### 📊 Results & Findings
🧪 Participants
- 3 healthy adults (ages 26–31) with no prior experience
- Each completed tasks under all four conditions: VKWO, KWO, EWO, and EW

🎯 Key Findings
- Vibrotactile Feedback (EW Condition):
  - Participants performed significantly better with EMG + vibration (EW) compared to EMG-only (EWO)
  - Vibrotactile cues effectively conveyed movement direction, aiding in task execution

🌀 Cylinder Grasping Task Observations
- Easiest: Small cylinders
- Most difficult: Large cylinders and those at 45° or 135° orientations
- 135° orientation led to frequent grasping failures

⚠️ Operational Limitations
- Complex virtual button design introduced errors in task timing
  - Accounted for 9%–26% of total trial time

🔧 System Limitations
- EMG classifier error rates were high:
  - Ranged from 41.4% to 62.25%, affecting control reliability
- Vibration delays and serial port issues occasionally disrupted EW condition

🌐 Virtual Environment Challenges
- Fixed camera view and lack of depth cues caused:
  - Misalignment between palm and thumb
  - Increased grasping failures due to limited spatial perception

### 🔧 Technologies & Tools Used
- **Programming Languages:** C++/C, C#, Matlab.
- **Libraries & Frameworks:** MuJoCo.
- **Development Tools:** Linux, Windows, Raspberry Pi.

### 📂 Dataset & Resources
- Data source(s): None
- Relevant papers or references:
  - [A somatotopic bidirectional hand prosthesis with transcutaneous electrical nerve stimulation based sensory feedback](https://www.nature.com/articles/s41598-017-11306-w)
  - News to check: [A worldwide research overview of Artificial Proprioception in prosthetics](https://pubmed.ncbi.nlm.nih.gov/40261833/)

### 🚀 Future Work or what if I can start over?

🔧 System and Experimental Design Improvements:

- Simplify the Virtual Button <br/>
  The current button used for time logging is overly complex and affects accuracy. Replacing it with a simpler UI or a physical button could reduce training time and improve logging precision.
- Switch to MuJoCo Pro <br/>
  Unlike MuJoCo HAPTIX, MuJoCo Pro supports keyboard function customization and programmatic .xml loading—making experiments easier to run and improving video review quality.
- Refine EMG–Vibrator Integration <br/>
  Improve the EMG classifier to work more harmoniously with vibrators placed on the same hand, minimizing misclassification.
- Adapt for Amputee Use <br/>
  Redesign the system for amputees by:
  - Adjusting EMG electrode and vibrator placement
  - Exploring motion capture systems to better simulate real-world prosthetic use
- Enhance Mouse Control  <br/>
  The current mouse-based control of the virtual hand is unintuitive. Consider alternatives like joystick input or gesture-based control for better usability.
- Improve the Virtual Environment  <br/>
  Issues like fixed viewpoints and poor depth cues cause frequent palm/thumb misalignment. Improvements may include:
  - Adjustable viewpoints (without overwhelming users)
  - Visual aids like additional depth cues or reference spheres
- Optimize EMG Classifier Training <br/>
  While training date/duration had little impact, electrode placement was critical. A standardized placement protocol per user is essential.
- Fix Vibrator Delay & Serial Port Bugs <br/>
  Address hardware/software issues causing:
  - Vibration delays
  - Serial port disconnections, especially in the EW condition
- Increase Trial Counts <br/>
  More training and test trials are necessary to:
  - Improve classifier accuracy
  - Allow users to develop better control strategies
- Add New Experimental Conditions <br/>
  Introduce additional testing conditions to isolate variables and better understand feedback contributions:
  - KW – Keyboard + vibrotactile feedback
  - VEWO – EMG + Visual feedback, no vibrotactile feedback
- Enhance Data Analysis <br/>
  Explore more nuanced performance metrics, such as time-weighted scoring, to better evaluate system responsiveness and user adaptation.

🤖 System Integration and Application:
- Adapt the Full System for Amputees: <br/>
  Refine and apply the system in real-life settings with amputee users, or move toward commercialization.
- Build a Robust, Reliable Setup: <br/>
  Ensure the system is stable, user-friendly, and suitable for repeated use in both lab and clinical settings.
- Integrate Multimodal Feedback: <br/>
  Combine vibrotactile feedback with other sensory modalities to replicate a more lifelike, biological hand experience.
- Reduce Abandonment Rates: <br/>
  Ultimately, the goal is to build a prosthetic feedback system that improves usability and comfort—increasing adoption and enhancing the quality of life for prosthetic users.


