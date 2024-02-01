---
title: Installation
---

## Prerequisites

Before installing the OpenBB SDK, ensure that you have the following prerequisites:

- Python 3.11 or higher
- Pip package manager

## Updating the Package Manager

To ensure that the package manager is up to date, run the following command:

```console
pip install --upgrade pip
```

## Creating and Activating a New Environment

It is recommended to create a new environment before installing the OpenBB SDK. This helps to isolate the SDK and its dependencies from other Python packages on your system. Follow these steps to create and activate a new environment:

1. Open a terminal or command prompt.
2. Run the following command to create a new environment named "openbb-env":

   ```console
   conda create -n openbb-env python=3.11
   ```

   This will create a new environment with Python 3.11 installed.

3. Activate the new environment by running the following command:

   ```console
   conda activate openbb-env
   ```

   This will activate the "openbb-env" environment.

## Installing the OpenBB SDK

To install the latest version of the OpenBB SDK, run the following command:

```console
pip install --upgrade openbb
```

This will install the core OpenBB SDK.

If you want to install additional extensions and providers, you can use the following commands:

- To install all extensions and providers (both officially supported and community maintained ones):

  ```console
  pip install --upgrade openbb[all]
  ```

- To install a specific extension, replace `<extension_name>` with the desired extension name:

  ```console
  pip install --upgrade openbb[<extension_name>]
  ```

- To install a specific provider, replace `<provider_name>` with the desired provider name:

  ```console
  pip install --upgrade openbb[<provider_name>]
  ```

After installing the OpenBB SDK, you can import it in your Python code using the following statement:

```python
import openbb
```

Make sure to import the necessary modules and functions from the SDK for your specific use case.

## Post-Installation

After a fresh installation or when installing/uninstalling extensions, it is recommended to rebuild the Python interface. This can be done automatically, but you can also trigger it manually if needed. Start a Python session and import the OpenBB SDK:

```python
import openbb

# Manually trigger the build
openbb.build()
```

Restart the Python interpreter and you can start using the OpenBB SDK.

## Documentation

For more detailed information and examples on using the OpenBB SDK, refer to the [official documentation](https://openbb-finance.github.io/OpenBBTerminal/).
