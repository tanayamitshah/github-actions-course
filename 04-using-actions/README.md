# Using Actions in Workflows

Actions are provided by GitHub and other third parties (from the GitHub Marketplace) but custom actions can also be used. Actions are used with `uses`. The use of actions instead of scripts avoid repetition and extensive commands. These actions can be configured via the `with` key-value pair.

This GitHub Actions workflow demonstrates how to use actions within our GitHub Actions workflow to test a React application.

## Workflow Details

- **Trigger**: This workflow is triggered manually from the UI.

- **Runner**: It runs on an Ubuntu environment provided by GitHub-hosted runners.

## Workflow Steps

1. **Checkout Code**: The workflow checks out the code from the repository using the `actions/checkout` action.

2. **Set up Node.js**: The `actions/setup-node` action sets up a Node.js environment with version 20.x. By specifying the `.x` option, we ensure that the latest release of the version 20 will be used.

3. **Install Dependencies**: It installs project dependencies using `npm ci`.

4. **Test**: It runs tests for the application using `npm run test`.

We use the `defaults` option in our `job` definition to define the common `working-directory` for the `run` commands executed from within steps. This default only applies to the `run` commands.
