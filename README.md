# PostStint Analysis (PS-Analysis)

**Your local AI driving coach for iRacing.**
**Drive. Learn. Optimize.**

PostStint Analysis analyzes your driving after each stint and helps you improve both your driving technique and your car setup. It runs locally on your PC, uses your iRacing telemetry, and combines your own driving data with anonymous community reference cards.

**Alpha version 0.1.11 — currently limited to a maximum of 7 testers.**

[**Download the latest release**](https://github.com/hitschler23/PostStint-Analysis-PS-Analysis-/releases/latest) · [View source code](https://github.com/hitschler23/PostStint-Analysis-PS-Analysis-)

---

## What is PostStint Analysis?

PS-Analysis is a local driving coach and setup assistant for iRacing. After your session, it reads the telemetry on your PC and gives practical feedback so you can find lap time.

A standalone tool. Not affiliated with iRacing.com.

### Driving Coach
- Analyzes braking, throttle, steering and cornering speed.
- Identifies braking zones and where time is available.
- Compares your driving with the community reference for the same track, car, weather, temperature and fuel load.
- Names the near edge of that range, for example a few meters later on the brake or a few percent less brake pressure.
- Supports spoken output.

### Setup Assistant
- Helps you identify potential setup improvements.
- Works with setup reference ranges from the community.
- Covers tire pressure, camber, toe, springs, dampers, anti-roll bars, wings, ride height, brake bias and differential settings, where the telemetry file actually contains those values.

### Community telemetry, per corner
Each telemetry card can carry, for a corner:

- Brake point in meters before the corner, and brake pressure
- Throttle point relative to the apex, and throttle percentage
- Steering angle at the apex
- Apex speed
- Setup parameter ranges

The goal is to build a useful reference from real sessions and to move a driver toward that reference one step at a time.

---

## Community cards

Community cards are shared reference data for one combination of:

- Track
- Car
- Dry or wet
- Track temperature band
- Fuel-load band

**Telemetry cards** hold the driving ranges above.
**Setup cards** hold the setup ranges.

Each combination has one living entry. A new session is merged into that entry. An outlier does not blow the range open. Wet and dry are never mixed. If the exact card is missing, a less specific compatible card can be used.

Fuel load selects the band:

- **Below 15 liters:** Hotlap
- **15–55 liters:** Race
- **Above 55 liters:** Endurance

---

## Your data stays on your PC

The original iRacing `.ibt` files stay on your computer. Lap times, personal memory and setups stay local. The coach works from that local data and from community cards already on the PC.

What can leave the PC is an anonymous reference range for track, car, conditions, fuel band, telemetry and setup. No name, no team, no complete telemetry file.

Sign-in is Discord. One click opens the browser. The PC stores only your Discord user ID and display name.

Offline, nothing new is sent. You keep working with your own data and the cards already downloaded. If a session should not contribute, go offline before you drive.

### Train the coach

Older `.ibt` files are not read on their own. The button **Train the coach** asks first:

You are training the coach with your data. The data is anonymous and cannot be traced back to you. Confirm that you want this.

Only after you confirm are those files turned into the same anonymous cards. Each file is recognized by its content and counted once. A renamed copy is still the same file and is skipped. That keeps the ranges from being distorted.

### Which laps count

- Only clean, eligible laps are used.
- Off-track laps are excluded.
- Laps without the required temperature or fuel information are skipped, not guessed.
- If the track changes between dry and wet, laps go into the matching card.
- The complete `.ibt` is not uploaded.

---

## On your PC

The installer is in English, so it is readable outside Germany. On a German Windows it stays German.

Telemetry is taken from the real Documents folder Windows reports. That includes a normal `Documents` folder, a folder redirected through OneDrive, and a localized name such as `ドキュメント`, including user names that are not Latin letters.

After a new sign-in, the short introduction comes first. **Train the coach** is the step after online/offline. The online window stays closed until you finish that introduction with **Done**. On the next sign-in it opens right away.

Analysis runs locally after the session, so the PC is not doing this work while you are on track. Sharing and updates need the online services. Local coaching continues with what is already stored.

---

## Alpha — maximum 7 testers

PS-Analysis is in alpha. This phase is limited to 7 testers. The aim is to find bugs, improve coaching quality, and make the app more reliable. Tester feedback shapes the next releases.

[**Get PS-Analysis 0.1.11 alpha**](https://github.com/hitschler23/PostStint-Analysis-PS-Analysis-/releases/tag/v0.1.11)

---

## Current version

**PS-Analysis 0.1.11 alpha**

- Discord sign-in
- Train the coach on older telemetry, each file once, anonymous
- Introduction before the online window on first sign-in
- Installer in English, German on German Windows
- Telemetry path follows the real Documents folder, including OneDrive and localized folder names
- Community cards per corner: brake, throttle, steering, apex speed, and setup ranges
- The coach names the near edge of those ranges

Thanks to ラグナチャン in Japan for the clear findings on installer language, the Documents folder, and the old name in the setup texts.

**PostStint Analysis — Drive. Learn. Optimize.**
