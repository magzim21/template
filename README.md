# Repo template
This is a repo template 👨🏼‍🔬  
This README is a template for furure repos ➕ recommendations.  
The quality of a README description often differentiates a good project from a bad project.  

Add badges of your taste with [shields.io](https://shields.io/), [this collection](https://github.com/Ileriayo/markdown-badges), [this collection](https://ileriayo.github.io/markdown-badges/)  
![Hello World](https://img.shields.io/youtube/channel/subscribers/UCaBfu5WbxH97cJ38_KrSCfA?style=social)  
![Octopus Deploy](https://img.shields.io/badge/octopus%20deploy-0D80D8?style=for-the-badge&logo=octopusdeploy&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Ethereum](https://img.shields.io/badge/Ethereum-3C3C3D?style=for-the-badge&logo=Ethereum&logoColor=white)  
This may include CI test status, deployments status, security checks, dependecies info. Badges are fully customizable. Some badges does not work with private repos (depends on CI system).


Include a link to confluence not  to repeat yourslef (DRY).

## Getting started  
Usage:
![usage](https://public-bk-for-pics.s3.ca-central-1.amazonaws.com/git-template/CleanShot+2022-06-09+at+17.14.30.jpg)  

## Table of Contents (Optional)
*optional  
TODO

## Description
Short. 
What was your motivation?  
What problem does it solve?  
What application does?
Why you used the technologies you used?


### How to Install and Run the Project
optional

### Dependencies
Specify **dependencies to build** and **dependencies to deploy**.  
Reminder: explicitly declare and isolate dependencies


## Features
Consider following features for your furute repo:
- Make it good looking - [Markdown syntax](https://www.markdownguide.org/basic-syntax/). It is also possible to use HTML syntax when markdown does not support something (eg pictures aligning).
- Make it fun - use emoji 🥁
- To be demonstrative, use `.gif` instead of many screenshots. I use [CleanShot](https://cleanshot.com/) for this.
![gif example](https://public-bk-for-pics.s3.ca-central-1.amazonaws.com/git-template/CleanShot+2022-06-09+at+18.29.59.gif)
- Consider [enforcing](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches#require-signed-commits) on this repo [signed commits](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification)
![signed commits example](https://public-bk-for-pics.s3.ca-central-1.amazonaws.com/git-template/CleanShot+2022-06-09+at+17.39.02.jpg)
![how to enforce signing commits](https://public-bk-for-pics.s3.ca-central-1.amazonaws.com/git-template/CleanShot+2022-06-09+at+17.45.41.jpg)
- Protect **main** branch when collaborate
![protect branch](https://public-bk-for-pics.s3.ca-central-1.amazonaws.com/git-template/CleanShot+2022-06-09+at+17.49.55.jpg)
- Consider enabling [discussions](https://docs.github.com/en/discussions). Settings ➡️ Features ➡️ Discussions. Your community will be thankful for this nice channel to **discuss&collaborate**.
- Consider enabling [github wiki](https://docs.github.com/en/communities/documenting-your-project-with-wikis/about-wikis). It is made for development/contributors documentation. 
- Consider enabling [Github pages](https://pages.github.com/). Settings ➡️ Pages.  It is static website to **host user documentation**. Conventionally hosted on `gh-pages` branch.
    - Consider adding a [custom domain to Github Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain). Like this one [github.maxim.run](http://github.maxim.run/). It is just a `CNAME`.
- Create a logo for your project within 1 sec with this AI tool (namelix.com)[https://namelix.com/]. It generates a bunch of unique names from your keywords, makes stylish logos with corporate identities for each.


## Project status
I believe it is important.
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.


## Contributing
State if you are open to contributions and what your requirements are for accepting them.
### Branching strategy
Agree on your flow and follow it. Clean stale branches from time to time.  
Here are suggested flows:
- [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow) - `main` ➕ `feature` branches. Easy to start. Good for small teams. Remember to merge often!
- [GitLab flow](https://docs.gitlab.com/ee/topics/gitlab_flow.html) - `main` ➕ `development` or environment branches. Good for GitOps.
- [CI / Trunk Based Development](https://www.youtube.com/watch?v=v4Ijkq6Myfc) - only `main` branch. Good when you are just starting up, need to iterate quickly or you work mostly with senior developers. Do not use with open source.]
- [SimGit flow](https://levelup.gitconnected.com/better-git-branching-strategy-multi-apps-monorepos-and-multiple-teams-in-focus-cd17b56962f2) - a simplified version of [Legacy GitFlow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow). Good for BIG teams.  

### Releases
Releases must follow [semantic versioning](https://semver.org/lang/uk/)  
`{major}.{minor}.{patch}-{tag}+{buildmetadata}`
-   {major} is only incremented if the release has breaking changes (includes bug fixes which have breaking behavioural changes
-   {minor} is incremented if the release has new non-breaking features
-   {patch} is incremented if the release only contains non-breaking bug fixes
- `-{tag}+{buildmetadata}**` is optional
-   {tag} denotes a **pre-release** of the version preceding. Sorting happens in ASCII sort order. For example, A-Z comes before a-z.
-   {buildmetadata} contains additional information about the version, but **does not affect** the semantic version preceding it.
- Semantic Versioning is all **about  releases, not builds**.
- When you are ready to release, you simply run one of 
```bash
standard-version 
standard-version -- --prerelease alpha
standard-version --skip.bump --skip.commit --skip.tag
standard-version --dry-run 
```
`standard-version`  It intelligently determines which parts of semantic version `breaking.feature.fix` must be bumped based on latest commits. It generates changelog, commits this changelog file, adds tag `vx.x.x` to the new commit.
*It does not bump major version if base version is `v0.x.x`.  



### Commit messages style
Use the same formatting for commit messages like [conventional commits](https://www.conventionalcommits.org/) suggests. 
```txt
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```
Following this convention, CHANGELOG.md can be generated automatically.
Conventional commmits can be "enforced" with Husky. [Husky](https://typicode.github.io/husky/#/) is a tool for git hooks.     
Do `npx husky install` install githooks for this repo.  
`.husky/commit-msg` enforces commit messages to follow [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/).  
In this repo `.commitlintrc.yaml` is for this purpose.





## Licence
Choose your license
![Choose your license](https://public-bk-for-pics.s3.ca-central-1.amazonaws.com/git-template/CleanShot+2022-06-09+at+19.31.21.gif)

## Related projects
- [github bio generator](https://rahuldkjain.github.io/gh-profile-readme-generator/)
- [.gitignore file generator](https://www.toptal.com/developers/gitignore/)
- [semver comparsion operators](https://github.com/Masterminds/semver)

## Include Credits
A list with maintainers should be here. People you may relay on.  


Enjoy Coding ❤