<details><summary>How do I update my installation to the latest version?</summary>

The code is constantly being updated with new features and bug fixes. The process for updating will vary by the installation type:

- For a `pip` installation, when a new version is published: `pip install -U openbb[all]`
- Upgrade a cloned version of the GitHub repo with:

```console
git fetch
git pull
poetry install -E all
```

**Notes:** If the cloned repository is a fork, pull from: `git pull origin main`, or, `git pull origin develop`. If there are changes locally to the files that conflict with the incoming changes from GitHub, stash them before pulling from main with `git stash`.
</details>
