
https://medium.com/@marcosantonocito/fixing-the-gh001-large-files-detected-you-may-want-to-try-git-large-file-storage-43336b983272

Error occured in local of window when push to code

remote: Resolving deltas: 100% (43/43), done. <br /><br />
remote: error: GH001: Large files detected. You may want to try Git Large File Storage - https://git-lfs.github.com. <br /><br />
remote: error: Trace: ed6fa5ff6faac7a72e1d77e38ca5417a2ef111167d49cda0cd3a90c7c0c21663 <br /><br />
remote: error: See http://git.io/iEPt8g for more information. <br /><br />
remote: error: File **croc-stdin-738110029** is 392.36 MB; this exceeds GitHub's file size limit of 100.00 MB
To https://github.com/RahulPhpDev/online_shop.git <br /><br />



put this command
 git filter-branch -f --index-filter 'git rm --cached --ignore-unmatch **croc-stdin-738110029**' <br /><br />
 reponse and wait--
 WARNING: git-filter-branch has a glut of gotchas generating mangled history
         rewrites.  Hit Ctrl-C before proceeding to abort, then use an
         alternative filtering tool such as 'git filter-repo'
         (https://github.com/newren/git-filter-repo/) instead.  See the
         filter-branch manual page for more details; to squelch this warning,
         set FILTER_BRANCH_SQUELCH_WARNING=1.


