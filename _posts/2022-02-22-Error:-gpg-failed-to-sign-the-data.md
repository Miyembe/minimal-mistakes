---
title: "Git commit failed because of the gpg error""
excerpt: "Error: gpg failed to sign the data"
categories:
  - cod
tags:
  - git

---
The OS: Linux 20.04 

First of all, check if GPG configured and personal key with the command below:
```
gpg --list-keys
```

If you don't have key, please create a new one using the command below:
```
gpg --gen-key
```

It will ask you to type your mane and email.

After generation, you will see the result. 

```
pub   rsa3072 2021-11-04 [SC] [expires: 2023-11-04]
      4CFE07C1D4D72BD7E54A5C9081C1F8C53615D3CF
uid           [ultimate] zidan <email@eamil.com>
sub   rsa3072 2021-11-04 [E] [expires: 2023-11-04]
```

Using the string in the second line, you can modify git config using the following command.

```
git config --global user.signingkey 4CFE07....
```

Done! 

Source: https://www.dailytask.co/task/error-gpg-failed-to-sign-the-data-when-i-use-git-commit-ahmed-zidan
