##自制比较有用的 autohotkey 脚本

#### ^Space 目前个人最顺手的 win8 以上使用 ctrl+space 切换中英文输入法方案
why use?
* 尽管很多中文输入法使用 shift 可以切换中英文，但是对 coding 非常不便利，加上个人感觉中文输入法打英文字母的 delay 比原生的英文键盘多 1-3ms（无法忍受）。
* 一些搜索到的建议方案，如 alt+shift 切换语言有很长的延迟（1s）；win+space 并不在按下时切换；最大的问题是假如安装了多于两种语言，比如中，英，日，那么将会在三种语言之间循环，而不能满足只切换中英文。
* win 自带的“中文输入法切换中英文的快捷键”不能隐藏输入法窗口，因此无法判断哪个进程目前是中文还是英文。
* 过去有些人做了注册表 hack，可以在中文里加入 US Keyboard，但是将来如果要添加/删除语言或输入法，很可能出现输入法语言列表彻底乱掉，默认语言消失而不得不重新对注册表做更复杂的修改。
* 使用某国产输入法顺序切换工具并不是一个足够安全和便利的方案。
* 适应新的输入习惯？不。。。 <s>几十年的习惯并不是一两年就能改掉的（巨硬已死？</s>

于是经过很多次搜索，到目前并没有一个完全符合需求的方便切换中英文输入法的方案，即使是有见到 autohotkey 脚本也只是重定向按键，或者切换到指定输入法而无法切换回来。

就自制了一个目前所能想到的兼容性最好的复活 Ctrl+Epace 切换中英文输入法的脚本：

通过 autohotkey 可以像旧版 windows 一样直接使用 ctrl+space 切换中文和英文输入法，无需更改注册表，切换延迟比系统自带的切换方案低很多，即使安装多于3种语言仍然能保持只切换中英文...顺手爆炸了（

注意事项：系统必须已有 English (United States) 语言和 Keyboard Layout: US 输入法；中文语言和至少一个中文输入法。  
例如 mac 如果用 bootcamp 装 windows，英文并不是US键盘，而是 United States (Apple) ，这时需要手动添加 US 键盘。否则会切换到一个不存在的英文键盘上。

注意事项2：autohotkey似乎对有提权的程序支持并不太好，也偶尔有锁定系统再解锁失效的可能，彻底关闭UAC后没有这些问题。

#### others?
新脚本持续添加中