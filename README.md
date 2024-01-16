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
