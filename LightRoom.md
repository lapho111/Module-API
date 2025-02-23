#!name=light room Cao Cấp 
#!desc=Unlock By Lạp Hộ 

 

/****************************** 
📌 Tác Giả：LapHo 
📌 Cập Nhật：2025-2-17   
📌 Liên Lạc：Zalo: 0886632736   
📌 Face Book: https://www.facebook.com/lapho111 
*******************************/ 

 

 

[MITM] 
hostname = %APPEND% photos.adobe.io 

[Script] 
LightRoom=type=http-response,pattern=^https:\/\/photos\.adobe\.io\/v2\/accounts*,requires-body=1,script-path=https://raw.githubusercontent.com/lapho111/Shadowrocket/refs/heads/main/LightRoom.js 
