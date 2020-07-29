# Command Line Renaming 

## install rename cmd

```
brew install rename
```

### Usage

- replace
rename 's/sl_/softlipa_/' *.extension

- delete
rename 's/sl_//' *.extension

- find starts of string
rename 's/^sl_/softlipa_/' *.extension

- find end of string
rename 's/$size_XL/size_L/' *.extension

- group
rename 's/(sl|slp)_/softlipa_/' *.extension

- lower/upper case (?)
rename ‘y/A-Z/a-z/’ *.extension
ps.this will failed, use below cmd first
```
for f in *; do mv "$f" "$f.tmp"; mv "$f.tmp" "`echo $f | tr "[:upper:]" "[:lower:]"`"; done
```


#### ref
`
https://www.howtogeek.com/423214/how-to-use-the-rename-command-on-linux/
`
