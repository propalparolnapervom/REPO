# README

## DOCS

[General info](https://githooks.com/)

## OVERALL

The hooks templates folder will be chosen by the following precedence:

    - The argument given with the `--template` option.
    - The value of the `$GIT_TEMPLATE_DIR`.
    - The `init.templatedir` git configuration variable.
    - The default templates directory (`/usr/share/git-core/templates/` on Linux).

## DEFINE GIT HOOK (OPTION 1)

    1. Put dir with your execution files (`pre-commit`, etc) to the root of your git repo. Let it be `.githooks`, for example.
    2. Put `Makefile` on the same level where `.githooks` dir (which is root of the git repo).
    3. Add, for example, following definition:

```
init:
	git config core.hooksPath .githooks
```
    4. Do `make init` every time you pull git repo. Thus it will define where to find hooks for git (as it defines `git config` for the repo).