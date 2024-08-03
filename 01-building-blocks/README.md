# Section 1 - Building Blocks

## GitHub Actions Workflows, Jobs, and Steps

GitHub Actions is a powerful automation tool that allows you to build, test, and deploy your code right from your GitHub repository. Understanding the key building blocks — workflows, jobs, and steps — is essential for effective automation.

### Workflows

A workflow is a customizable, automated process that you can define in your repository. Workflows are defined at the repository level. It's typically used for continuous integration (CI), continuous deployment (CD), and other automation tasks. Here are the important aspects of workflows:

- **Trigger**: Workflows are triggered by specific events, such as pushes, pull requests, or scheduled events. You define when and how a workflow runs. See the [triggering-workflows](../02-workflow-events/README.md) folder for more information about triggering workflows.

- **YAML Configuration**: Workflows are defined in a YAML file (e.g., `.github/workflows/main.yml`) within your repository. It is required that the workflows are in the `.github/workflows` directory. This configuration file specifies the workflow's name, triggers, jobs, and steps.

### Jobs

A job is a unit of work within a workflow i.e. they are defined at the workflow level. You can have multiple jobs in a workflow, and they can run in parallel or sequentially. Here are the key points about jobs:

- **Runs-On**: Each job specifies the runner environment, such as Ubuntu, macOS, or Windows. You choose the environment that best suits your workflow.

- **Parallelism**: You can configure jobs to run concurrently, which can speed up your workflow's execution time.

### Steps

A step is an individual task within a job. Steps are the smallest building blocks of a workflow and are where the actual work happens. If a step in a job fails (non-zero exit code), subsequent steps in the job will not run. Here are the important aspects of steps:

- **Name**: Each step has a name that helps identify its purpose. It appears in the GitHub Actions log to provide clarity during execution.

- **Run Commands**: Steps execute commands or scripts. These can include shell commands, script files, or even invoking actions from external sources (GitHub Marketplace, your own custom actions, etc.). For multiline run commands, use the YAML literal block style which is indicated by a pipe i.e. `|` which will preserve new lines.

- **Inputs and Outputs**: Steps can have inputs and produce outputs, allowing them to communicate and share data with other steps.

## Visual Studio Code Extension

The GitHub Actions extension lets you manage your workflows, view the workflow run history, and helps with authoring workflows.

## Exercise

See `.github/workflows/01-building-blocks.yaml`.
