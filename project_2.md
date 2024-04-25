### Project 2

#### 1. Objective Definition:

Construct an alpha selection framework to help filter the most robust and effective alphas from a growing big alpha pool, in order to get a better prediction precision compared to baseline. The framework's input is alpha pool, the output is the alphas being selected to add to the model, the object is to ensure we make progress in model and to avoid some risks.

#### 2. Scope & Constraints:

Scope: The related area knowledge may includes statistics, algebra, optimization, machine learning/deep learning and coding skill is needed (usually in Python)
Constraints: Part of data should be out of reach to do out-sample test

#### 3. Problem Selection:

Alpha selection framework

Generally speaking it can be seen as a porfolio optimization problem or a risk control problem, because when we test an alpha's effectiveness, we should do the correlation test, measure the reliability of data, the risk exposure and whether it is fit with the market condition at present. If the market condition changes, alphas can be invalid. To make the whole prediction more robust, we can do test on alphas in different situations

#### 4. Data & Tools:

Data: Alpha datas and market datas, along with risk data (like Barra)
Tool: Coding environment and supportive tools: calculation, visualization & experiments

#### 5. Methodology Outline:

- Data analysis: do alpha pool statistics, check data reliability, examine the risk exposure, divide alphas into different groups (according to different kinds and different usable environment respectively)
- Model development: construct a baseline if needed. Use baseline model (tree or MLP) to test marginal contribution of alpha (eg. We can set 10 different tree models, like gbdt, to test the rubost of a series of new alphas. If alphas do benefit to all 10 models and pass the correlation, risk and market condition test, they can be add to the comprehensive model)
- Validation: use reserved data to do out-sample test; do pressure test: use more historical data and artificial data in different market/risk conditions to test the robust of alphas; finally put the framework into real-time environment to do validation.

#### 6. Expected outcomes:

- The framework should be able to select most helpful alphas from the pool, and make progress in the final prediction result.
- It can be used as a part of alpha management system, help filtering the new alphas and choose best alpha for modeling and trading. 
- More research can be done based on it, like how to apply this framework to genetic programming to create more high value alphas.