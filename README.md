# Democritus

## STAGE 1: Prototype
This prototype disvocers the eligibitly of the following sktech, it was made mostly by ChatGPT.

Pre Experiments: This is the first prototype I have created for the project: [Main Code](https://github.com/omaralsebaey/Democritus/blob/main/MainCode.ipynb). It is the main backend algorithm. For prototyping purposes the objective and constraints will be developed as a CQM, and converted to BQM. For each experiment, the added code for experimentation is surrounded by comments to signify so. Due to accessibilty constraints, I only have access to classical solvers. Hence some experiments should be repeated with a real QPU. For now, I will be using the *ExactSolver* and the *SimulatedAnnealingSampler*. The *ExactSolver* will be to confirm that the math and algorithms are correct. While the *SimulatedAnnealingSampler* will be for scaling the algorithms to ensure a real QPU will be able to solve it. Finally, some experiments are for testing purposes, to make sure the test subject works, while other experiments are for researching purposes. 

Post Experiments:  Was SA used? [Main Code.1]() I checked if its a weight issue. Moving forward I will be adding less detail to the text as it took too much time. I will try to still maintain efficient documentation, Please refer back to me for any questions or comments.
Exp 2, the only research one should be postponed to the BQM. 
MTZ works for small []()
repeat with QPU?


### Experiments Summary    
| No | Title             | Purpose | Expected Result | Pass | Repeat with QPU |
|:---|-------------------|:-----:|-----|:----:|:-----:|
| #1 | Variable Count    | Testing | Correct No | ✅ | ❌ |
| #2 | Coefficient Range | Research | NA | NA | ✅ |
| #3 | All zero energy   | Test | Cost too high | ✅ | ❌ |
| #4 | Classical vehicle | Test | Lowest cost when constraint satisfied | ❌ | ❌ |
| #5 | Feasibility check | Test | No violations | ✅ | ✅ |
| #6 | Manual cost check | Test | Match true cost | ✅ | ✅ |
| #7 | Visualization     | Test | Valid routes | ❌ | ✅ |  
<br>

- **Experiment 1: Variable Count**  
Notebook: [Variable Count](https://github.com/omaralsebaey/Democritus/blob/main/Experiment1.ipynb)  
Abstract: This test is to check if the BQM contains all required variables. Nothing extra, Nothing missing.  
Expected Result: Correct Number of variables.  
Pass: ✅

- **Experiment 3: All Zero Solution**  
Notebook: [All Zero Solution](https://github.com/omaralsebaey/Democritus/blob/main/Experiment3.ipynb)  
Abstract: We need to make sure the solver does not think that an all zero solution (as in no routes used, 
no customers visited) is a viable solution.  
Expected Result: Cost too high.  
Pass: ✅

- **Experiment 4:**  
Notebook: [Classical Vehicle](https://github.com/omaralsebaey/Democritus/blob/main/Experiment4.ipynb)  
Abstract: This
test is to verify that each “exactly once” constraint (such as visiting a customer once or starting from the depot once) is correctly 
encoded in the QUBO model.  
Expected Result: The valid sample should have a lower cost compared to other samples.  
Pass: ❌

- **Experiment 5:**  
Notebook: [Feasibility Check](https://github.com/omaralsebaey/Democritus/blob/main/Experiment5.ipynb)  
Abstract: Due to the probabilistic and heuristic nature of quantum annealing, a low energy solution does not necessarily
mean it's feasible. This experiment introduces a feasibility checking test to make sure the candidate solution
satisfies every constraint in the model.  
Expected Result: All constraints should be feasible.  
Pass: ✅

- **Experiment 6:**  
Notebook: [Manual Cost Check](https://github.com/omaralsebaey/Democritus/blob/main/Experiment6.ipynb)  
Abstract: This experiment ensures that the energy calculated by the BQM accurately represents the true routing cost of the
optimal solution. This is done by manually calculating the cost and comparing it with the solver's result.  
Expected Result: Manually calculated cost should match solver's cost.  
Pass: ✅

- **Experiment 7:**  
Notebook: [Visualization](https://github.com/omaralsebaey/Democritus/blob/main/Experiment6.ipynb)  
Abstract: This test visualizes solver outputs as ordered vehicle routes to verify continuity and physical validity.  
Expected Result: Possible routes.  
Pass: ❌

