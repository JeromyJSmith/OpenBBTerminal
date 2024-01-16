---
title: Installation and Updates
sidebar_position: 1
description: This page provides detailed instructions for the installation and updating processes for software, addressing frequently encountered installation issues. These instructions include resolving the "Microsoft Visual C++ 14.0 or greater is required" error, benefits of using Miniconda for package management, methods to update installations, and solutions for other common installation errors.
keywords:
- Installation
- Updates
- Microsoft Visual C++ 14.0
- Miniconda
- pip install
- PyPi Nightly
- C++ Build Tools
- Homebrew
- bt wheel build failure
- ARM/Linux Raspberry Pi machines
---

import HeadTitle from '@site/src/components/General/HeadTitle.tsx';

<HeadTitle title="Installation and Updates - Faqs | OpenBB SDK Docs" />

<details><summary>"Microsoft Visual C++ 14.0 or greater is required"</summary>

Download and install [C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/) from the official Microsoft website. After installation, restart your machine and then try the installation again.

</details>

<details><summary>Do I have to use Miniconda?</summary>

Miniconda is a lightweight package manager that allows for effortless management of Python environments. It is recommended for installing the OpenBB SDK due to its flexibility and ease of use.

</details>

<details><summary>How do I update my installation to the latest version?</summary>

The code is constantly being updated with new features and bug fixes. The process for updating will vary depending on the installation type:

- For a `pip` installation, when a new version is published, run the following command: `pip install -U openbb[all]` to update to the latest version.
- If you have cloned the GitHub repository, you can upgrade it to the latest version by running the following commands:
  ```
  git fetch
  git pull
  poetry update && git merge main && poetry install -E all
  ```
  Note: If the cloned repository is a fork, pull from `git pull origin main` or `git pull origin develop`. If there are local changes that conflict with the incoming changes from GitHub, stash them before pulling from main using `git stash`.

</details>

### PyPi Nightly

To install the nightly build, follow these steps:

```
pip install openbb-terminal-nightly[all]
```

Note: The nightly version may not be stable and should not be used in a production setting.

<details><summary>"Microsoft Visual C++ 14.0 or greater is required"</summary>

Download and install [C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/) from the official Microsoft website. After installation, restart your machine and then try the installation again.

</details>

<details><summary>Error: failed building wheel for bt and detailed Homebrew installation steps for Mac and Linux users</summary>

There may be an additional message that is printed from this error, stating: "Microsoft Visual C++ 14.0 or greater is required. Get it with "Microsoft C++ Build Tools".

To resolve this error:
- Download and install [C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/) from the official Microsoft website.
- Restart your machine.
- For Mac and Linux users, if a C++ compiler is not installed, install Homebrew by running the following command:
  ```
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
  Then run:
  ```
  brew install gcc
  brew install cmake
  ```
- Additionally, Mac users should install Rosetta by running the following command:
  ```
  softwareupdate --install-rosetta
  ```

</details>

<details><summary>Miniconda3 installation on ARM/Linux Raspberry Pi machines

Refer to this issue on the [Conda GitHub page](https://github.com/conda/conda/issues/10723) for more information.

</details>

<details><summary>Error: Library not loaded: '/usr/local/opt/libomp/lib/libomp.dylib'</summary>

To resolve this error, first ensure that Homebrew is installed by running the following command:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
After installing Homebrew, run the following command to install libomp:
```
brew install libomp
``
```
brew install libomp
```

</details>
