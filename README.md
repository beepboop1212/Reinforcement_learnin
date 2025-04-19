# 🤖 Q-Learning Maze Solver

This project is an implementation of a **Q-Learning agent** that learns to navigate a maze from a start position to a goal using **reinforcement learning**. The agent learns through trial and error, receiving rewards for reaching the goal and penalties for hitting walls or taking unnecessary steps.

---

## 🧠 Key Concepts

- **Q-Learning**: A value-based Reinforcement Learning algorithm used to find the optimal action-selection policy.
- **Exploration vs Exploitation**: The agent balances between exploring the environment and exploiting learned knowledge.
- **Reward System**:
  - ✅ Goal: +100
  - ❌ Wall: -10
  - ➖ Step: -1

---

## 🧰 Technologies Used

- Python
- NumPy
- Matplotlib

---

## 🧱 Maze Structure

The maze is a 2D NumPy array where:
- `0` = Free space
- `1` = Wall

Example:

```python
maze_layout = np.array([
    [0, 1, 1, 0, 0],
    [0, 0, 1, 1, 0],
    [0, 0, 0, 0, 0],
    [1, 1, 0, 1, 1],
    [0, 0, 0, 0, 0]
])



⸻

🧪 How It Works
	1.	Initialize Maze with start and goal positions.
	2.	Q-Learning Agent begins with no knowledge (Q-values initialized to zero).
	3.	Agent explores the maze across multiple episodes, updating its Q-table based on:
	•	Immediate reward
	•	Future expected rewards
	4.	Once trained, the agent can find optimal or near-optimal paths to the goal.

⸻

📈 Training Results

Example training (100 episodes):
	•	✅ Average Reward: ~29
	•	📉 Average Steps: ~20

After training:
	•	Optimal paths found within 8–10 steps
	•	Reward increased to ~90+

⸻

🚀 How to Run

1. Install Dependencies

pip install numpy matplotlib

2. Run the Script

Simply run the Python script or Jupyter Notebook.

python maze_solver.py

3. Output
	•	The agent’s path is printed and visualized
	•	Path shows start (S), goal (G), and learned path (#)
	•	Episode stats and Q-learning progress are plotted

⸻

🔍 Sample Output

Learned Path:
(0, 0)-> (0, 1)-> (1, 1)-> (1, 2)-> (2, 2)-> (2, 3)-> (2, 4)-> (3, 4)-> Goal!
Number of steps: 8
Total reward: 93



⸻

📌 Notes
	•	This project simulates how AI agents learn environments without supervision.
	•	You can modify maze size, start/goal, or rewards to experiment with different dynamics.
	•	Agent uses 4 actions: Up, Down, Left, Right.

⸻


🧠 Author’s Tip

Start with a small maze and increase complexity as the agent learns. Try changing penalties or discount factor to observe agent behavior!

---
