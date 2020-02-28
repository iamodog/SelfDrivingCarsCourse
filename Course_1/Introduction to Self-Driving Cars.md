# The Story of Autonomous Vehicles

Revenir dessus ( vidéo de 13 min)

# Taxonomy of Driving

The driving task is composed of 3 sub-tasks:

- Perception
- Motion Planning
- Controlling the vehicle

There is 6 levels to classify a driving system automation:

- Level 0: No automation
- Level 1: Driving assistance (longitudinal or lateral control)
- Level 2: Partial driving automation (longitudinal and lateral control)
- Level 3: Level 2 + OEDR (Object and Event Detection and Reponse)
- Level 4: Level 3 + Fallback(Handles emergency: the driver can entirely focus on other tasks)
- Level 5: Level 4 + Unlimited ODD (Operational Design Domain) can operate under any condition

Actually, the maximum available in the industry is the level 3, however Waymo has deployed vehicle for public transport with the level 4 in a defined geographic area.

# Requirements for Perception

Perception is making sense of the environment and ourselves in the environment.

The main tasks for perception are detecting and assessing various types of static and dynamic objects and agents in the environment and the task of making sense of how the vehicle is moving trough the environment.

# Driving Decisions and Actions

There is differents types of planing: long term, short term and immediate planning.

For this, we have 2 differents planning approaches: Reactive and predictive planning.
Obviously, the most we can use predictive planning, better it is, however, reactive planning is sometimes unavoidable.
