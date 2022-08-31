# workflows

_A collection of workflows I use in my repos_

## Usage

1. Make sure reusable repos are enabled in your repository: `REPO/settings/actions` -> Actions permissions
2. Create a new workflow: you can either use one from the `dependents` directory in this repo or create your own

```yml
# .github/workflows/NAME.yml

name: Your reused workflow
on:
  # ...

jobs:
  workflow:
    # This is the path to the workflow file you want to re-use
    uses: EndBug/workflows/.github/workflows/FILE.yml@main
    with: 
      # ...
```

All workflow files are in the [`.github/workflows`](https://github.com/EndBug/workflows/tree/main/.github/workflows) directory of this repo.  

For more info regarding reusable workflows, see [GitHub's docs](https://docs.github.com/en/actions/using-workflows/reusing-workflows).
