# Create patchs file and apply patches

1. Create a patch file:
```
diff -u file.org file.new > change.patch
```

2. Apply a patch to update the content of a file:
```
patch filename < change.patch
```


3. Reverse applied patch:
```
patch -R filename < change.patch
```


4. Create a patch for whole directory:
```
diff -ruN OldDir NewDir > change.patch
```
Here:
	* -r -> scan all sub dirs
	* -u -> diff file in unified format
	* -N -> empty the absent files

5. Apply a patch:
```
patch -p0 < change.patch
```
Notes: change.patch in the same parent directory with the folder.
	* -p0 -> apply to the same folder name as created.
