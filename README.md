# Democritus

## Experiments: STAGE 1
This is the first prototype I have created for the project: [Main Code](). It is the main backend algorithm. For prototyping purposes the objective and constraints will be developed as a CQM, and converted to BQM. For each experiment, the added code for experimentation is surrounded by comments to signify so. Due to accessibilty constraints, I only have access to classical solvers. Hence some experiments should be repeated with a real QPU. For now, I will be using the *ExactSolver* and the *SimulatedAnealingSampler*. The *ExactSolver* will be to confirm that the math and algorithms are correct. While the *SimulatedAnealingSampler* will be for scaling the algorithms to ensure a real QPU will be able to solve it. Finally, some experiments are for testing purposes, to make sure the test subject works, while other experiments are for researching purposes. 


### Experiments Summary    
| No | Title             | Purpose | Short Description | Expected Result | Pass | Repeat with QPU |
|:---|-------------------|:-----:|-----|-----|:----:|:-----:|
| #1 | Variable Count    | Testing | | Correct No | ✅ | ❌ |
| #2 | Coefficient Range | Research | | penalties ~10–100× objective |  | ✅ |  |
| #3 | all-zero energy   | Test | |  high (infeasible) |  |  | ❌ |
| #4 | one-hot energy    | Test | | lowest when constraint satisfied |  |  | ✅ |
| #5 | sampler run       | Test | | returns diverse samples |  |  | ✅ | 
| #6 | feasibility check | Test | | all violations = 0 |  |  | ✅ |
| #7 | route cost check  | Test | | matches true cost |  |  | ✅ |
| #8 | visualization     | Research | | continuous, valid routes |  |  | ✅ |



- **EXP TEST**  
  Notebook: [TEST](https://github.com/omaralsebaey/Democritus/blob/main/Experiment1.ipynb)  
  Abstract: xxx
  Expected Result:
  Pass: ✅
