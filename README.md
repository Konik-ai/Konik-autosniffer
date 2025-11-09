Konik-Autosniffer

Konik-Autosniffer is an experimental project aimed at simplifying and accelerating the process of porting new cars to openpilot.

🚗 What is Autosniffer?

Autosniffer is a tool we’re designing to guide the user through a series of in-car actions (displayed directly on the openpilot screen) and automatically label the corresponding CAN message timeframes.

Example:

The device asks: “Turn on the left blinker.”
The user performs the action → the tool marks that section of the CAN log as left_blinker.

This makes it much easier for developers and the community to identify, verify, and confirm CAN signals when working on new car ports.

🧠 Why we’re building it

Porting new cars to openpilot requires a lot of manual CAN signal analysis. Autosniffer aims to standardize and partially automate this process by:

guiding the user through predefined actions,

tagging timestamps automatically,

and later cross-confirming signals between multiple recordings of identical car models.

The long-term vision is to use machine learning to help recognize signals automatically and, eventually, assist in the porting process itself.

🛠️ Development plan

Stage 1 – Guided Signal Tagging

Build a guided recorder that runs on an openpilot device (or on Konik A1M / C3X).

Display clear instructions to the user (e.g., “Press the brake pedal for 3 seconds”).

Record and label CAN data automatically with precise timestamps.

Stage 2 – Cross-Confirmation and Machine Learning

Implement cross-confirmation between recordings of identical car models using data hosted on the server stable.konik.ai as a shared base.

Use ML models to learn and recognize patterns in the CAN data and verify signals automatically.

Stage 3 – Assisted Porting

Develop ML-based tools to help automate portions of the openpilot porting process.

🧩 Tech overview

Target platform: Konik A1M / C3X (or laptop with Panda)

Data format: standard openpilot CAN logs + metadata (JSON sidecar)

Server: stable.konik.ai – base for data collection and cross-confirmation

👥 Looking for collaborators

We’re at the very beginning and looking for people with experience in:

openpilot porting,

Cabana and CAN log analysis,

Python / C++ / data processing,

or machine learning for signal recognition.

If you’d like to join, contribute ideas, or test early prototypes — join our community on Discord:
👉 Konik-Autosniffer Discord Channel
