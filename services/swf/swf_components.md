- Workflow: A sequence of steps required to perform a specific task. It is also commonly referred to as a decider.
- Activities: A single step in the workflow.
- Tasks: That interacts with the workers that are part of the workflow.
  - Activity task: Tells the worker to perform a function
  - Decision task: Tells the decider the state of the workflow execution, which allows the decider to determine the next activity to be performed.
- Worker: Responsible for receiving a task and taking action on it. Can be any type of component such as an EC2 instance, or even a person.