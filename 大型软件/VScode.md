

------

# 快捷键

## 全局

```python
Ctrl + P					# 全局搜索
Ctrl + Shift + P			# 显示所有命令
Ctrl + Shift + X			# 打开应用商店(会与QQ浏览器的区域截图快捷键冲突)
```
## 文本

###  Windows

```python
F5		# 运行程序
F9      # 所在行设置断点
home/end        # 移动光标到行 首/尾
alt + up/down       # 向 上/下 移动行
alt + left/right        # 光标回到 上/ 下 一个位置（跨文本）
Ctrl + ~		# 显示/隐藏终端
Ctrl + /		# 切换行注释
Ctrl + D    # 选定当前词汇 or 将下一个查找匹配项添加到选择
Ctrl + L        # 选择当前行（鼠标3击）
ctrl + u        # 光标回到上次状态（包含位置）（不能跨文本）
ctrl + home/end     # 移动光标到文本 首/尾
Ctrl + PgUp/PgDn        # 切换 上/下 标签页
ctrl + up/down      # 不移动光标移动文本滚轮
ctrl + left/right       # 跳token移动光标
ctrl + delete       # 删除光标后面的词（token)
ctrl + alt + left/right     # 文本便签页向 左/右 扩展移动
ctrl + alt + up/down        # 向 上/下 扩展多行编辑光标
Ctrl + Shift + ~        # 新建一个终端并打开
ctrl + shift + l        # 选择所有匹配项  # *
Ctrl + Shift + K        # 删除行    # 会和搜狗输入法 软键盘 快捷键冲突
Ctrl +(Shift)+ Enter        # 向 上/下 空行
shift + home/end        # 移动光标到行 首/尾 的同时选中内容
shift + alt + up/down       # 向 上/下 复制行
shift + alt + left/right        # 缩小/扩大 选中范围  # *

# 组合键
ctrl + k, ctrl + 0      # 折叠所有代码；
ctrl + k, ctrl + j      # 展开所有代码；
```

- 快捷操作：

1. 多行选择 + 多行编辑
   
   `首先点击左上角` 然后 `shift + alt + 单击右下角`
   ![](https://exp-picture.cdn.bcebos.com/c255efc595ee41c17b1a83e68d88912ca4ca9b96.jpg?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_500%2Climit_1%2Fformat%2Cf_jpg%2Fquality%2Cq_80)

### macOS

- 默认

```python
command + /		# 切换行注释  # most
command + D		# 选定当前词汇 or 将下一个查找匹配项添加到选择
command + L		# 选中当前行，继续按是往下多选
command + left/right		# 光标移动到行 首/尾
option + z		# 切换自动换行
option + left/right		# 光标根据文字块移动
option + up/down			# 将行进行 上/下 移动
option + command + up/down		# 在 上/下 添加光标
option + command + left/right		# 光标在 左/右 标签移动
shift + ctrl + left/right		# 缩小/扩大 选中范围
shift + option + a		# 切换块注释
shift + option + up/down		# 多选 上/下 拷贝复制
shift + command + k		# 删除行

## command + k,
command + q		# 光标转到上一个编辑的位置
```
- 自定义

因为我叫Jacob，所以把`command + j`改成了`command + j, command + j`,然后所有的组合键均使用`command + j, your choose`

```python
# command + j,
command + p		# (path)聚焦到导航路径视图  # 神器！
command + u		# 光标重做
command + t		# (teminal)焦点到终端视图上
command + l		# 删除行
```

## 其他操作

### ctrl + k, r

选中一个文件，`ctrl + k, r` 在文件管理器中打开文件所在文件夹。

### Ctrl + Shift + P

- `Ctrl + Shift + P`		# 显示所有命令

```python
//	命令						//中文
view:toggle menu bar		# 视图：切换菜单栏
```

### Ctrl  + Shift + U

- `Ctrl  + Shift + U`		# 进入输出终端

```python
# 输出终端操作
Ctrl + End			# 翻到最下
```

## 快捷键终结设置教程

1. 简单的设置方式

- 文件 -> 首选项 -> 键盘快捷方式

![](https://i.loli.net/2021/06/29/SsGFRMhyTjnO94g.png)

- 这里就可以自定义自己喜欢的快捷键了

2. 进阶教程

- 在上述界面中找到右上角的图标，打开键盘快捷键方式(JSON)

![](https://i.loli.net/2021/06/29/TqVZtdXLW9AwKuH.png)

- 可以在`.json`文件中自由编辑快捷键的方式了，command命令可以在上一个界面右键复制命令ID获取。

![](https://i.loli.net/2021/06/29/Mnwi8yHh2rZqXSU.png)

# 个人操作习惯记录

## Shift + F10 // 右键菜单

在文本编辑界面，`Shift + F10` 可以打开右键菜单栏，然后上下可以选择命令选项，回车即可。

![image-20210702091826187](https://i.loli.net/2021/07/02/7GCRAmdvNLho5af.png)

## Ctrl + F // 搜索

- `Ctrl + F` 当前文件搜索；`Ctrl + Shift + F` 当前项目搜索
- 上下查找

`Enter` 下一个匹配项；`Shift + Enter` 上一个匹配项。

- Alt + W // 全字匹配

- 不常用

```python
Alt + C				# 区分大小写
Alt + R				# 正则表达式
Alt + L				# 在选定内容中查找
```

# keybindings.json
```json
// 将键绑定放在此文件中以覆盖默认值

[

 	 {

    ​    "key": "ctrl+j ctrl+j",

    ​    "command": "workbench.action.togglePanel"

  	},
    {
        "key": "ctrl+j ctrl+right",
        "command": "workbench.action.splitEditorRight"
    },
    {
        "key": "ctrl+j ctrl+left",
        "command": "workbench.action.splitEditorLeft"
    },
    {
        "key": "ctrl+j ctrl+down",
        "command": "workbench.action.splitEditorDown"
    },
    {
        "key": "ctrl+j ctrl+up",
        "command": "workbench.action.splitEditorUp"
    }
]
```