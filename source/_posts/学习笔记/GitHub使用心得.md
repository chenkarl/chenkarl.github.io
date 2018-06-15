---
title: GitHub使用心得
date: 2017-10-27 22:28:41
tags:
---
```

npm ERR! fatal: 'submodule' appears to be a git command, but we were not
npm ERR! able to execute it. Maybe git-submodule is broken?

```

尝试执行以下命令
'git submodule update --init --recursive'
git版本在2.9以下的，应该是不可以的，可以更新到2.17以上版本就可以解决该问题。 