# template-repo-for-workshops

This repo is meant to be a template for making workshop/demo repositories that anyone should immediately be able to replicate with binder/colab

## Badges

### [Binder](https://mybinder.org/)

Binder can spin up an environment with dependencies from [environment.yml](.binder/environment.yml) already present, and viewers can interact with this environment immediately with effectively no setup on their end.

You can create a badge like this to launch a binder environment for this repo

[![Binder Badge](.binder/badge_logo.svg)](https://mybinder.org/v2/gh/mlatsjsu/template-repo-for-workshops/HEAD)

This badge can be displayed in any markdown file or cell.

Binder can also use a `requirement.txt` with pip but I prefer to use conda/mamba environment.

Use the following command to generate the `environment.yml` file

```sh
conda env export --from-history -f environment.yml
or
mamba env export --from-history -f environment.yml
```

the `--from-history` tag will ensure only the main dependencies are listed and not the dependencies of the dependencies of the dep...........
