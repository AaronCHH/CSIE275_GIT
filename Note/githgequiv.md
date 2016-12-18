## Hg .hgignore, syntax: glob is the same behaviour as git's .gitignore.  

Git .git/config, ~/.gitconfig, use git-config to modify the values  
Hg .hg/hgrc, ~/.hgrc, use hg help -c config  

Git git commit -v  
Hg hg diff | less; hg commit  

Git gitk  
Hg hg view, or thg from TortoiseHg  

Git git gui  
Hg Mercurial doesn't ship GUI to select changesets, only console hg record command.  

Git git rebase  
Hg hg rebase. For git rebase --interactive there's hg histedit, or Mercurial Queues  

Git git push URL ; git remote add origin URL  
Hg hg push URL; $EDITOR .hg/hgrc ; [paths] default = URL  

Git gitk, git log origin/master..HEAD  
Hg hg outgoing  

Git git format-patch RANGE  
Hg hg email -m filename -o  

Git git add . ; Note the dot  
Hg hg add ; No dot needed.  

Git git checkout REVISION-KEY  
Hg hg update CHANGESET  


## Just to fill the blanks, some of the most useful commands from Mercurial:  

Hg hg record  
Git git add -p; git commit  

Hg hg inc [URL]  
Git No real equivalent. You can only do equivalent of hg pull; hg log -r .:  

Hg hg out URL  
Git Please add if you know how.  

## For merge conflict resolution, the hg resolve command in Mercurial has a few options that change the behaviour:  

Hg hg resolve -m FILE (marks the file as having been resolved by manually fixing up the conflict problem)  
Git git add FILE  

Hg hg resolve -u FILE marks the file as having been unresolved  
Git git reset HEAD FILE to unstage the file  

Hg hg resolve -l (lists files with resolved/unresolved conflicts)  
Git git status - files that merged cleanly are added to the index automatically, those that are not have conflicts  

Hg hg resolve FILE (after a merge, attempts to re-merge the file)  
Git no equivalent for re-merging that I know of.  

## Source
* http://stackoverflow.com/questions/1450348/git-equivalents-of-most-common-mercurial-commands  
