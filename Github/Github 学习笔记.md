# Github 学习笔记

### 与本地项目关联

1. github创建仓库，初始化README.md文件.

2.  本地创建仓库，与本地仓库关联. **注意：将远程仓库README.md同步到本地才能关联**

   ``` shell
   git pull origin master --allow-unrelated-histories
   ```

3. 添加修改

   ```shell
   git add .		
   ```

4. 提交修改到缓存，添加备注

   ```shell
   git commit -m "comment"	
   ```

5. 推送修改到远程仓库.

   ```shell
   git push -u origin master
   ```

   **第一提交需要上面命令，以后只用输入**

   ```shell
   git push
   ```

   ​

