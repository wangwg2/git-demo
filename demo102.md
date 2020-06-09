### Demo 102

#### master (0.1.0)
```bash
git add .
# add demo102.md

git commit -m "demo 102"
git tag -a 0.1.0

git push origin master
git push --tags
```

#### develop
```bash
git checkout -b develop master
git push origin develop
```

```bash
git clone -b develop git@github.com:wangwg2/git-demo.git gitdemo-dev

git remote add prod git@github.com:wangwg2/git-demo.git
git remote set-url origin git@github.com:wangwg2/git-demo-dev.git
```


#### hotfix
```
git clone git@github.com:wangwg2/git-demo.git git-demo-hotfix
```

```bash
git checkout -b hotfix-0630001 master 

## add:     hotfix-0630001.txt
git add .
git commit -m "hotfix-0630001: fix bug 0630001"
git push origin hotfix-0630001
```

合并到
```bash
git checkout master
git merge --no-ff hotfix-0630001
git tag -a 0.1.1

git rebase -i [startpoint]  [endpoint]

git push origin master
git push origin --tags
```

```bash
git checkout develop
git merge --no-ff hotfix-0630001
git branch -d hotfix-0630001
```

#### develop/feature01
(`git-demo-dev`)
```bash
git checkout -b feature01 develop

## add feature01.md
git add .
git commit -m "feature01-001"
git push origin feature01

## modify feature01.md
git add .
git commit -m "feature01-002"
git push origin feature01

## modify feature01.md
git add .
git commit -m "feature01-003"
git push origin feature01
```

```bash
## 在 “feature01” 完成开发
git checkout devleop                ## 切换到分支 "develop"
git merge --no-ff feature01         ## 合并分支

git rebase -i [startpoint]          ## 合并提交历史
git push origin develop             ## 推送分支 "develop"
git branch -d feature01             ## 删除分支 “feature01”
```
