# PostStint Analysis (PS-Analysis)

**Your local AI driving coach for iRacing.**  
**Drive. Learn. Optimize.**

PostStint Analysis analyzes your driving after each stint and helps you improve both your driving technique and your car setup. It runs locally on your PC, uses your iRacing telemetry, and combines your own driving data with anonymous community reference cards.

**Alpha version 0.1.10 — currently limited to a maximum of 7 testers.**

[**Download the latest release**](https://github.com/hitschler23/PostStint-Analysis-PS-Analysis-/releases/latest) · [View source code](https://github.com/hitschler23/PostStint-Analysis-PS-Analysis-)

---

## 🏁 What is PostStint Analysis?

PS-Analysis is a local driving coach and setup assistant designed for iRacing. After your session, it analyzes your telemetry and provides practical feedback to help you find lap time.

### Driving Coach
- Analyzes braking, throttle, steering and cornering speed.
- Identifies braking zones and potential areas for improvement.
- Compares your driving against available reference data.
- Provides actionable coaching feedback to help you improve consistency and pace.
- Supports spoken output using your own voice recording.

### Setup Assistant
- Helps you identify potential setup improvements.
- Works with setup reference ranges from the community.
- Covers parameters such as tire pressure, camber, toe, springs, dampers, anti-roll bars, wings, ride height, brake bias and differential settings.

### Detailed Community Telemetry
Version 0.1.10 introduces more detailed community telemetry for individual corners, including:

- Braking points and brake pressure
- Throttle application
- Steering input
- Apex speed
- Setup parameter ranges

The goal is to build increasingly useful reference data from real driving sessions.

---

## 🧠 Community Cards — The Core of PS-Analysis

Community cards provide shared reference data for specific combinations of:

- Track
- Car
- Dry or wet conditions
- Track temperature range
- Fuel-load range

There are two types of cards:

**Telemetry Cards** contain reference ranges for driving behavior, including braking zones, brake pressure, throttle, steering and cornering speed.

**Setup Cards** contain reference ranges for actual vehicle setup parameters.

Each combination has one shared community entry. Contributions are weighted into the existing reference data, while outliers are handled to reduce the influence of unusual values. Empty combinations are not created unnecessarily.

The fuel load determines the driving mode:

- **Below 15 liters:** Hotlap
- **15–55 liters:** Race
- **Above 55 liters:** Endurance

If an exact reference is unavailable, PS-Analysis can fall back to a less specific compatible reference. Wet and dry data are never mixed.

---

## 🔒 Your Data. Your PC. Your Control.

PS-Analysis is designed around local processing and data privacy.

**Your original driving data stays on your computer.**

- Original iRacing `.ibt` files remain local.
- Your lap times, personal memory and setups remain local.
- Your password is stored as a hash on your PC.
- Core coaching and analysis use your local data and previously downloaded community cards.
- Community sharing is limited to anonymous reference data, not complete telemetry files.

When you are offline, no new community data is sent. You can continue working with your own data and previously downloaded references.

If you do not want a team setup or a particular session to contribute to the community, go offline before driving.

### What gets shared?

Only eligible laps from sessions driven while online can contribute to community cards. The shared information consists of anonymous reference ranges for the relevant track, car, conditions, fuel range, telemetry and setup parameters.

Names, team information and original telemetry files are not included in the community cards.

Files already present in your iRacing folder, as well as sessions driven before going online, are never uploaded retroactively.

---

## 📊 How Are Laps Processed?

PS-Analysis does not automatically use every lap.

- Only clean, eligible laps from online driving sessions are considered.
- Laps involving off-track incidents are excluded.
- Laps without the required temperature or fuel information are skipped rather than guessed.
- If conditions change during a session, eligible laps are grouped into the appropriate dry or wet reference cards.
- Each valid lap contributes to its matching combination instead of uploading the complete `.ibt` file.

This helps keep the community references relevant to the conditions in which the car was driven.

---

## 🖥️ Local AI and Performance

PS-Analysis uses local AI components for its coaching workflow. Analysis takes place after the driving session, helping avoid unnecessary computing load while you are on track.

The aim is to provide useful coaching without requiring a central server to perform the core analysis.

Community sharing and updates depend on the online services being available; local analysis can continue using the data already stored on your PC.

---

## 🚧 Alpha Testing — Maximum 7 Testers

PS-Analysis is actively being developed and is currently in the alpha stage.

**Only 7 testers maximum are planned for this testing phase.**

The current priority is to test the coaching quality, telemetry analysis, setup references, installation and overall stability with real iRacing sessions.

Feedback from testers will help improve the system and the quality of its recommendations.

[**Get PS-Analysis 0.1.10 alpha**](https://github.com/hitschler23/PostStint-Analysis-PS-Analysis-/releases/tag/v0.1.10)

---

## 🛠️ Current Version

**PS-Analysis 0.1.10 alpha**

Latest improvements:
- Denser community telemetry for individual corners
- Braking, throttle, steering and apex-speed reference data
- Setup parameter ranges
- Continued development of local coaching and community references

PS-Analysis is an evolving project. Features, recommendations and stability may change during alpha testing.

**PostStint Analysis — Drive. Learn. Optimize.**
