## 📌  Master Thesis: Development and Testing of a Virtual Environment for the Study of Kinesthetic Feedback Restoration

### 📚 Description
This research aims to evaluate the potential of using vibration-induced proprioceptive feedback in upper limb prosthetics through a non-invasive, closed-loop system. By integrating a virtual robotic hand with EMG input and sensory feedback, the study explores how such feedback can enhance user interaction during daily grasping tasks—laying the groundwork for future improvements and potential real-world applications for amputees. 

### 🛠 Methodology
This study includes two experiments: the Mapping Experiment and the Proprioception Experiment.

1. Mapping Experiment – Personalized Feedback Mapping
- Goal: Customize proprioceptive feedback for each user by identifying matching sensory illusions.
- Components:
  - Vibration feedback system
  - Evaluation interface (C#)
  - Stimulus controller (Raspberry Pi)
  - Custom arm map showing vibration location and perceived movement
- Procedure:
  - Vibrators placed based on palpation
  - Users report illusion during stimulation
  - Data logged on perceived motion (direction, vividness, naturalness, speed, etc.)

2. Proprioception Experiment – Grasping Task Evaluation
- Goal: Assess the usability and effectiveness of vibration feedback in prosthetic hand control, particularly in simulating hand preshaping.
- Setup:
  - Virtual robotic hand using MuJoCo HAPTIX
  - Control via non-invasive EMG signals
  - Sensory feedback via four vibrators (pronation, supination, opening, closing)
- Test Conditions:
  - KWO: Keyboard, no feedback
  - EWO: EMG, no feedback
  - EW: EMG with feedback
  - VKWO: Visual + Keyboard (control condition for validation)
- Procedure:
  - Subjects operate a virtual hand in different grasping scenarios
  - Feedback provided or withheld depending on the condition
  - Hand visibility toggled to simulate sensory reliance
- Data Collected:
  - Motor position, task duration, grasp timing, success score
  - Video and sensor data for analysis

### 📊 Results & Findings
- Participants: 3 healthy adults (ages 26–31) with no prior experience; tested under VKWO, KWO, EWO, and EW conditions.
- Vibrotactile Feedback: EW condition (EMG + vibration) significantly outperformed EWO (EMG only); vibration helped convey movement info.
- Cylinder Tasks:
  - Small cylinders were easiest; large cylinders were hardest.
  - 45° and 135° orientations were more challenging.
  - 135° caused grasping difficulties.
- Operational Limitations:
  - Virtual button was too complex, skewing time logging and prolonging trials (9%–26% of total time).
- System Limitations:
  - EMG classifier had high error rates (41.4%–62.25%).
  - Vibrator delays and serial port issues occurred during EW.
- Virtual Environment Issues:
  - Fixed view and poor depth cues led to palm/thumb misalignment and frequent grasp failures.

### 🔧 Technologies & Tools Used
- **Programming Languages:** C++/C, C#.
- **Libraries & Frameworks:** MuJoCo.
- **Development Tools:** Linux, Windows, Raspberry Pi.

### 📂 Dataset & Resources
- Data source(s): None
- Relevant papers or references:
  - [A somatotopic bidirectional hand prosthesis with transcutaneous electrical nerve stimulation based sensory feedback](https://www.nature.com/articles/s41598-017-11306-w)
  - News to check: [A worldwide research overview of Artificial Proprioception in prosthetics](https://pubmed.ncbi.nlm.nih.gov/40261833/)

### 🚀 Future Work or what if I can start over?

🔧 System and Experimental Design Improvements:

- Virtual button improvement: The current virtual button for time logging is too complex and affects accuracy. A simpler design or physical button is recommended to reduce training time and improve precision.
- Use of MuJoCo Pro: The MuJoCo HAPTIX API does not allow modification of keyboard functions, but MuJoCo Pro does. Switching to MuJoCo Pro can simplify experiments and allow programmatic loading of .xml files for better video review.
- EMG and vibrator integration: The EMG classifier needs refinement to work in harmony with vibrators placed on the same hand.
- Experimentation for amputees: Adjust placement of EMG electrodes and vibrators for amputees. Consider using a motion capture system to better simulate real-world prosthesis applications.
- Mouse control improvement: Develop alternatives or enhancements to simplify virtual hand control via mouse.
- Virtual environment improvement: Fixed viewpoints and poor depth cues cause misalignment issues with the palm and thumb. Possible improvements include adjustable viewpoints (without increasing complexity) or additional visual cues (e.g., extra spheres for depth perception).
- EMG classifier training: Although training duration and date don't impact results, electrode placement is crucial and must be adjusted per participant.
- Solve vibrator delay & serial port issues: Investigate the cause of vibrator delays and fix automatic serial port closures occurring under the EW condition.
- Increase trial counts: More trials and training are needed to achieve consistent results and let participants optimize their control strategies.
- Add experimental conditions: Consider additional control conditions:
  - KW: Keyboard with vibrators.
  - VEWO: Visual feedback without vibrators.
These allow better assessment of vibrotactile feedback and comparison with visual feedback.
- Improve data analysis methods: Introduce time-weighted scoring as a potential evaluation metric.

🤖 System Integration and Application:
- Apply the complete system to amputees or commercialize it.
- Build a robust and stable system.
- Combine this system with other sensory feedback mechanisms to mimic the sensory experience of a biological hand as closely as possible.
- The ultimate goal is to develop a new prosthetic system that reduces abandonment rates among amputees and improves their quality of life.


