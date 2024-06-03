+++
title = 'Uonwifi'
date = 2024-06-03T13:08:07Z
draft = true
+++


Using Python

# Curl Command
```
curl http://gstatic.com/generate_204
```
# Curl Output
```
curl http://gstatic.com/generate_204
<html><body><script language="JavaScript">window.location="https://portal.uonbi.ac.ke:1003/fgtauth?0315ca8bcb35b214";</script></body></html>[merlin@archlinux scripts]$ 
```

# 1.Step One:
    - extract the magic of which in this case is `0315ca8bcb35b214` from the url in the curl output `https://portal.uonbi.ac.ke:1003/fgtauth?0315ca8bcb35b214`
    - set the variable name to magic
    - set another variable my_referer to the base usr including the port of which in this case is `https://portal.uonbi.ac.ke:1003`


# Draft Solutions

- ### Solution 1

Pipe the curl output straight to python

```
curl http://gstatic.com/generate_204 | python3 extract_variables.py
```


