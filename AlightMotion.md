#!name= Alight Motion Pro 
#!desc= Unlock By Lạp Hộ 

 

/****************************** 
📌 Tác Giả：LapHo: Remake   
📌 Cập Nhật：2025-2-17   
📌 Liên Lạc：Zalo: 0886632736   
📌 Face Book: https://www.facebook.com/share/lapho111 
*******************************/ 

 

[MITM] 
hostname = us-central1-alight-creative.cloudfunctions.net 

 

[Script] 
Alightmotion = type=http-response,script-path= https://raw.githubusercontent.com/lapho111/Shadowrocket/refs/heads/main/Alight%20Motion.js,pattern=^https:\/\/us-central1-alight-creative\.cloudfunctions\.net\/getAccountStatusAndLicenses,max-size=131072,requires-body=true,timeout=10,enable=true 
