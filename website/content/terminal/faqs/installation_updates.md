---
title: Installation and Updates
sidebar_position: 1
description: This page provides comprehensive insights about installing and updating
  the OpenBB Terminal. It discusses system requirements, installation process, common
  errors and their solutions. Information about updating the OpenBB Terminal through
  different methods is also covered.
keywords:
- OpenBB Terminal installation
- Updating OpenBB Terminal
- System requirements for OpenBB Terminal
- Installation errors with OpenBB Terminal
- Python pip installation
- Microsoft Visual C++
- Homebrew installation
- libomp
- Conda installation issue
---

import HeadTitle from '@site/src/components/General/HeadTitle.tsx';

<HeadTitle title="Installation and Updates - Faqs | OpenBB Terminal Docs" />

## Installation and Updates

<details><summary>How much hard drive space is required?</summary>

An installation will use approximately 4-5 GB of space, with additional storage required for optional machine learning models.

</details>

<details><summary>What is the minimum version of Windows or MacOS required to install the OpenBB Terminal?</summary>

The OpenBB Terminal installation packages are compatible with:

- Windows 10 or later.
- MacOS Monterey or later.

**Note:** Machines which are not compatible with the installer packages may be able to install from the source code.

</details>

<details><summary>How do I update my installation to the latest version?</summary>

The terminal is constantly being updated with new features and bug fixes. The process for updating will vary by the installation type:

- For the Windows installer, uninstall the existing version before updating.
- For other installation types, uninstall the previous version and reinstall the latest version. Any user settings and data will remain.
- For a `poetry` installation, when a new version is published: `poetry update openbb-terminal`
- Upgrade a cloned version of the GitHub repo with:

```console
git fetch
git pull
poetry update openbb-terminal
```

**Notes:** If the cloned repository is a fork, pull from: `git pull origin main` or `git pull origin develop`. If there are changes locally to the files that conflict with the incoming changes from GitHub, stash them before pulling from main with `git stash`.

</details>

### PyPi Nightly

To install the nightly build, use the following command:

```console
pip install openbb-terminal-nightly[all]
```

**Note**: This version may not be stable and should not be used in a production setting.

<details><summary>"Microsoft Visual C++ 14.0 or greater is required"</summary>

Download and install [C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/), restart the machine, then try again.

![image](https://github.com/OpenBB-finance/OpenBBTerminal/assets/85772166/ceb57be0-6dae-42f2-aca6-bf62ce7d6135)

![image](https://github.com/OpenBB-finance/OpenBBTerminal/assets/85772166/f8aef8fc-a080-4164-bd36-460714ec44f3)

</details>

<details><summary>If you encounter the following error, take the following steps to address it:</summary>

There may be an additional message that is printed from this error, stating: "Microsoft Visual C++ 14.0 or greater is required. Get it with "Microsoft C++ Build Tools".

Download and install it. [https://visualstudio.microsoft.com/visual-cpp-build-tools/](https://visualstudio.microsoft.com/visual-cpp-build-tools/)

Mac and Linux users may also encounter a similar error because a C++ compiler is not installed. Install Homebrew:

```console
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Then run:

```console
brew install gcc
brew install cmake
```

</details>

<details><summary>Miniconda3 will not install on ARM/Linux Raspberry Pi machines.</summary>

Refer to this issue on the Conda [GitHub](https://github.com/conda/conda/issues/10723) page.

</details>

<details><summary>To handle this error, follow these steps to resolve the issue:</summary>

To resolve this error, follow these steps:

To handle this error, follow these steps to resolve the issue:

```console
brew install libomp
```

</details>
