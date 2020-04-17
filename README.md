# Handling Git Merge Conflicts


####Merge Conflicts Happen.  

Here is a quick and simple resolution that will have you on your way in seconds . . . provided that you know what the merge conflict is and how it should be resolved.

If you know that your local changes are the ones that you want to keep -- and this applies to __*all*__ files then  simply use --ours 

```
git checkout . --ours
```

Likewise, if you want to overwrite __*all*__ local files with the remote ones use --theirs

```
git checkout . --theirs
```


In the case where th are just one or a few files in question, and you might want to mix and match which ones you want to work with, you can adapt the commands. 

To keep your version of a file

```
git checkout --ours -- <filename>
git add <filename>
git commit -m "resovled merge conflict for <filename>"
```

To keep their version of a file

```
git checkout --theirs -- <filename>
git add <filename>
git commit -m "resovled merge conflict for <filename>"
```
