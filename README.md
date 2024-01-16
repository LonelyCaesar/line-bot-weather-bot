# lineBot氣象小助理

# 一、說明
本專題使用anaconda3.9以上版本、網路爬蟲(爬取)、linebot開發流程及預設功能提供地址製作出一個lineBot氣象小助理，串接雷達回波與地震資訊、目前氣象資訊、天氣預報和空氣品質快速問答說明功能。
套件安裝準備：
1.	請先註冊並登入LINE Developer並建立 Line Channel
2.	請先下載ngrok.exe放置於桌面上，點開後輸入ngrok htt6 5000就會產生網址將貼在建立好的api的Webhook URL上然後測試。
3.	輸入flask --app 自己的檔名 --debug run。
4.	輸入pip install flask-ngrok指令安裝套件。
5.	輸入pip install line-bot-sdk指令安裝套件。
6.	氣象資料開放平台https://opendata.cwa.gov.tw/index。

# 二、相關文章
透過 Messaging API，機器人伺服器可以向 LINE 平台發送資料並從 LINE 平台接收資料。請求以 JSON 格式透過 HTTPS 傳送。Bot伺服器與LINE平台之間的通訊流程如下：
1.	用戶向 LINE 官方帳戶發送訊息。
2.	LINE 平台將 webhook 事件傳送到機器人伺服器的 webhook URL。
3.	機器人伺服器檢查 webhook 事件並透過 LINE 平台回應用戶。
參考網址：
https://developers.line.biz/en/docs/messaging-api/overview/

![messaging-api-architecture f40bffbb](https://github.com/LonelyCaesar/line-bot-weather-bot/assets/101235367/8111f8bc-290b-4ba2-a85a-8e744bed74db)

# 三、實作
LineBot氣象小助理完整demo：
透過氣象資料開放平台的json爬取要的資料、開啟ngrok取得網址、授權碼貼在code上面及LINE Developer的key作串接並能夠完整的執行。

程式碼：
'''
from flask_ngrok import run_with_ngrok
from flask import Flask, request
'''
