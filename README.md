# Automated-Commit

This repository contains a GitHub Actions workflow that automatically updates a file named `TIMESTAMP.txt` with the current date and time every 12 hours. This README provides a detailed overview of how the workflow operates and guides you through customizing and using it, especially if you're new to GitHub or GitHub Actions.

## Overview

The `Automated-Commit` workflow demonstrates the capabilities of GitHub Actions for automating routine tasks within a repository. Specifically, this workflow:

- Checks out the latest code from the `master` branch.
- Updates the `TIMESTAMP.txt` file with the current date and time.
- Commits the change to the repository if any modifications are detected.
- Pushes the changes back to the `master` branch.

## Workflow Structure

The workflow is defined in the `.github/workflows/master.yml` file and includes:

- **Triggers**: Configured to run every 12 hours and can be manually triggered via the GitHub UI with the `workflow_dispatch` event.
- **Jobs and Steps**: Contains a job `update_commit` that runs on the latest Ubuntu runner, performing tasks such as setting up Git, updating `TIMESTAMP.txt`, and committing and pushing changes.
- **Permissions**: Granted write permissions to the repository contents.

## Using This Workflow

### Creating Your Own Version

To create your own version of this repository and workflow:

1. Click the "Use this template" button on the GitHub repository page.
2. Choose a name for your new repository and select "Create repository from template".
3. Clone your new repository to make further customizations locally.

### Customizing the Workflow

Before using the workflow, you'll need to customize it with your GitHub user email and name:

1. Navigate to the `.github/workflows/master.yml` file in your repository.
2. Edit the file, replacing `"rxmxdhxni@gmail.com"` with your email and `"dante4rt"` with your GitHub username in the `Setup Git Configuration` step.
3. Commit your changes.

### Viewing Workflow Runs

To view the history of workflow runs:

1. Navigate to the `Actions` tab of your repository.
2. Select the `Automated-Commit` workflow to see details of each run.

### Manually Triggering the Workflow

You can manually trigger the workflow:

1. Go to the `Actions` tab of your repository.
2. Select the `Automated-Commit` workflow.
3. Click `Run workflow`, select `master`, and click `Run workflow` again.

## Contributing

Contributions are welcome! Feel free to fork the repository, make your changes, and submit a pull request.

## Support

For issues or questions, please file an issue in the `Issues` section of the repository.

Thank you for exploring the Automated-Commit workflow!
