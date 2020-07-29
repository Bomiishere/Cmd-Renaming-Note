# Command Line Renaming 

## install rename cmd

```
brew install rename
```

### Usage

#### Replace
```rename 's/sl_/softlipa_/' *.extension```

#### Delete
```rename 's/sl_//' *.extension```

#### Find start of string
```rename 's/^sl_/softlipa_/' *.extension```

#### Find end of string
```rename 's/$size_XL/size_L/' *.extension```

#### Group
```rename 's/(sl|slp)_/softlipa_/' *.extension```

#### Lower / Upper case (?)
```rename ‘y/A-Z/a-z/’ *.extension```
ps.this will failed, use below cmd first
```
for f in *; do mv "$f" "$f.tmp"; mv "$f.tmp" "`echo $f | tr "[:upper:]" "[:lower:]"`"; done
```


#### ref
[1. https://www.howtogeek.com/423214/how-to-use-the-rename-command-on-linux/)](https://www.howtogeek.com/423214/how-to-use-the-rename-command-on-linux/)
