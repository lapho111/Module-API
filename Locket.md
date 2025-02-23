#!name= Locket Gold 
#!desc= Unlock By Lạp Hộ 

 

/****************************** 
📌 Tác Giả：LapHo: Remake   
📌 Cập Nhật：2025-2-17   
📌 Liên Lạc：Zalo: 0886632736   
📌 Face Book: https://www.facebook.com/share/lapho111 
*******************************/ 

 

[Script] 
revenuecat = type=http-response, pattern=^https:\/\/api\.revenuecat\.com\/.+\/(receipts$|subscribers\/[^/]+$), script-path= https://raw.githubusercontent.com/lapho111/Locket/refs/heads/main/locket1.js, requires-body=true, max-size=-1, timeout=60 
deleteHeader = type=http-request, pattern=^https:\/\/api\.revenuecat\.com\/.+\/(receipts|subscribers), script-path= https://raw.githubusercontent.com/lapho111/Locket/refs/heads/main/locket2.js, timeout=60 

 

[MITM] 
hostname = %APPEND% api.revenuecat.com 
