# 天敏 *TM7*

# 重新拉分支
- 从TM6拉出新的分支 
- [步骤](#newbranch)
	- 父分支名：TM6_20161110
- 出全量包
- 出差分升级包
- 测试升级
- 测试黑屏补丁










## newbranch  
在本地代码仓库
repo forall -c "git命令" 对仓库下所有git仓库操作
1. 将分支全部切换到要拉出分支的分支上
远端分支切换并追踪： repo forall -c "git checkout --track 远端分支"
2. 确保分支为最新代码：repo sync 
3. 从当前分支拉出新分支：repo forall -c "git checkout -b 新分支"
4. 将新拉分支推到远端：repo forall -c "git push 仓库 新分支"
5. 修改repo 创建仓库分支
cd .repo/manifests
git checkout -b 新分支
修改.repo/manifests/default.xml
git commit 
git push 仓库 新分支