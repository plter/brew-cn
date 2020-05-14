# brew-cn
清华镜像版 brew

# 说明  

大陆用户使用brew存在一定的困难，为此我整理了这个文档，便于大陆用户使用清华brew镜像。

# 流程 

1. `git clone https://github.com/plter/brew-cn.git`
1. 进入`brew-cn`目录，执行 `install.sh`
1. 执行到 “==> Tapping homebrew/core” 时 Ctrl-C 中止
1. `git clone https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/linuxbrew-core.git "$(brew --repo homebrew/core)"`
1. `git clone https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-cask.git "$(brew --repo homebrew/cask)"`
1. `git clone https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-cask-fonts.git "$(brew --repo homebrew/cask-fonts)"`
1. `git clone https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-cask-drivers.git "$(brew --repo homebrew/cask-drivers)"`
1. `git -C "$(brew --repo)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git`
1. `echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles' >> ~/.bash_profile
source ~/.bash_profile`