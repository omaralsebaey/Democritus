# Democritus

## STAGE 1: Prototype
**Pre Experiments:**  
This is the first prototype I have created for the project: [Main Code](https://github.com/omaralsebaey/Democritus/blob/main/MainCode.ipynb). It is the main backend algorithm. For prototyping purposes the objective and constraints will be developed as a CQM, and converted to BQM. For each experiment, the added code for experimentation is surrounded by comments to signify so. Due to accessibilty constraints, I only have access to classical solvers. Hence some experiments should be repeated with a real QPU. For now, I will be using the *ExactSolver* and the *SimulatedAnnealingSampler*. The *ExactSolver* will be to confirm that the math and algorithms are correct. While the *SimulatedAnnealingSampler* will be for scaling the algorithms to ensure a real QPU will be able to solve it. Finally, some experiments are for testing purposes, to make sure the test subject works, while other experiments are for researching purposes. 

**Post Experiments:** I will split this xxxx into three parts, Problem 1: Exp 4, Probelm 2: MTZ, Furhter Notes.
- Problem 1: Exp 4  
Experiemtn 4 has failed. Hence I started tracking where ghe problem is, whether its a logical fault itht he protoype, fault in the experiemnt, or something else. To narrow down where the issue is, I continued the other experiments, 5,6, and 7. As they may reveal something valuable. Exp 5 and 6 passed but not 7. Exp 7 clearly showed that the prototype creates subtours. So I decided to fix that and see how it affects Exp 4. I made a new version of the main code MainCode.1(), which includes a MTZ constrain. Which indeed fixed the Exp 7, but not Exp 4. So now the conclusion I have reached is to move on to the next stage the BQM. As it’s possible moving to the BQM can resolve the issue on its own. Worst case scenario solving the issue is postponed. I see this is a relieving choice to go for, since I am entering my final exams season at the current stage.
- Problem 2: MTZ  
I am currrently facing irony. The MTZ constraint which resolves a significant issue I have is an problem of itself. Though it is a great contraint, it only works for the current CQM, and collapses when given a large BQM. So moving to the next stage I will have to eliminate subtours using a BQM friendly method. I should I have taken that into consideration before adding the MTZ.
- Further Notes  
There are various other comments on the prototypes and experiments. 
Was SA used? 
Moving forward I will keep my text more direct as it took too much time. I will try to still maintain efficient documentation, Please refer back to me for any questions or comments.
Exp 2, the only research one should be postponed to the BQM. 
repeat with QPU?
This prototype disvocers the eligibitly of the following sktech, it was made mostly by ChatGPT.


### Experiments Summary    
| No | Title             | Purpose | Expected Result | Pass | Repeat with QPU |
|:---|-------------------|:-----:|-----|:----:|:-----:|
| 1 | Variable Count    | Testing | Correct No | ✅ | ❌ |
| 2 | Coefficient Range | Research | NA | NA | ✅ |
| 3 | All zero energy   | Test | Cost too high | ✅ | ❌ |
| 4 | Classical vehicle | Test | Lowest cost when constraint satisfied | ❌ | ❌ |
| 5 | Feasibility check | Test | No violations | ✅ | ✅ |
| 6 | Manual cost check | Test | Match true cost | ✅ | ✅ |
| 7 | Visualization     | Test | Valid routes | ❌ | ✅ |  
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

