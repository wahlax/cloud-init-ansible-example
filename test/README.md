Start vm, let provision, stop vm, enable experimental flags, start vm again. Cloud init must be installed before utilized.

```
vagrant up
vagrant halt
. cloud-init-env.shl
vagrant up
```
