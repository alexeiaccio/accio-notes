---
title: 'Yarn Upgrade'
aliases: ['yarn-upgrade']
---

[[Yarn]]

> This worked for me:
>
> ```shell
> yarn global add npm-check-updates
>
> ncu -u
> ```
>
> got this list in the terminal:
>
> ![issue](https://camo.githubusercontent.com/c4f3a3c949fb38accb18849321425a69b3d59773/68747470733a2f2f692e696d6775722e636f6d2f356b334a3961492e706e67)
>
> Used yarn install with the --check-files flag:
>
> ```shell
> yarn install --check-files
>
> ncu -u
> ```
>
> ![result](https://camo.githubusercontent.com/a5ecb1350f96c9403e9956750e3e8cdb9125523e/68747470733a2f2f692e696d6775722e636f6d2f65426a5a666f622e706e67)
>
> Also if you want to upgrade only one package and have it reflect in the `package.json` this worked for me:
>
> ```shell
> yarn add lodash@latest
>
> or
>
> yarn add lodash@<version>
> ```
>
> Time to dance! :)
