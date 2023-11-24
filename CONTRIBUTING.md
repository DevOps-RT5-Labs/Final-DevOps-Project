# Contribution guidelines

## How to contribute

- Clone the repository
- Create a new branch from `develop` with the name of the ticket you're working on. (you can find the ticket name in the [project board](https://github.com/orgs/DevOps-RT5-Labs/projects/1)). Ticket names are in the format `identifier: description`. For example, `init-repo: Initiate the Repository and Block pushing to Main`. Branch names should be in the format `feature-*identifier*`.
- Commits **MUST** follow [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) format. You can use [this VSCode extension](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits) to help you with that.
  - For Conventionnal Commits scopes, here's a list of the ones that we use:
    - `app`: for the web application
    - `infra`: for the infrastructure (Terraform, Ansible, Kubernetes, etc.)
    - `build`: for the build system (Docker, etc.)
    - `ci`: for the CI/CD pipeline
    - `monitoring`: for the monitoring system
    - `docs`: for documentation
    - `qa`: for quality assurance (tests, etc.)
    - `misc`: for anything else
- Open a pull request from your branch to `develop` and assign it to the person who's responsible for reviewing it.