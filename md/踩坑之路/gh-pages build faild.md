## gh-pages 每次build时总提示 build falid try again later
```
问题描述：如题

背景：我使用的是`idoc` 生成的html，它将markdown文件按照目录顺序生成
     一直查不到问题所在，然后我新建了了仓库，使用相同的文件仍然失败，
     我试了下仓库只有index.html是可以的
     
问题原因：通过逐个目录增加测试，发现是md目录内文件过多造成build失败

解决办法：通过在master存下完整文件，然后在gh-pages分支下只保存html即可，在gh-pages分支下删除md目录
```
