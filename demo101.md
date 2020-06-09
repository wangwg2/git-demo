### Demo 101

#### 1. 远程 repository

注册登录 github.com, 创建 repository `git-demo` (选择 `public`)

#### 2. 本地 repository
初始化本地 repository
```bash
# 创建新文件夹并打开，创建新的 git 仓库。
mkdir git-demo && cd git-demo            # 创建目录
git init                                 # 初始化git仓库
```

创建git相关文件和工作，如`.gitignore`,`README.md`,`demo101.md`文件

```bash
# 查看状态
git status
# 跟踪新文件
git add .gitignore README.md demo101.md  # 跟踪指定文件
git add -A                               # 跟踪当前目录下所有文件
# 提交更新
git commit -m "first commit"
```

#### 3. 远程 repository
```bash
# 将本地仓库连接到远端服务器
git remote add origin git@github.com:wangwg2/git-demo.git
# 将改动提交到远端仓库。master为要推送的分支。
git push -u origin master
```

