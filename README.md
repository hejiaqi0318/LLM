# 🔑 在 macOS 中设置 OpenAI API Key 环境变量

本指南介绍如何在 macOS 中设置 OpenAI API Key 到环境变量，方便在命令行或代码中使用。

---

## 1. 确认当前使用的 Shell

在终端输入以下命令，查看当前 Shell 类型：

```bash
ps -p $$ 
```

如果输出包含 -zsh → 使用的是 Zsh

如果输出包含 -bash → 使用的是 Bash

## 2. 打开配置文件

根据 Shell 类型，打开对应的配置文件：

Bash 用户：

```bash
nano ~/.bash_profile
```

Zsh 用户：

```bash
nano ~/.zshrc
```

## 3. 添加 API Key

在文件末尾添加一行（将 <你的API密钥> 替换成实际 Key）：

```bash
export OPENAI_API_KEY="<你的API密钥>"
```

## 4. 保存文件

在 nano 编辑器中操作步骤：

- 按 Control + X

- 输入 Y 确认保存

- 回车 Enter 退出
  
## 5. 让配置立即生效

执行以下命令，让刚才的修改立即生效：

Zsh 用户：

```bash
source ~/.zshrc
```

Bash 用户：

```bash
source ~/.bash_profile
```

## 6. 验证是否成功

输入以下命令：

```bash
echo $OPENAI_API_KEY
```

如果能输出你设置的密钥，说明配置成功 ✅
