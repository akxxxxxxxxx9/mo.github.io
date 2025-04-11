#使用telegram建立無限空間永久免費圖床，單一檔案30M上傳。
>覆蓋大多數文件格式：支援絕大多數常見圖片、影片、動圖等，同時也支援其他大多數格式的文件
>免費文件存放解決方案，具備上傳、管理、讀取、刪除等全貨架功能，涵蓋文件全生命週期，支援鑑權、目錄、圖片審查、隨機圖等各項各項功能
---
##準備工作
1.githube帳號
2.cloudflare帳號
3.Telegram帳號
---
##前提
 - 創建BotBotbot机器人 [@BotFather](https://t.me/BotFather)發送/newbot，依照提示輸入機器人的備註、使用者名稱等資訊。成功創建後獲得TG_BOT_TOKEN。
   -  建立一個新的頻道（Channel），進入新建的頻道，選擇頻道管理，將剛才建立的機器人設為頻道管理員。
   -  向[@VersaToolsBot](https://t.me/VersaToolsBot)轉發一則第2步驟新頻道中的消息，獲取TG_CHAT_ID（ID）
---
##開始部署
1.在github，Fork[MarSeventh/CloudFlare-ImgBed：基於CloudFlare Pages的開源文件託管解決方案（圖床/文件床/網盤）](https://github.com/MarSeventh/CloudFlare-ImgBed)
2.Cloudflareboard倉庫， 點選開始設定 
4.填寫項目名稱，建構指令填寫npm install，點選儲存並配置

```python
AUTH_CODE = diggoo
BASIC_USER = admin
BASIC_PASS = 123
TG_CHAT_ID = -1002180544284
TG_BOT_TOKEN = 1544711526:AAHiQI #機器人API
``` 

5.綁定KV資料庫：1,建立一個新的KV資料庫 2,-進入對應項目設定->綁定->新增->KV命名空間->變數名稱，填入img_url，KV命名空間選擇剛才建立好的KV資料庫