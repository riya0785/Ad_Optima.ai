# Ad_Optima.ai

Ad Bidding Optimization Using Reinforcement Learning

**📌 Project Title:**
Ad Bidding Optimization Using DQN, PPO, and Actor-Critic Algorithms

**📖 Description:**
This project explores the use of Deep Reinforcement Learning (DRL) techniques—DQN (Deep Q-Network), PPO (Proximal Policy Optimization), and Actor-Critic—to optimize bidding strategies in real-time bidding (RTB) systems for online advertising. Each model is trained per website to maximize click-through performance while simulating discrete and continuous bid environments.


🚀 **Algorithms Implemented:**

Algorithm	Action Space	Description
1. DQN	Discrete	Uses a fixed set of bid values. Suitable for environments with predefined bid options.
2. PPO	Continuous	Leverages policy gradients with clipping for stability. Best suited for environments where fine-tuned bid precision is required.
3. Actor-Critic	Continuous	Combines value and policy learning. Learns both optimal value function and bid policy in tandem.
   
**🧠 Key Features:**
1. Custom Gym Environment tailored for ad bidding with reward structure based on winning auction and clicks.

2. Per-Website Agent Training to capture individual website bidding dynamics.

3. Weighted Feature State Vectors using bid_amount correlation for better learning efficiency.

4. Evaluation: Total clicks, most frequent bid, and average bid per website.

Visualizations: Bar plots of total clicks per website and summary tables of bid strategy.

**🧪 How to Run**

Setup Environment

bash
Copy
Edit
pip install -r requirements.txt

# Train DQN Agent
python dqn_ad_bidding.py

# Train PPO Agent
python ppo_ad_bidding.py

# Train Actor-Critic Agent
python actor_critic_ad_bidding.py
⚠️ Each script will automatically train and evaluate the model on all websites in the dataset.

📊 Output & Results:
Total Clicks Per Website (Bar chart)

Optimal Bid Per Website (Most frequent bid, average bid, frequency)

Optionally: Store trained models or logs using Tensorboard or pickle.

📈 Dataset Overview:
The dataset includes:

Time Features: day, hour, day_of_week

Ad Info: ad_type, website, user_segment

Performance: bid_amount, cost, base_ctr, adjusted_ctr

Target Features: won_auction, impression_served, click_occurred

Budget Feature: remaining_daily_budget

📦 Requirements (in requirements.txt)
pgsql
Copy
Edit
stable-baselines3
gymnasium
pandas
numpy
scikit-learn
matplotlib
shimmy
