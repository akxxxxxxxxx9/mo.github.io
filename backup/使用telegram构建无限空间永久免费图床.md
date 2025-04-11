#使用telegram构建无限空间永久免费图床，单个文件30M上传。
>免費文件寄存解決方案，具備上傳、管理、讀取、刪除等全貨架功能，涵蓋文件全生命週期，支援鑑權、目錄、圖片審查、隨機圖等各項特性
##准备工作
1.githube账号
2.cloudflare账号
3.Telegram帐号
   1.创建Bot机器人[@BotFather](https://t.me/BotFather)加入机器人[@VersaToolsBot](https://t.me/VersaToolsBot)
      +  建立機器人：向[@BotFather](https://t.me/BotFather)發送/newbot，依照提示輸入機器人的備註、使用者名稱等資訊。成功創建後獲得TG_BOT_TOKEN。
      +  建立一個新的頻道（Channel），進入新建的頻道，選擇頻道管理，將剛才建立的機器人設為頻道管理員。
      +  向[@VersaToolsBot](https://t.me/VersaToolsBot)轉發一則第2步驟新頻道中的訊息，取得TG_CHAT_ID（ID）
##开始部署
1.在github，Fork项目[MarSeventh/CloudFlare-ImgBed：基於CloudFlare Pages的開源文件託管解決方案（圖床/文件床/網盤）](https://github.com/MarSeventh/CloudFlare-ImgBed)
2.Cloudflare Dashboard，進入Pages管理頁面打開，選擇建立項目，選擇连接到 Git 提供程序
3.依照頁面提示輸入項目名稱，選擇需要連接的git倉庫，點選开始设置
4.填寫项目名称，建置指令填寫npm install，點選保存并部署

'''AUTH_CODE = diggoo
BASIC_USER = admin
BASIC_PASS = 123
TG_CHAT_ID = -1002180544284
TG_BOT_TOKEN = 1544711526:AAHiQI  #机器人API
'''

5.綁定KV資料庫：1,建立一個新的KV資料庫 2,- 進入對應項目设置-> 绑定-> 添加-> KV 命名空间-> 变量名称，填寫img_url，KV命名空间選擇剛才建立好的KV資料庫
