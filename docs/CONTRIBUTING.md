Contributing to Fand
===========

**English** | [中文](https://github.com/FandMC/Fand/blob/master/docs/CONTRIBUTING_cn.md)

We're glad that you want to contribute to our project!  
In general, our review of pull requests is very lenient.  
And if you can follow the rules below, we can complete the review faster.

## Please fork using your personal account

We regularly merge existing PRs.  
If there're some small problems, we'll help you solve them by editing your PR.

But, if your PR is from a organization, we can NOT edit your PR, so we must merge your PR manually.

So, don't use orgnization accounts for fork!

See also [This issue](https://github.com/isaacs/github/issues/1681), and then you'll know why we can't edit PRs from organizations.

## Development Environment

Before coding, you need these softwares / tools as Dev Environment.

- `git`
- `JDK 17 or higher`
  - We used Gradle's toolchains, so you can build Fand using JRE 8. (When Gradle can't find JDK 17, it will download it automatically.)

If you're using Windows Operating System, you can use `WSL` to speed up building.

## Understanding "Patches"

Fand uses as the same patching system as Paper,  
and has been divided into two directories for the purpose of modifying different parts of it:

- `Fand-api` - Modifications to `Leaves-API` / `Paper-API` / `Spigot-API` / `Bukkit`.
- `Fand-server` - Modifications to `Leaves-API` / `Paper`/ `Spigot` / `CraftBukkit`.

The patching system is based on git, and you can learn about it at here: <https://git-scm.com/docs/gittutorial>

If you have forked the main repository, then you should follow the steps below:

1. Clone your repository to local
2. Run Gradle's `applyPatches` task in your IDE or terminal (You can run `./gradlew applyPatches` directly in terminal.)
3. Enter `Fand-api` or `Fand-server` directory to carry out modifications.

BTW, `Fand-api` and `Fand-server` are not normal git repositories.

- Before applying patches, the base will point to unmodified source code.
- Every commit after the base is a patch.
- Only commits after the last commit of Paper will be considered Fand' patches.

## Adding new patches

It's very easy to to add patches by following the steps below:

1. Modify the code of `Fand-api` and / or `Fand-server`
2. Add these changes to the local git repository (For example, `git add .`)
3. Commit these changes using `git commit -m <Commit Message>`
4. Run Gradle's task `rebuildPatches` to convert your commits to a new patch
5. Push your patches to your repository

After pushing, you can open a PR to submit your patches.

## Modifying patches

You can modify a existing patch by following the steps below:

1. Modify code at HEAD
2. Run `git commit -a --fixup <hash>` in your terminal to make a fix-up commit
    - If you want to edit the commit message, replace `--fixup` with `--squash`.
3. Run `git rebase -i --autosquash base` to rebase automatically, then just type `:q` to close the confirm page
4. Run Gradle's task `rebuildPatches` to modify existing patches
5. Push and PR again
