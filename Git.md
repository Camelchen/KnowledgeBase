#### Cheatsheet
* remove untracked files and folders :  **git clean -d -f**, [d=directories; f=force]
* checkout new remote branch : **git switch -c %branch_name% %remote_branch_name%**, [c=create]
* remove file from history: **git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch %path_to_file%" HEAD**
  ** the path is case sensitive
  ** after remove, may need remove backup branch: **git update-ref -d refs/original/refs/heads/master**

