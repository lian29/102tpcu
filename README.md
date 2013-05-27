操作

每次修改好了以後，可以先將修改存入stage

`git add "檔名"`

若一次修改大量檔案，可以將所有檔案修改都add進去stage

`git add .`

之後commit提交一次的修改

`git commit -m "註解"`

另外也可以把git add與git commit用一個指令完成

`git commit -a -m "註解"`

改好了使用

`git push`

如果您在github上的版本較新，也可以輸入git pull 更新本地端的repo

`git pull git://github.com/ken800314/Simple-words.git`
