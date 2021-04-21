# Jupyter_Notebook

## 基本说明

- 绿色：编辑模式 

- 蓝色：命令行模式

> 编辑模式下按 Esc 进入命令行模式
>
> 命令行模式下按 Enter 进入编辑模式

### 相关设置说明

#### 创建/初始化 config文档

- 打开anaconda prompt

- 输入：jupyter notebook --generate-config

#### 设置默认打开目录

- 打开文件：jupyter_notebook_config.py
- 找到：#c.NotebookApp.notebook_dir = ‘’
- 修改为你想设置的路径，然后保存
- 最后还需要在开始菜单找到 jupyter notebook 快捷键，右键➡更多➡打开文件所在位置，找打快捷方式在文件中的位置，右键➡属性➡目标，去掉最后的 %USERPROFILE%，应用、确定。
![更改默认目录](https://img-blog.csdnimg.cn/20190827175022714.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQwMTA4ODAz,size_16,color_FFFFFF,t_70)

#### 设置默认浏览器

- 打开文件：jupyter_notebook_config.py

- 找到：找到 # c.NotebookApp.browser = ''''

- 在下方添加

```python
import webbrowser
webbrowser.register("chrome",None,webbrowser.GenericBrowser(r"C:\\ProgramFiles(x86)\\Google\\Chrome\\Application\\chrome.exe"))
c.NotebookApp.browser = 'chrome'
```

## 命令行模式

```python
M		# 代码块变成标签-Markdown语法
Y		# 代码块变成代码
H		# 打开快捷键菜单
X		# 剪切代码块
C		# 复制代码块
Z		# 撤销删除
A		# 上面插入代码块
B		# 下面插入代码块
L		# 代码块显示行号
V				# 粘贴到上面
Shift + V		# 粘贴到下面
Alt + Enter		# 运行代码块并插入一个新的代码块 
Ctrl + Enter		# 运行代码块并选中当前代码块
Shift + Enter		# 运行代码块并选择下一个代码块
```

## 编辑模式

```python
Ctrl + M		# 进入命令行模式
```

# 设置相关

##　更换默认浏览器

[原作链接](https://blog.csdn.net/pei327586354/article/details/107485704)

- **1.启动cmd，键入“jupyter notebook --generate-config”，创建jupyter notebook的配置文件，同时会输出```jupyter_notebook_config.py```文件的路径，默认是“C:\Users\xxxx\.jupyter\jupyter_notebook_config.py”;**

> 创建之前可以用```everything```搜一下，说不定电脑里直接就有。

- **2.  找到该文件，使用notepad++打开(txt也行的啦)，
   在```“#c.NotebookApp.browser = ''”``` 下一行添加浏览器配置信息即可。配置信息如下：**
```
import webbrowser
webbrowser.register("chrome", None, webbrowser.GenericBrowser(u"C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe"))
c.NotebookApp.browser = 'chrome'
```

> 里面的path就是你浏览器启动程序所在的地址。

## 切换kernel

[原作链接](https://blog.csdn.net/Junhao_Lu/article/details/100625831)

## 切换主题

__安装主题:__

```python
pip install --upgrade jupyterthemes		# anaconda prompt
```

__常用操作：__

```python
jt -l		# 查看主题
jt -r		# 恢复默认主题
```

__[主题展示](https://blog.csdn.net/qq_41621362/article/details/89894126?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-2.control&dist_request_id=1332024.6981.16189848172240689&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-2.control)；[详细操作](https://blog.csdn.net/qq_30565883/article/details/79444750#commentsedit)；__

__推荐的主题：__
```python
jt -t chesterish -fs 14 -cellw 85% -ofs 13 -dfs 11 -T
jt -t chesterish -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N		# 1
jt -t grade3 -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N
jt -t gruvboxd -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N		# 1
jt -t gruvboxl -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N
jt -t monokai -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N
jt -t oceans16 -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N
jt -t onedork -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N
jt -t solarizedd -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N
jt -t solarizedl -f fira -fs 11 -cellw 70% -ofs 11 -dfs 11 -T -N
```

__含义__
```python
-f(字体)  -fs(字体大小) -cellw(占屏比或宽度)  -ofs(输出段的字号)  -dfs(表头的字号) -T(显示工具栏)  -N(显示自己主机名)
```

__注释字体修改（Italia 斜体改 normal）__

打开文件夹 `C:\Users\Lyun\.jupyter\custom`

找到文件并打开 `custom.css`

找到` cm-comment `中的内容，原内容为：

```
 color: #75715e;
 font-style: italic
```

修改后

```
color: #75715e;
 font-style: normal
```