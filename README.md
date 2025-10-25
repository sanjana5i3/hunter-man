

# 🎮 Unity 3D Game –The Hunter Man

## 🧩 Overview

This project is a Unity-based 3D game prototype featuring **player movement**, **enemy AI**, and a **coin collection system**.
The player can move, rotate, attack enemies, collect coins, and defend against attacks. The enemy follows the player using **NavMesh AI**, attacks when in range, and can take or deal damage.



## 🚀 Features

### 👤 Player System (`Player1.cs`)

* Smooth **movement and rotation** controls using arrow keys.
* **Attack** and **Defend** animations with spacebar input.
* **Health system** with a UI health bar.
* **Coin collection** system and coin score UI.
* **Enemy interaction:** Player can deal and take damage.
* **Camera follow system** for third-person view.
* **Game over logic:** Automatically reloads scene when the player dies.

### 💰 Coin Collection System (`Coincollections.cs`)

* Detects collision with the player using `OnTriggerEnter`.
* Increases the player’s coin count when collected.
* Optionally supports sound and particle effects.
* Destroys the coin object after collection.

### 👹 Enemy AI System (`Enemy.cs`)

* Uses **NavMeshAgent** for navigation and movement.
* Detects player within a **detection radius** and follows them.
* Attacks player when within **attack range**.
* Plays **attack**, **defend**, and **death** animations.
* Takes damage and triggers a **death sequence** when health reaches zero.



## ⚙️ Controls

| Action       | Key            |
| ------------ | -------------- |
| Move Forward | ⬆️ Up Arrow    |
| Rotate Left  | ⬅️ Left Arrow  |
| Rotate Right | ➡️ Right Arrow |
| Attack       | Spacebar       |

---

## 🧠 Core Mechanics

* **Player–Enemy Interaction:**
  The player can attack enemies within a defined `attackDistance`. The enemy responds with attack and defend animations.
* **Damage System:**
  Both the player and enemy have independent health values and can take or deal damage.
* **Coin Collection:**
  Coins are collected upon collision, incrementing the player’s score and updating the UI in real-time.
* **NavMesh AI:**
  Enemy movement uses Unity’s `NavMeshAgent` to dynamically chase and attack the player within range.


## 🧱 Components Required

Attach these scripts to the following GameObjects in Unity:

| Script               | GameObject | Notes                                                   |
| -------------------- | ---------- | ------------------------------------------------------- |
| `Player1.cs`         | Player     | Requires Animator, AudioSource, and Collider            |
| `Enemy.cs`           | Enemy      | Requires Animator, AudioSource, NavMeshAgent, Rigidbody |
| `Coincollections.cs` | Coin       | Requires Collider (set as Trigger)                      |



## 🖥️ UI Elements

* **Health Bar (Slider):** Displays player’s current health.
* **Score Text:** Shows total coins collected.
* **Scene Management:** Reloads on player death.



## 🛠️ Tools & Technologies

* **Engine:** Unity 3D
* **Language:** C#
* **Components Used:**

  * Rigidbody
  * NavMeshAgent
  * Animator
  * AudioSource
  * UI (Text, Slider)
  * SceneManager



## 🎯 Future Enhancements

* Add sound effects for movement and attacks.
* Implement particle effects for coin collection and damage.
* Introduce multiple enemy types with varied behaviors.
* Add save/load system for coins and health.

