---
layout: post
slug: Catatan G1T, SMK Kelas 10
---

untuk materi sekolah yang update, sangat melelahkan dan membingungkan, apalagi saya nge-game mulu, mana sempat, keburu telat.

ditulis untuk bapak guru saya tercinta, pak Adi


#### Pembuatan Repository G1T

Installasi dari archLinux saya, karena disekolah gaboleh pake debian based, mana sempat keburu pusing, bisa pake list dari "yay" atau manual pake "AUR", saya tidak wong selo, jadi pake apa yang dipake sama manusia umum, pake "pacman"

```
[tama@tamaoksa ~]$ sudo pacman -S git
[sudo] password for tama: 
warning: git-2.42.0-1 is up to date -- reinstalling
resolving dependencies...
looking for conflicting packages...

Packages (1) git-2.42.0-1

Total Installed Size:  26,31 MiB
Net Upgrade Size:       0,00 MiB

:: Proceed with installation? [Y/n] 
(1/1) checking keys in keyring                     [######################] 100%
(1/1) checking package integrity                   [######################] 100%
(1/1) loading package files                        [######################] 100%
(1/1) checking for file conflicts                  [######################] 100%
:: Processing package changes...
(1/1) reinstalling git                             [######################] 100%
:: Running post-transaction hooks...
(1/3) Creating system user accounts...
(2/3) Reloading system manager configuration...
(3/3) Arming ConditionNeedsUpdate...
```



cek

```
[tama@tamaoksa ~]$ git --version
git version 2.42.0
```



config setting

```
[tama@tamaoksa ~]$ git config --global user.name "oksaamerta"
[tama@tamaoksa ~]$ git config --global user.email oksaamerta@proton.me
[tama@tamaoksa ~]$ git config --list
user.name=oksaamerta
user.email=oksaamerta@proton.me
```



pembuatan repo

```
[tama@tamaoksa ~]$ mkdir blog

[tama@tamaoksa ~]$ cd blog

[tama@tamaoksa blog]$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /home/tama/blog/.git/
```



coba buat file README dan isinya

```
[tama@tamaoksa blog]$ vim README.md

[tama@tamaoksa blog]$ ls
README.md

[tama@tamaoksa blog]$ git add README.md

[tama@tamaoksa blog]$ git commit -m "first commit"
[master (root-commit) 3124d13] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

[tama@tamaoksa blog]$ git branch -M main

[tama@tamaoksa blog]$ git remote add origin https://github.com/oksaamerta/blog.git
```


coba push

```
[tama@tamaoksa blog]$ git push -u origin main
Username for 'https://github.com': oksaamerta
Password for 'https://oksaamerta@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/oksaamerta/blog.git/'
```

error, karna belum membuat kode token, buatnya di "akun-setting-developer-token klasik"



coba push lagi

```
[tama@tamaoksa blog]$ git push -u origin main
Username for 'https://github.com': oksaamerta
Password for 'https://oksaamerta@github.com': 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 228 bytes | 228.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/oksaamerta/blog.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/first_commit.png" />



#### revisi file, menambah file baru, dan melihat status log

git status

```
[tama@tamaoksa blog]$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
[tama@tamaoksa blog]$ git log
commit a53cd9338a9eb490b9f262e12144099702fe9f9d (HEAD -> main, origin/main)
Author: oksaamerta <oksaamerta@proton.me>
Date:   Tue Sep 19 06:49:59 2023 +0700

    coba upload gambar

commit 3124d134643fe5be6a5ff760e6d77e209e32fea8
Author: oksaamerta <oksaamerta@proton.me>
Date:   Tue Sep 19 06:31:30 2023 +0700

    first commit
```



edit file, lalu commit, sekalian upload gambar

```
[tama@tamaoksa blog]$ vim README.md

[tama@tamaoksa blog]$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```



melihat log

```
[tama@tamaoksa blog]$ git log --oneline
f46632f (HEAD -> main) revisi sedikit
a53cd93 (origin/main) coba upload gambar
3124d13 first commit
```



#### repo G1T yang sudah dibuat ?

tinggal buat folder lalu lakukan pull

```
[tama@tamaoksa ~]$ mkdir oksa

[tama@tamaoksa ~]$ cd oksa

[tama@tamaoksa oksa]$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /home/tama/oksa/.git/

[tama@tamaoksa oksa]$ git remote add origin https://github.com/oksaamerta/oksaamerta.github.io

[tama@tamaoksa oksa]$ git pull origin master
remote: Enumerating objects: 662, done.
remote: Counting objects: 100% (190/190), done.
remote: Compressing objects: 100% (121/121), done.
remote: Total 662 (delta 92), reused 141 (delta 55), pack-reused 472
Receiving objects: 100% (662/662), 3.42 MiB | 1.21 MiB/s, done.
Resolving deltas: 100% (339/339), done.
From https://github.com/oksaamerta/oksaamerta.github.io
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master
[tama@tamaoksa oksa]$ git status
On branch master
nothing to commit, working tree clean
```


cek folder

```
[tama@tamaoksa oksa]$ ls
about.md     example2-archive.md          index.md                 README.md
archive.md   favicon-16x16.png            _layouts                 _sass
assets       Gemfile                      LICENSE.txt              _screenshots
_config.yml  googleecca1f4c2a60d66e.html  no-style-please.gemspec
_data        _includes                    _posts
```



#### Sekian, dan terimakasih

yang sudah terlewat bulan agustus, jangan lupa nilai seratus pak :D