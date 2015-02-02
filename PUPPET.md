# Test puppet change without pulling the change 
## run with root
```bash
/opt/bin/./puppet agent --test --noop
```

# get puppet variable usage
```bash
/opt/puppet/bin/facter
```

# direct test small changes on puppet server
```bash
/etc/puppet/modules
```
# Certificate
```
puppet ca sign hostname-of-agent
```
## Location of CA
```
/path_puppet/puppet/ssl/ca/signed
```
