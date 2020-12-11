# Power-Up With Tekton Pipelines
Pearson training, December 16 2020.

## Intro
* Welcome
* How this will work
* What we will cover
* About me
* Installing necessary tools
  * minikube
  * kubectl
  * tkn
  * Tekton
  * VS Code tooling

---

## Tasks
* What is a Task
* What is a Step
* What is a TaskRun
* Tekton official Task catalog
* Parameters
* Shared volumes

### Hands-On
* Create a simple Task (1.yaml)
* Add parameters to a task (2.yaml)
* Add multiple steps to a task
* Shared volume between steps (3.yaml)

### Exercise
* Create your own task that outputs a log (4.yaml)
* Stretch goal (5.yaml)
  * Add a second `sleep` step to your task with a parameter for the number of seconds
  * Add a second parameter to the task for the name of the person to greet

---

## Pipelines
* What is a Pipeline
* What is a PipelineRun
* Parameters
* Task Order
* VS Code Pipeline visualizer

### Hands-On
* Create a simple pipeline with two tasks (6.yaml)
* Add Parameters to Pipelines (7.yaml)
* Reorder Tasks (8.yaml)
* Re-use Tasks (9.yaml)

### Exercise
* Given the tasks in 10.yaml, create an optimal pipeline to make a PB&J sandwich (11.yaml)
* Stretch goal:
  * Add a parameter to the Pipeline to echo who is eating the sandwich (12.yaml)

---

## PipelineResources
* A quick note on PipelineResources

---

## Workspaces
* What is a Workspace
* Types
* PVs and PVCs
* Using a PipelineRun for template

### Hands-On
* Create a read and write task
* Create a Pipeline that writes then reads from the Workspace (13.yaml)
* Create a PV/PVC to be used with the pipeline (14.yaml)
* Create a PipelineRun with a Workspace template (15.yaml)

### Exercise
* Create a pipeline that clones the git repo from https://github.com/joellord/tekton-lab-sample and outputs the content of sample.txt in a subsequent Task (16.yaml, 17.yaml)

---

## WhenExpressions
* A quick note about Conditions
* What is a WhenExpression

### Hands-On
* Create a greet task and a compliment task
* Create a pipeline that greets the person specified in the parameters and compliments depending on the name (18.yaml)

### Exercise
* Modify the last Pipeline to output a warning if the branch that is requested in the git clone task is `development` (19.yaml)

---

## Triggers
* Tekton Triggers
* OpenShift Pipelines Demo

---

## Putting it together
* Deploy an application using a Tekton Pipeline
  * Git Clone
  * Run npm test
  * Run npm lint
  * Push to registry