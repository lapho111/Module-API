 #!name=Youtube Premium 
#!desc=Unlock By Lạp Hộ 

 
/****************************** 
📌 Tác Giả：LapHo 
📌 Cập Nhật：2025-2-17   
📌 Liên Lạc：Zalo: 0886632736   
📌 Face Book: https://www.facebook.com/lapho111 
******************************/ 

 
[Rule]   
AND,((DOMAIN-SUFFIX,googlevideo.com), (PROTOCOL,UDP)),REJECT   
AND,((DOMAIN,youtubei.googleapis.com), (PROTOCOL,UDP)),REJECT   

[URL Rewrite]     
(^https?:\/\/[\w-]+\.googlevideo\.com\/(?!dclk_video_ads).+?)&ctier=L(&.+?),ctier,(.+) $1$2$3 302   
^https?:\/\/[\w-]+\.googlevideo\.com\/(?!(dclk_video_ads|videoplayback\?)).+&oad _ reject-200   
^https?:\/\/(www|s)\.youtube\.com\/api\/stats\/ads _ reject-200   
^https?:\/\/(www|s)\.youtube\.com\/(pagead|ptracking) _ reject-200   
^https?:\/\/s\.youtube\.com\/api\/stats\/qoe\?adcontext _ reject-200   

[Script]   
youtube.request = type=http-request,pattern=^https:\/\/youtubei\.googleapis\.com\/youtubei\/v1\/(browse|next|player|reel\/reel_watch_sequence|get_watch),requires-body=1,max-size=-1,binary-body-mode=1,engine=script-engine,script-path= https://raw.githubusercontent.com/lapho111/Shadowrocket/refs/heads/main/youtobe%2311.js   
youtube.response = type=http-response,pattern=^https:\/\/youtubei\.googleapis\.com\/youtubei\/v1\/(browse|next|player|search|reel\/reel_watch_sequence|guide|account\/get_setting|get_watch),requires-body=1,max-size=-1,binary-body-mode=1,engine=script-engine,script-path= https://raw.githubusercontent.com/lapho111/Shadowrocket/refs/heads/main/YouTobe%2312.js,argument="{"lyricLang":"off", "captionLang":"off","blockUpload":false,"blockImmersive":false,"debug":false}"   

[MITM]   
hostname = %APPEND% -redirector*.googlevideo.com,*.googlevideo.com,www.youtube.com,s.youtube.com,youtubei.googleapis.com   
