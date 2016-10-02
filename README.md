# Layer 6
## SSOの2方式

- エージェント方式 - SSOを利用したいサーバにモジュールをインストール
- リバースプロキシ方式 -　全ての通信がSSOサーバを通過

## リバースプロキシ
> リバースプロキシとは、ある特定のWebサーバーの代わりにクライアント（ユーザー）からのアクセスを受け付ける代行（プロキシ）サーバーのひとつで、Webサイトを運営する側のネットワークに設置されるもののことである。

> 通常、プロキシサーバーはクライアント側に置かれ、クライアントがWebサーバーにアクセスする動作を中継する役割を果たすが、これとは逆にリバースプロキシは、Webサーバーの手前に置かれ、サーバーへの要求を受け取ってそれを背後のWebサーバーに受け渡すために用いられる。

> 特定の（代行されている側の）サーバーにアクセスしようとしたクライアントは必ずリバースプロキシを経由することになるため、Webサーバーが直接アクセスを受けることがなくなり、つまり負担が軽減される。また、認証機能やアクセス制御機能を持つものも多く、セキュリティの面でも導入効果が得られる。

## Cookie
食べ物じゃないよ
### Set-Cookie Serure
>https: のページで使用するCookieには発行時に secure属性をつける。
secure属性が付けられたCookieは、http:のコンテンツ宛には送られない。

> http: のページにおいてもCookieを使用する必要がある場合は、Cookie の値を第三者が傍受し得ることを十分に考慮した上で secure属性のつかない Cookieを発行する。

## FTP
- アクティブモード => ダウンロード。port20
- パッシブモード => アップロード。portは任意

# Layer 4
## TCP
### portの上限数
 16ビット(6万位)

# Layer 3
## LB(ロードバランサ)の2方式

- DSR - ServerとLBを同じ階層に
- インライン - LBをServerの手前に


## ループバックIF
 仮想IP(VIP)のIF

## スループットとビットレート
 NWではスループットを用いる。


## FW
### 動的FW
 過去に通過したリクエストパケットに対応付けられるものだけを通過させる。セッション単位で宛先/戻りが同じFWを通過する必要がある。
“時間を待たずに”,”その先の故障も検知”。

## ICMP
- "3" : destination unreachable
- “0” : echo request

## セキュリティ
### IPS(防御 : Prevention)

- 検出の誤り
 フェールスポジティブ - 正常な通信を不正とする
 フェールスネガティブ -  不正な通信を見逃す

## IDS(検知 : Detection)

- シグネチャ型 - 事前定義
- あのまり型 - 振る舞いで検出

## 遮断機能

- TCP通信の遮断機能
 TCPのRSTフラグをオンにして、不正な通信を遮断。

- UDP通信の遮断機能
 ICMPのヘッダに"3" : destination unreachableを付与

## NIC
- プロミスキャスト・・宛先MACアドレス以外のフレームも受信


## Layer 2
## SW
- ミラーポート

## プロトコル

### ARP
- IPアドレスからMacアドレス

### GARP
- IPアドレスの重複を検知。

### NAR444
>　このような従来のNATとは異なり，NAT444ではIPv4グローバル・アドレスを持つIPv4インターネット，IPv4プライベート・アドレスを持つLANとの間に，ISP（Internet services provider）シェアド・アドレスという特別なIPv4アドレスを持つネットワークを設ける（ただし必ずしもISPシェアド・アドレスである必要はなく，任意のIPアドレスでよい）。「444」とは，この3種類のアドレスを割り当てたネットワーク空間を指す

>一方で，NAT444を導入すると「一部のアプリケーションの動作に問題が出る」との見方がある。その原因として主に想定されるのは，（1）1ユーザー当たりのセッション数の不足，（2）NAT越えがうまくいかない──の二つである。

