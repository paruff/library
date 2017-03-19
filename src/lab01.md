# Version control - Lab 01
## GIT


### GUI
1. Open Sourcetree
2. Clone/new -> Source/Path 
3. Destination Navigate to C:/users/{ldapid}/Documents\workspace-sts/ , you may need to create projects

### Validate
1. Start Windows Explorer, assert c:/users/{ldapid}/Documents\workspace-sts/hello_world/pom.xml



## GIT for SVN Summary

| GIT      |SVN        |
| ------------- |:-------------:|
| git clone url | svn checkout url |
| git pull      |svn update |
| git status	|svn status |
| git add file | svn add file|
| git rm file  | svn rm file |
| git mv file | svn mv file |
| git commit -a	| svn commit |
| git log   |	svn log |
| git tag -a name	| svn copy http://example.com/svn/trunk http://example.com/svn/tags/name |
| git branch branch 
| git checkout branch |	svn copy http://example.com/svn/trunk http://example.com/svn/branches/branch |
| git merge branch	| svn merge -r 20:HEAD http://example.com/svn/branches/branch |
| git pull |	svn update |

[Git - SVN Crash Course](http://git.or.cz/course/svn.html)
[git concepts simplified](http://gitolite.com/gcs.html#(1))
