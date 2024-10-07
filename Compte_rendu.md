# clonage d'un repo github
## git clone https://github.com/gaetanjoannic/test.git
Cloning into 'test'...
warning: You appear to have cloned an empty repository.

# liste des changements
## git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test/

nothing added to commit but untracked files present (use "git add" to track)

# ajout d'un fichier
## git add HELLO.txt

# commit l'ajout du fichier
## git commit -a
[master (root-commit) 7e7eb05] nouveau fichier
 1 file changed, 1 insertion(+)
 create mode 100644 HELLO.txt

# commit d'une modification
## git commit -a
[master fc503bf] ajout de txt
 1 file changed, 2 insertions(+), 1 deletion(-)

# envoie des modifications 
## git push --set-upstream https://github.com/gaetanjoannic/test.git master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (6/6), 468 bytes | 21.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/gaetanjoannic/test.git
 * [new branch]      master -> master
 branch 'master' set up to track 'https://github.com/gaetanjoannic/test.git/master'.

 # commit d'une erreur
 ## git commit -a 
 [master 25c5859] introduction d'une erreure
 1 file changed, 2 insertions(+), 1 deletion(-)

 # affichage des logs
 ## git log
 commit 25c585929bef8c4d291acf7031d013e8029f319f (HEAD -> master)
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:28:33 2024 +0200

    introduction d'une erreure

commit fc503bf33faf243544edeecfd2efe6f754156b0e
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:21:07 2024 +0200

    ajout de txt

commit 7e7eb052b75b3ed89ea4e8518c7817530fad3e7a
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:19:08 2024 +0200

    nouveau fichier
    ...skipping...
Date:   Mon Oct 7 11:21:07 2024 +0200

    ajout de txt

commit 7e7eb052b75b3ed89ea4e8518c7817530fad3e7a
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:19:08 2024 +0200

    nouveau fichier
    ...skipping...
commit fc503bf33faf243544edeecfd2efe6f754156b0e
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Author: gaetanjoannic <gaejoannic@hotmail.fr>
commit fc503bf33faf243544edeecfd2efe6f754156b0e
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:21:07 2024 +0200

    ajout de txt

commit 7e7eb052b75b3ed89ea4e8518c7817530fad3e7a
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:19:08 2024 +0200

    nouveau fichier
...skipping...
Date:   Mon Oct 7 11:21:07 2024 +0200

    ajout de txt

commit 7e7eb052b75b3ed89ea4e8518c7817530fad3e7a
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:19:08 2024 +0200

    nouveau fichier
...skipping...
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:21:07 2024 +0200

    ajout de txt

commit 7e7eb052b75b3ed89ea4e8518c7817530fad3e7a
Author: gaetanjoannic <gaejoannic@hotmail.fr>
Date:   Mon Oct 7 11:19:08 2024 +0200

    nouveau fichier

# correction du message d'erreur
## git commit --amend
[master feb4ee1] introduction d'une erreure
 Date: Mon Oct 7 11:28:33 2024 +0200
 1 file changed, 2 insertions(+), 1 deletion(-)

 # annulation du dernier commit (soft)
 ## git reset HEAD^
 Unstaged changes after reset:
M       HELLO.txt

# annulation du dernier commit (hard)
## git reset --hard HEAD^
HEAD is now at 7e7eb05 nouveau fichier

# récupération des changements fait sur github
## git pull
From https://github.com/gaetanjoannic/test
 * branch            master     -> FETCH_HEAD
Updating 7e7eb05..d6bbda5
Fast-forward
 HELLO.txt | 3 ++-
 oui.txt   | 1 +
 2 files changed, 3 insertions(+), 1 deletion(-)
 create mode 100644 oui.txt

 # commit de la fusion
 ## git commit -a
 [master 75de055] modification d'une ligne
 1 file changed, 2 insertions(+), 1 deletion(-)
 
# listage des branches
## git branch
* master

# création d'une nouvelle branche
## git branch uneidee

# passage sur la branche nouvellement créée
## git checkout uneidee
Switched to branch 'uneidee'

# suppression de la branch
## git -D uneidee
Deleted branch uneidee (was 1c1b041).

# création d'un tag
## git tag v1.0

# envoie du tag au serveur
## git push --tags
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 544 bytes | 68.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/gaetanjoannic/test.git
 * [new tag]         v1.0 -> v1.0

 # supression du tag
 ## git tag -d v1.0
 Deleted tag 'v1.0' (was 1c1b041)