# 🏙️ **TURF WARS**

**A tile-based tactical territory-control game by Lars Nohrstedt — 2025**

Turf Wars is a turn-based, deterministic strategy game played on a procedurally seeded grid of “city blocks.”
You begin as a small gang controlling a single block center. Rival AI gangs do the same.
Each turn, you expand your turf, capture streets, take block centers, and try to dominate the city.

---

# 🎮 **How to Play**

## **Your Objective**

You win by doing **either** of the following:

### ✔ **Domination Victory**

Control **more than half of all block centers**.

### ✔ **Elimination Victory**

Eliminate every other gang by taking their last remaining turf slot.

---

# 🧩 **The Board**

The city is a grid of square **blocks**, each made of:

* **9 interior tiles (3×3)**
* The center tile is the **block’s center** — controlling it grants a new recruit to your gang full access to the block.
* Streets (the yellow road tiles) separate blocks.

### **Cell types**

* **Black tiles** — normal turf slots, claimable by any gang.
* **Dashed tile** — block center (special).
* **Road tiles** — streets between blocks; cannot be claimed.

---

# 🚷 **Movement & Claiming Rules**

You don’t move “units.”
Instead, each claimed tile represents one of your thugs having claimed that turf. For now.

Each turn you receive a number of **thug placements** (moves).
Click glowing tiles to claim them.

---

## **1. Moves Per Turn**

You always get at least **1 move** per turn.

Additional moves:

* **+1** if you control **more than one street**
* **+1 per block center** you control

Controlling centers is key for victory.

---

## **2. Movement Within a Block**

You may place a thug on:

* Any orthogonally adjacent tile to your own (up/down/left/right)
* OR anywhere inside the block **if you control that block’s center**

---

## **3. Moving Into Adjacent Blocks**

You cannot enter a new block unless the streets support it.

### **Orthogonal Entry (N, S, E, W)**

To enter an adjacent block horizontally or vertically:
➡️ **You must control the 3-tile street on your side of the border.**

Example:
Moving right into the block to your east requires you to control the **east street** of your current block.

---

### **Diagonal Entry (corner-to-corner)**

To step diagonally into a neighboring block through the corner:
➡️ **You must control BOTH streets that meet at that corner.**

This makes diagonal access rare and strategically valuable.

---

## **4. Capturing a Block Center**

To take a block center tile:
➡️ You must control **all 8 surrounding tiles** of that block.

This represents total block dominance.

---

# 💥 **Game End Conditions**

A game ends when:

### ✔ A gang controls >50% of block centers

OR

### ✔ A gang wipes out all others

OR

### ✔ A full round passes where *every player* has no moves (stalled city)

A modal shows the Game Over summary and a button to start a new match.

---

# 🤖 **AI Personalities**

Each AI gang is assigned a personality using the deterministic world seed.
Every personality behaves differently, and their interactions create emergent city-wide dynamics.

What they all have in common is that if they are able to claim a block center they will most definitely do so.

### **1. AGGRESSIVE**

* Prioritizes attacking enemy turf.
* Always targets the **weakest enemy**.
* Expands only when no attacks are available.

**Playstyle:** Bloodthirsty and reckless.

---

### **2. EXPANSIONIST**

* Prioritizes unclaimed tiles first.
* Then attacks **weakest** enemies.
* Aims for maximum growth per turn.

**Playstyle:** Fast, sprawling land-grabbers.

---

### **3. DIPLOMATIC**

* Avoids conflict early.
* Prefers empty tiles.
* **If forced to attack, always targets the *strongest* enemy**.

**Playstyle:** Kingmaker — breaks the leader’s momentum.

---

### **4. OPPORTUNISTIC**

**Priority order:**

1. Capture streets
2. Claim corner tiles
3. Claim empty tiles
4. Attack enemies

If attacking:

* They target the **weakest enemy**,
* Unless that enemy is a **Diplomat**, then they target the **strongest**.

**Playstyle:** Calculating and surprising.

---

### **5. FORTIFIER**

Focuses on **defensive architecture**:

* Prioritizes blocks where they own the center (fortresses)
* Builds **border fortifications** in neighboring blocks
* Disrupts opponents’ streets
* Claims corners to break diagonal access
* Attempts to prevent multi-block attacks

**Playstyle:** Defensive, territorial, suffocating.

---

### **6. RAIDER**

A predatory, hit-and-run AI:

1. Targets the **strongest enemy**, not the weakest
2. Breaks streets before expanding
3. Claims corner tiles
4. Prefers attacking over claiming empty tiles
5. Takes empties only if no attack is possible

**Playstyle:** Chaos-driven assassin.

---

# 🌱 **World Seeds**

The game is fully deterministic:

* Entering a **seed string** in the New Game menu fixes:

  * AI personalities
  * Starting positions

* Leave the field empty to auto-generate a seed.

This means:

* You can replay specific matches
* You can share seeds with friends
* You can build difficult scenarios intentionally

---

# 🧠 **Emergent Behavior**

Turf Wars produces a surprising amount of emergent tactics:

### **Territorial creep**

Expanding gangs collide along street borders, creating natural choke points and “front lines.”

### **Foothold wars**

The ability to enter a block hinges on a single street — producing “street wars.”

### **Corner traps**

Controlling corner tiles denies diagonal movement and can lock down multiple blocks.

### **Political fights**

Diplomats target leaders.
Raiders target leaders.
Aggressives target the weak.
Fortifiers build walls.
Expansionists gobble everything.

The personalities combine into unpredictable, fascinating mid-game dynamics.

---

# 🏁 **Controls**

* **Click** glowing tiles to place a thug.
* The game auto-ends your turn when you run out of moves. Press **End Turn** to end turn early.
* Check the right sidebar for rule-reminders, current leader-board, and active gang list.
* Click **New Game** to bring up the game setup menu.

---

# 🧪 **Prototype Notes**

A core feature should be interesting enough to stand alone as a game.
This is a vibe-coded proof-of-concept of the movement rules and their emergent behavior.
Forcing myself to focus on the game rules rather than the code was an experience in itself.
With that said I would not ship the code, but I am happy with the emergent behavior.




