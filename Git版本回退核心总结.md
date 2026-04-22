# Git 版本回退核心总结

1. **提交本质**：`git commit`是给Git 版本回退核心总结

   1. **提交本质**：`git commit`是给文件保存 "快照"，相当于游戏存盘，可随时恢复。
   2. 查看历史
      - `git log`：查看完整提交历史（从新到旧）
      - `git log --pretty=oneline`：简化输出，显示 commit id 和提交信息
      - commit id 是 SHA1 哈希值，分布式环境下避免冲突
   3. 版本回退
      - 用`HEAD`表示当前版本，`HEAD^`上一个，`HEAD~n`往上 n 个
      - `git reset --hard <版本号/HEAD^>`：硬回退，同时更新工作区文件
   4. **后悔药**：回退后找不到新版本 commit id 时，用`git reflog`查看所有操作历史，找到对应 id 后再次执行`git reset --hard`即可恢复。

2. 文件保存 "快照"，相当于游戏存盘，可随时恢复。

3. 查看历史

   - `git log`：查看完整提交历史（从新到旧）
   - `git log --pretty=oneline`：简化输出，显示 commit id 和提交信息
   - commit id 是 SHA1 哈希值，分布式环境下避免冲突

   

4. 版本回退

   ：

   - 用`HEAD`表示当前版本，`HEAD^`上一个，`HEAD~n`往上 n 个
   - `git reset --hard <版本号/HEAD^>`：硬回退，同时更新工作区文件

   

5. **后悔药**：回退后找不到新版本 commit id 时，用`git reflog`查看所有操作历史，找到对应 id 后再次执行`git reset --hard`即可恢复。