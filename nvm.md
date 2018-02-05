## nvm

nvm是用来管理node版本的，可以更新node，切换node,安装node

参考   https://github.com/creationix/nvm

#### 安装 nvm

根据本机的系统选择下载路径

```
OSX和linux版本：
https://github.com/creationix/nvm
```

```
window版本：
https://github.com/coreybutler/nvm-windows
```

#### 解压nvm

将下载的nvm压缩包解压，在 C:\Users\15204\AppData\Roaming\下可以看到解压后的文件nvm(AppData是隐藏路径，需要手动搜索)，并将在会使用到的node版本移动到nvm内，这样就可以使用并切换node了。

#### nvm路径

C:\Users\15204\AppData\Roaming\nvm

验证安装

```
nvm  -v  
```

安装node

```
nvm install v6.10.0    
```

运行node

```
nvm run node --version
```

切换node的版本

```
nvm use '版本号'
```

显示nvm下安装的node版本

```
nvm list
```

要恢复路径，可以停用

```
nvm deactivate
```

想要使用默认node，别名default

```
nvm alias default node
```

显示node信息

```
node -v
```
