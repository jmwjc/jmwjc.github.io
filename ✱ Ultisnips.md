# 基本结构
```
snippet 关键词 "说明" 设定
	内容
endsnippet
```

# 设定
- `b`代表关键词出现在行首时展开
- `A`代表自动展开
- `w`代表独立关键字展开
- `i`代表忽略前后字节直接展开
- `r`代表需要trigger展开
- `t`Do not expand tabs
- `s`Remove whitespace
- `m`Trim all whitespace from right side of snippet lines
- `e`Custom context snippet

# 内容
- `$0`最后光标处
- `$1`第一个光标处
- `${1:默认}`默认输入
- `${1:${VISUAL}}`在visual模式下选择输入
	1. 在visual模式下选中代码，按下`trigger`
	2. 展开snippet并输入

# 使用python定义snippet
- `!p`代表使用python
- `global !p`该方程被所有代码公用