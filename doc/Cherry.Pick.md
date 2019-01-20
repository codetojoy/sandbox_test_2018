
### Background

* branches: `dev`, `stable`, `release-v-1-0`
* in `release-v-1-0`:
    * push build info for 1
    * tag build 1
    * push "late fix"
    * push build info for 2
    * tag build 2
* for example:

```
16847b3 v 1.0 build 2
739aae5 example fix
4d6e75c build info for V 1.0 build 1
``` 

### Cherry-Pick

* we want to apply commit `739aae5` to `dev` and `stable`
* steps:
    * `git checkout dev`
    * `git cherry-pick -n 739aae5` 
    * confirm with `git status`
    * `git commit -m "applying late fix"`
    * `git push origin dev`
* similarly for the `stable` branch



