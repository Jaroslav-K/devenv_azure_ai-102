# ms-ai-102-lab-env #
This repository provides a Visual Studio Code development environment for Microsoft's AI-102: AI Engineer Lab course. It follows the instructions given in AI-102-AIEngineer setup - https://microsoftlearning.github.io/AI-102-AIEngineer/Instructions/00-setup.html.

## Motivation ##
During the AI-102 course, the lab environment sometimes took too long to start, causing delays or lags in completing modules.
Virtual sessions for these labs were terminated upon completing the lab, so I couldn't keep my changes or retrospectively review the code.

The docker setup makes the environment more portable and easy to install and manage all of the dependencies for Python/C# as well as Azure CLI.

## Usage ##
1. Clone the AI-102 Lab repository;
2. Add the `.devcontainer` directory to the root of the local repository;
3. Open the root directory of the local repository in VS Code and either
    a. Accept the suggestion to reopen in a container or
    b. Shift + Ctrl + P (Windows) / Shift + Cmd + P (macOS) and choose `Remote-Containers: Reopen in Container`.
4. Wait until the container is built (it takes longer the first time) and the project is reopen in the container;
5. In the exercises, instead of launching the lab, follow the exercise instructions.

## Caveats ##
- Not fully tested: problems are solved while using the environment; feel free to make pull requests or make changes;
- No PowerShell: although it can be added, I wanted to to keep the Docker image as small as possible and so, left it out. This means that CMD scripts won't run (I converted them to *nix shell scripts);
- Python instead of Miniconda: Azure CLI is not available as a distribution package for the ARM architecture (really,Microsoft? Making it hard for Raspberry Pi and macOS users...) and I couldn't use the install script provided by Microsoft with Miniconda. Hadn't have any problems, so far, in regard to Python usage.

## Acknowledgements ##
- Microsoft for the AI-102 course and the lab environment


