# Democritus

## Experiments: STAGE 1
Pre Experiments: This is the first prototype I have created for the project: [Main Code](https://github.com/omaralsebaey/Democritus/blob/main/MainCode.ipynb). It is the main backend algorithm. For prototyping purposes the objective and constraints will be developed as a CQM, and converted to BQM. For each experiment, the added code for experimentation is surrounded by comments to signify so. Due to accessibilty constraints, I only have access to classical solvers. Hence some experiments should be repeated with a real QPU. For now, I will be using the *ExactSolver* and the *SimulatedAnealingSampler*. The *ExactSolver* will be to confirm that the math and algorithms are correct. While the *SimulatedAnealingSampler* will be for scaling the algorithms to ensure a real QPU will be able to solve it. Finally, some experiments are for testing purposes, to make sure the test subject works, while other experiments are for researching purposes. 

Post Experiments:  Was SA used? [New Code]() I checked if its a weight issue

### Experiments Summary    
| No | Title             | Purpose | Expected Result | Pass | Repeat with QPU |
|:---|-------------------|:-----:|-----|:----:|:-----:|
| #1 | Variable Count    | Testing | Correct No | ✅ | ❌ |
| #2 | Coefficient Range | Research | penalties ~10–100× objective |  | ✅ |
| #3 | All zero energy   | Test | Cost too high | ✅ | ❌ |
| #4 | Classical vehicle | Test | Lowest cost when constraint satisfied | ❌ | ❌ |
| #5 | Feasibility check | Test | all violations = 0 | ✅ | ✅ |
| #6 | Manual cost check | Test | Match true cost | ✅ | ✅ |
| #7 | visualization     | Research | continuous, valid routes |  | ✅ |  
<br>

- **Experiment 1: Variable Count**  
Notebook: [Variable Count](https://github.com/omaralsebaey/Democritus/blob/main/Experiment1.ipynb)  
Abstract: This test is to check if the BQM contains all required variables. Nothing extra, Nothing missing.  
Expected Result: Correct Number of variables.  
Pass: ✅

- **Experiment 2:**  
Notebook: []()  
Abstract:   
Expected Result:  
Pass:

- **Experiment 3: All Zero Solution**  
Notebook: [All Zero Solution](https://github.com/omaralsebaey/Democritus/blob/main/Experiment3.ipynb)  
Abstract: We need to make sure the solver does not think that an all zero solution (as in no routes used, 
no customers visited) is a viable solution.  
Expected Result: Cost too high  
Pass: ✅

- **Experiment 4:**  
Notebook: []()  
Abstract:   
Expected Result:  
Pass:

- **Experiment 5:**  
Notebook: []()  
Abstract:   
Expected Result:  
Pass:

- **Experiment 6:**  
Notebook: []()  
Abstract:   
Expected Result:  
Pass:

- **Experiment 7:**  
Notebook: []()  
Abstract:   
Expected Result:  
Pass:
