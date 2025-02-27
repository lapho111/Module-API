#!name= Spotify Premium
#!desc= Unlock By Lạp Hộ

[General]
bypass-system = true
skip-proxy = *.local, *.crashlytics.com
tun-excluded-routes = 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12

[MITM]
hostname = spclient.wg.spotify.com

[Script]
spotify-json = type=http-request,type=http-request,pattern=^https:\/\/spclient\.wg\.spotify\.com\/(artistview\/v1\/artist|album-entity-view\/v2\/album)\/,requires-body=0,script-path= https://raw.githubusercontent.com/lapho111/Shadowrocket/refs/heads/main/Spotify1.js
spotify-proto = type=http-response,pattern=^https:\/\/spclient\.wg\.spotify\.com\/(bootstrap\/v1\/bootstrap|user-customization-service\/v1\/customize)$,requires-body=1,binary-mode=1,max-size=0,script-path= https://raw.githubusercontent.com/lapho111/Shadowrocket/refs/heads/main/Spotify2.js,script-update-interval=0
