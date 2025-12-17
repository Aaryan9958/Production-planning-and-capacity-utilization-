Production Scheduling Optimization Using MILP (Mixed-Integer Linear Programming model) for multi-product beverage manufacturing

Project Overview
This project builds a Mixed-Integer Linear Programming (MILP) optimization model to schedule weekly production for a beverage manufacturing plant producing three products:
-Ready-to-Drink Protein Shake (P1)
-Zero-Sugar Energy Drink (P2)
-Functional Flavored Water (P3)

The factory operates three shared resources:
-Mixing & Blending Tank (M1) — bottleneck
-Filling Line (M2)
-Packaging Line (M3)
The goal is to determine the optimal daily production plan that meets demand while minimizing total cost, setups, and late orders.

Business Problem
Beverage companies face common operational issues:
1.Bottleneck machines cause delays
2.Too many product changeovers
3.High overtime or underutilization
4.Inconsistent on-time delivery
5.Poor visibility into how demand spikes affect the system

This project solves these problems using Operations Research + Optimization.

Solution Approach
A complete Mixed-Integer Linear Programming (MILP) model was built using Python and PuLP.

Decision Variables:
-Units produced per product per day
-Binary setup indicator
-End-of-day inventory

Constraints:
-Machine capacity per day
-Processing time per product per machine
-Setup time per changeover
-Inventory balance
-Fulfillment of demand

Objective Function:
Minimize Total Cost, including:
Production cost + setup cost + holding cost + late penalty.

Scenarios Simulated:
The model runs three realistic planning scenarios:

1. Scenario A – Flexible
-All machines run at full capacity
-Low setup cost
-System operates with maximum flexibility
-Achieves ~98% on-time delivery

2. Scenario B – Setup-Minimizing
-Higher cost for switching products
-Encourages batching
-Slightly higher total cost
-Same throughput as Scenario A

3. Scenario C – Tight Capacity + Rush Demand
-Reduced Mixing Tank capacity
-Additional rush order added
-System becomes constrained
-On-time delivery drops to ~47%

Key Insights
1. Mixing Tank (M1) is the bottleneck
M1 operated at 100% utilization in all scenarios, restricting total throughput.

2. Scenario A is the optimal strategy
Best balance of cost, throughput, and service level.

3. Scenario C exposes system weakness
Rush orders and reduced capacity overwhelm the bottleneck.

4. Setup penalties impact cost
But do not change the bottleneck or throughput significantly.

KPIs Generated
The model computes:
-Total cost
-Throughput (per product and total)
-Late units
-On-time delivery %
-Total setups
-Machine utilization (daily & average)
-Full daily production schedule

Tech Stack
-Python
-PuLP (MILP Optimization)
-Pandas
-NumPy
-Matplotlib 
