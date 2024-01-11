---
title: tr
documentation on how to troubleshoot and fix errors in the installation, including steps to identify and resolve common issues that may cause the run to fail. This includes: 
1. Check the installation file for syntax errors, typos, and required fields. Verify that the YAML syntax is correct and all necessary fields are properly configured in the installation file.
2. Review the log output for error messages that provide clues about the cause of the failure. Search for specific error codes or messages that can be researched to identify the cause of the failure.
3. Verify that the required environment variables and secrets are properly configured. Ensure that they are accessible and correctly set up in the GitHub repository settings to avoid issues with environment variable and secret accessibility.
4. Double-check the dependencies and versions used in the installation. Ensure that the correct versions of tools, packages, and libraries are being used to prevent issues related to dependencies and versions.
5. Test the installation locally to replicate the environment and debug the run. This can help identify issues that may be specific to the environment and assist in debugging the installation.
6. If the error is related to external services or dependencies, verify the availability and connectivity of external services such as package registries and API endpoints to resolve issues related to external dependencies.
7. Reach out to the maintainers or community for support if the issue is not resolved. Provide detailed information about the failure and the troubleshooting steps taken so far.
<br>Documentation on how to display top repositories using the GitHub API.
  Instructions include usage, parameters details, and examples. The user can sort
  the repos by stars or forks, and can filter by repo categories.
keywords:
- top repositories
- github api
- parameters
- stars
- forks
- repo categories
- filter
- sort
- usage
---

import HeadTitle from '@site/src/components/General/HeadTitle.tsx';

<HeadTitle title="alt/oss/tr - Reference | OpenBB Terminal Docs" />

Troubleshooting and Fixing GitHub Actions Run Errors [Source: https://api.github.com]

### Usage

```bash
tr [-s {stars,forks}] [-c CATEGORIES]
```

#### Parameters
- `[-s {stars,forks}]`: Sort repositories by stars or forks.
- `[-c CATEGORIES]`: Filter repositories by categories. If more than one, separate with a comma, e.g., finance,investment.

#### Examples
```bash
curl https://api.github.com/repos | tr -s stars -c finance,investment
```

---

Installation and Troubleshooting Steps

| Name | Description | Default | Optional | Choices |
| ---- | ----------- | ------- | -------- | ------- |
| sortby | Sort repos by {stars, forks}. Default: stars | stars | True | stars, forks |
| categories | Filter by repo categories. If more than one separate with a comma: e.g., finance,investment |  | True | None |

![cases](https://user-images.githubusercontent.com/46355364/153897646-99e4f73f-be61-4ed7-a31d-58e8695e7c50.png)

---
