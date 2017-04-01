# Android Studio 快捷键

---

#### 常用快捷键
ctrl+shift+enter 自动跳到代码尾部并添加 ; 号

Ctrl+j 自动代码（比如 自动生成for循环）

Ctrl + Shift + u 大小写切换

Ctrl + Shift + e  或 ctrl+e  可以显示最近编辑的文件列表

Ctrl + alt + m   抽取方法

Ctrl＋[ 或 ]   可以跳到大括号的开头结尾

Ctrl＋Shift＋Backspace可以跳转到上次编辑的地方

Ctrl＋F12  可以显示当前文件的结构进行查找

Ctrl＋F7   可以查询当前元素在当前文件中的引用，然后按F3可以选择

Ctrl＋N 可以快速打开类

Ctrl＋Shift＋N 可以快速打开文件

Ctrl＋Alt＋V 可以引入变量

Ctrl＋Alt＋T 可以把代码包在一块内，例如try/catch

ALt + F7  检查文件是否被引用

F2 或 Shift + F2  高亮错误或警告快速定位

Shift + F6 重构-重命名

Alt + Insert 生成代码 (如get,set方法,构造函数等)

Ctrl + F 或 Ctrl + F3 本查找文本

---

#### 修改成员变量前缀:
如果你命名成员变量习惯前面加一个m的前缀，但是生成getter和setter的时候，又不希望方法名中有这个m，可以如下设置。
File->Settings->Code Style->Java,然后在右边面板中选择Code Generation标签，Naming，Field这一行，对应的Name prefix中加上m.

---

#### 取消多作的空格：
每次保存的时候，每行多余的空格和TAB会被自动删除（例如结尾、空行的多余空格或TAB）
Settings->IDE Settings->Editor->Other->Strip trailing spaces on Save->None