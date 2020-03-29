# msfvenom zsh completion  

![](https://i.imgur.com/DJV1Jie.gif)

## install 

```
# You have to install oh-my-zsh first.

# Download the msfvenom plugin.
git clone https://github.com/Green-m/msfvenom-zsh-completion ~/.oh-my-zsh/custom/plugins/msfvenom/

# Open your ~/.zshrc file and enable msfvenom plugin like below
# plugins=(...  msfvenom)

source ~/.zshrc
```
@#fengzi 2020309
解决zsh补全msfvenom出现_values:compvalues:11: not enough arguments(参数不足)的问题
1、venom-cache文件放入~\.zsh\
2、~/.zshrc配置文件
插件加入
plugins=(git msfvenom)
最后加入
fpath=(~/.zsh/completion $fpath)
autoload -Uz compinit && compinit -i 
