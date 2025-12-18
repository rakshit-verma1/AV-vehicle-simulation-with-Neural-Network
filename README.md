# Self-Driving Car Simulation using a Simple Neural Network (JavaScript)

This project demonstrates how to build a **simple neural network from scratch in JavaScript** and use it to train a car to **avoid traffic** in a 2D simulation.

The project is purely **educational**, focused on understanding how perception (sensors), decision-making (neural networks), and evolution-style learning can work together — **without using any ML libraries**.

This implementation is based on the FreeCodeCamp tutorial:
https://www.youtube.com/watch?v=Rs_rAxEsAvI

---

## 🚗 Project Overview

- Cars drive on a multi-lane road rendered using **HTML Canvas**
- Each AI car has:
  - Ray-based distance sensors
  - A feed-forward neural network
- Sensor readings are fed into the neural network
- The network outputs steering and acceleration decisions
- The best-performing car is selected each frame
- Its neural network can be **saved** and **reused** across sessions

Two live visualizations:
- **Car Simulation Canvas**
- **Neural Network Visualization Canvas**

---

## 🧠 Learning Strategy

This project does **not** use backpropagation.

Learning happens through:
1. Creating many cars (`N = 1000`)
2. Selecting the car that travels the farthest without collision
3. Mutating its neural network slightly
4. Repeating over many frames

This resembles a simple **genetic / evolutionary learning approach**.

---

## 🎮 Controls

| Button | Description |
|------|------------|
| 💾 Save | Saves the current best neural network to `localStorage` |
| 🗑️ Discard | Clears saved network and restarts learning |

Saved networks automatically load on refresh.

---

## ⚙️ Configuration

Inside `script.js`:

```js
const N = 1000;
```

- Increase `N` → better learning, higher CPU usage
- Decrease `N` → faster performance

---

## 🗂️ File Structure

```
.
├── index.html
├── styles.css
├── script.js
├── car.js
├── sensor.js
├── network.js
├── visualizer.js
├── road.js
├── controls.js
├── utils.js
```

---

## ▶️ How to Run Locally

1. Clone the repository
2. Open `index.html` in a browser
3. Let the simulation run

---

## 🌐 Live Demo

[Deployed Link(N=1000)](https://rakshit-verma1.github.io/AV-vehicle-simulation-with-Neural-Network/)

---

## 📚 Learning Outcomes

- Neural networks from scratch
- Sensor-based perception
- Evolution-style learning
- Canvas-based visualization

---

## 🏗️ Credits

Inspired by **FreeCodeCamp – Self Driving Car with JavaScript**  
https://www.youtube.com/watch?v=Rs_rAxEsAvI

---

## ⚠️ Disclaimer

For educational purposes only.