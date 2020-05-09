---
title: single- vs double-quotes in unix commands
categories: ["unix"]
---

## what i learned
You can't insert variables in Unix commands if you're using single quotes. 

this won't work
```shell
export SECRET="huh"

echo 'you can not see my secret $secret'
```

but this will
```shell
export SECRET="huh"

echo "you can see my secret $SECRET"
```
