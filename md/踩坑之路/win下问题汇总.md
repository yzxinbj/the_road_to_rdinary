# win下问题汇总
正好最近换ssd后，重装系统后需要重新配置环境和安装各种工具  
所以正好把遇到的问题写下，方便他人

## win下连接开发机遇到的问题
1. 需要下载XShell，安装成功后点击工具下的新建用户密钥生成向导，按步骤生成密钥
2. 公司是用的freeipa来做管理，在上面加上生成的密钥
```
登录freeipa66.xhj.com，如果访问不到需要更改本机的host，到指定的ip
host文件地址：C:\Windows\System32\drivers\etc
```

## nvm for windows
由于开发不同项目时，老项目node版本有要求到很低，win下有nvm for windows  
`https://github.com/coreybutler/nvm-windows`  

## npm 镜像更换
```
临时使用 在命令后追加--registry 参数
npm install express --registry https://r.cnpmjs.org/
一次性更改并验证
npm config set registry https://r.cnpmjs.org/
npm config get registry
```
## node项目构建
1. 确定node版本
2. 确定依赖
3. 确定配置文件，环境变量