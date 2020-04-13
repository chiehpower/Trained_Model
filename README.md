# Trained Model

This repositroy mainly put some pretrained model for other repositories use.
In order to upload the model which size is over 100MB, I used the `Git Large File Storage (LFS)` to upload large files on GitHub.

---
# Instruction

Please follow the official [Website](https://git-lfs.github.com./) to install git lfs first. 

---
## Commands:

1. put your file to the destination folder. 
   For example:
   ```
   ~\Trained_Model\model.onnx
   ```
2. Use the track to add this file into `.gitattributes`
   ```
   git lfs track "(filename)"
   ```
    Such as `git lfs track "~\Trained_Model\model.onnx"`
3. Add the `.gitattributes` to git.
   ```
   git add .gitattributes
   ```
   For example:
   ```
   git add ~\Trained_Model\.gitattributes
   ```
4. Add your file to git.
   For example:
   ```
   git add ~\Trained_Model\model.onnx
   ```
5. Commit it and push on GitHub.
   ```
   git commit -m "Add model" && git push origin master
   ```

If you want to check the tracking files of lfs.
```
git lfs ls-files
```

---
# Add git submodule 
For example, I want to add this repository, `https://github.com/chiehpower/Installation`.

1. `git submodule add https://github.com/chiehpower/Installation`
   or `git submodule add https://github.com/chiehpower/Installation Installation` (Last one is local folder name.)

2. Check `git status` and `git add`.
3. `git submodule init` in order to let git know you adding the submodule.

Done.

*You can check in the root folder where there is a file, `.gitmodules`.*

---
# Reference

- [Git LFS Tutorial](https://github.com/git-lfs/git-lfs/wiki/Tutorial)