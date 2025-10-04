
# BlockForge: Multiplayer 3D Tetris

**Author:** Jiahao Wu  
**Project Type:** Multiplayer 3D Web Game  
**Technologies:** Three.js, Socket.io, JavaScript, HTML/CSS  

---

## 🧩 Overview

**BlockForge** is a real-time **multiplayer 3D Tetris-inspired game** that reimagines the classic puzzle gameplay in a fully interactive 3D environment. Players work together to manipulate falling blocks, rotate and move them in three dimensions, and strategically stack them inside a shared container space.  

Unlike traditional Tetris, BlockForge emphasizes **collaboration over competition**, requiring players to **communicate and coordinate** to fill the 3D space as efficiently as possible. With real-time synchronization, dynamic camera switching, and interactive block logic, the game creates a new kind of spatial puzzle-solving experience.

---

## 🕹️ Core Features

- 🧑‍🤝‍🧑 **Multiplayer Gameplay** – Built with **Socket.io**, players join a shared game session and control falling blocks together in real time.  
- 🧱 **3D Tetris Mechanics** – Classic block-dropping gameplay reimagined in 3D space. Players can rotate and move blocks along all axes.  
- 🧭 **Collaborative Objectives** – Instead of competing for score, players aim to fill the 3D container cooperatively.  
- 🔁 **Dynamic Camera System** – Players can toggle between **front and back views** for better spatial awareness.  
- 🧠 **Role Switching** – Players alternate between **controller** and **observer** roles, adding variety and teamwork to gameplay.  
- 🌐 **Web-Based** – Runs directly in the browser with no installation required.

---

## ⚙️ Technologies Used

- **Three.js** – Rendering the 3D environment, blocks, grid, lighting, and camera controls.  
- **Socket.io** – Real-time multiplayer communication and role synchronization.  
- **JavaScript (ES6)** – Core game logic, player input handling, block movement, and collision detection.  
- **HTML/CSS** – UI layout, rendering canvas, and responsive design.

---

## 🧠 Gameplay Mechanics

### 🎮 Player Roles
- **Controller:** Controls block movement — rotates, shifts, and drops pieces.  
- **Observer:** Watches gameplay from another perspective and swaps roles dynamically.  

### 🧱 Block Interaction
- **Arrow Keys:**  
  - `← / →` – Move block left or right  
  - `↑` – Rotate block  
  - `↓` – Accelerate block downward  

- **Real-Time Sync:** All block actions are broadcast across clients via Socket.io, so everyone sees the same world.

### 📦 Game Rules
- Blocks spawn at the top and fall due to gravity.  
- Blocks **collide with existing structures** and stack naturally inside the container.  
- The game ends when blocks reach the top of the container.  
- Players must **collaborate strategically** to build stable structures and avoid overflow.

---

## 🧰 Project Structure

```
BlockForge/
├── index.html            # Main entry point
├── script.js            # Core Three.js scene, block logic, camera, and animation loop
├── socket.js            # Socket.io multiplayer event handling
├── styles.css           # UI styles and layout
└── assets/              # 3D models, textures, or sounds (if any)
```

---

## 🔧 Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/blockforge.git
cd blockforge
```

### 2. Install dependencies
```bash
npm install
```

### 3. Run the server
```bash
node server.js
```

### 4. Launch the game
Open `http://localhost:3500` in your browser.

---

## 🧪 Key Implementation Details

- **Game Grid Rendering:**  
  Vertical and horizontal lines are drawn dynamically to form a 3D playfield.  
- **Real-Time Role Assignment:**  
  Socket.io assigns roles (`controller` or `observer`) to players as they connect.  
- **Collision Detection:**  
  Custom logic ensures blocks stack properly and detect floor/wall contact.  
- **Dynamic Queue System:**  
  Future blocks are queued with gradually decreasing lighting intensity to visualize upcoming pieces.  
- **Camera Switching:**  
  Smooth transitions between camera angles based on player role or input.

---

## 🚀 Future Improvements

- 🧠 **Physics Engine Integration:** Add realistic gravity, rotation inertia, and collisions with Cannon-ES.  
- 🤝 **Enhanced Multiplayer:** Support for more players and cooperative modes.  
- 🏆 **Scoring & Objectives:** Add levels, scores, or challenges for competitive play.  
- 📱 **Mobile Support:** Touch controls and responsive UI for mobile browsers.  
- 🧩 **New Block Types:** More complex shapes and power-ups to diversify gameplay.

---

## 🧑‍💻 Author

**Jiahao Wu**  
- [Portfolio](https://johnwu-8dvrhf4mi-pipixialetsgo.vercel.app)  
- [GitHub](https://github.com/PIPIXIALETSGO)

---

## 📜 License

This project is licensed under the MIT License — feel free to use, modify, and share it.
