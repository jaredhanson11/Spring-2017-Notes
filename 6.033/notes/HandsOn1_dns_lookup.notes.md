# Hands On 1: DNS

## Introduction

__dig__: command line tool for analyzing DNS of websisites

```
hansonj@mint-square:~$ dig wikipedia.org

;; ANSWER SECTION:
wikipedia.org.          572     IN      A       208.80.152.201
(name)                (expire) (class) (type)  (data (IP))
```
- type A: address reccrd
        - means wikipedia.org (name) is at 208.80.152.201 (IP)
- expire 572:
    - valid for 572 seconds
- ignore class, usually *IN* - (internet lookup)

```
hansonj@mint-square:~$ dig @hansonj.mit.edu wikipedia.org
```

- @hansonj.mit.edu
    - means check what the ip lookup is in `@server`'s DNS records
        - dns changes can take up to 48 hours to propogate, so two servers could
            have different DNS records
