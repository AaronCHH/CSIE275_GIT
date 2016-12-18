# Install git (Mac)  
1. 先安裝 Homebrew，Mac 的套件管理工具  
   請打開你的 Terminal，輸入以下：  
   ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"  

2. 輸入以下指令：  
   brew install git  

3. 打開 git 的彩色輸出：  
   git config --global color.ui true  

4. 設定 git 的 user 和 email (用註冊 github 的資訊)  
   git config --global user.name "你的名稱"  
   git config --global user.email "你的email"  
