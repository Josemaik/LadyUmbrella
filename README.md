
<br />
<p align="center">
  <img width="3840" height="1240" alt="MainKeyArt" src="https://github.com/user-attachments/assets/9425deb8-efff-4c28-ba44-283b32dd4aea" />
  <br />
  <h1 align="center">☂️ Lady Umbrella ☂️
	<br /><br />
    <p>
      <a href="https://store.steampowered.com/app/3956890/Lady_Umbrella/" target="_blank">
	    <img src="https://img.shields.io/badge/Now%20on%20Steam-1b2838?style=for-the-badge&logo=steam&logoColor=white" alt="Play on Steam">
      </a>
    </p>
  </h1>
</p>

Lady Umbrella is a 3d action-adventure shooter in which the player plays the role of special agent Francesca De Angelis (aka Lady Umbrella) who, while infiltrating the last mafia family in Italy, is betrayed and incriminated by her partner. She must now clear her name by preventing her own agency from arresting her, and defeating the mafia using her main weapon: a high-tech shotgun umbrella that functions as a shield and contains multiple hidden gadgets.

Switch between combat, traversal, and puzzle-solving — the umbrella isn’t just a weapon, it’s your lifeline.

<img src="https://github.com/user-attachments/assets/4aee6508-691b-43ef-b264-813fc3abeb55" width="400">
<img src="https://github.com/user-attachments/assets/cec211ad-5ac2-4f94-b322-ba4f90247155" width="400">
<img src="https://github.com/user-attachments/assets/8d223ce6-e1df-46c6-a53f-65ac19cfe8fe" width="400">
<img src="https://github.com/user-attachments/assets/f140a235-c668-46b4-8b40-988defa0bb5a" width="400">

### 🛠️ Contributions
---
#### Arena Builder Tool

Encounter Builder 
Custom tool designed to help designer team <strong>create, organize and test combat encounters</strong> efficiently, bridging the gap between design and gameplay.
The system dynamically <strong>generates and manages spawners and trigger boxes</strong>, giving designers full control over combat flow while keeping everything neatly structured within the editor outliner.</p>
                <p>Each spawner can be configured directly from the details panel to define:</p>
 [ArenaManager.h](Source/LadyUmbrella/AI/Managers/ArenaManager.h) | [ArenaManager.cpp](Source/LadyUmbrella/AI/Managers/ArenaManager.cpp)
 [AISpawnPoint.h](Source/LadyUmbrella/AI/Managers/AISpawnPoint.h) | [AISpawnPoint.cpp](Source/LadyUmbrella/AI/Managers/AISpawnPoint.cpp)
 [TriggerBoxArena.h](Source/LadyUmbrella/AI/Triggers/TriggerBoxArena.h) | [TriggerBoxArena.cpp](Source/LadyUmbrella/AI/Triggers/TriggerBoxArena.cpp)

## Arena Manager Components

<b>Enemy Spawner Component</b>,Responsible for managing all spawning logic in a combat arena. It organizes spawn points into waves, reinforcements groups ans special events.

[EnemySpawnerComponent.h](Source/LadyUmbrella/AI/Components/EnemySpawnerComponent.h) | [EnemySpawnerComponent.cpp](Source/LadyUmbrella/AI/Components/EnemySpawnerComponent.cpp)

<b>Enemy Coordination Component</b>, Responsible for managing coordinated, group-based enemy behaviour during combat by controlling various tokens that
                    determinate which enemies can perform actions such as attacking, flanking, firing electric bullets or throwing grenades.

[EnemyCoordinationComponent.h](Source/LadyUmbrella/AI/Components/EnemyCoordinationComponent.h) | [EnemyCoordinationComponent.cpp](Source/LadyUmbrella/AI/Components/EnemyCoordinationComponent.cpp)

<b>Enemy Zones Component</b>,Responsible for tracking and managing spatial "Zones" within arena, each containing data about how many enemies and free covers exist in that area.

[EnemyZonesComponent.h](Source/LadyUmbrella/AI/Components/EnemyZonesComponent.h) | [EnemyZonesComponent.cpp](Source/LadyUmbrella/AI/Components/EnemyZonesComponent.cpp)

## Behaviour Trees

<p>The AI Behavior Tree system is organized by archetype and it has been created following a hierarchy:</p>
 <ul>
  <li><strong>Main Tree:</strong> Controls the overall decision flow of the archetype (e.g., combat, patrol, arena entry).</li>
  <li><strong>Context Subtrees:</strong> Each represents a specific behavioral context or state (e.g., Combat, Patrol, EnterArena).
These are activated based on Blackboard conditions or Selector priorities.</li>
  <li><strong>Action Subtrees:</strong> Contain concrete tactical actions such as attacking, finding cover or flee.</li>
</ul>

[CustomTasks](Source/LadyUmbrella/AI/BTTasks) | [CustomServices](Source/LadyUmbrella/AI/BTServices) | 
[AIControllers](Source/LadyUmbrella/AI/Controllers)

## Enviroment Query System

<p>I utilized Unreal Engine's Environment Query System (EQS) to drive a variety of dynamic decision-making processes for AI agents, enabling them to react intelligently to their surroundings.

[EQS Files](Source/LadyUmbrella/AI/EQS)

### 🤝 Acknowledgements
---

All the playtesters who gave feedback on the game, from the earliest state to the end.<br />
Everyone at Zulo Interactive who made this game possible.
