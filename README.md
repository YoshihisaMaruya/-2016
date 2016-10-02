# SSOの2方式

- エージェント方式 -
- リバースプロキシ方式 -

# LB(ロードバランサ)の2方式

- DSR - ServerとLBを同じ階層に
- インライン - LBをServerの手前に

# GARP
 IPアドレスの重複を検知

# ループバックIF
 仮想IP(VIP)のIF

# スループットとビットレート
 NWではスループットを用いる。

#FW
## 動的FW
 過去に通過したリクエストパケットに対応付けられるものだけを通過させる。セッション単位で宛先/戻りが同じFWを通過する必要がある。

“時間を待たずに”,”その先の故障も検知”

# IPS(防御 : Prevention)

・検出の誤り
 フェールスポジティブ - 正常な通信を不正とする
  フェールスネガティブ -  不正な通信を見逃す

# SW
 ミラーポート

# NIC
 プロミスキャスト・・宛先MACアドレス以外のフレームも受信

# L2
 ICMP
 　-> "3" : destination unreachable
     -> “0” : echo request

# IDS(検知 : Detection)

- シグネチャ型 - 事前定義
- あのまり型 - 振る舞いで検出

・TCP通信の遮断機能
TCPのRSTフラグをオンにして、不正な通信を遮断。

・UDP通信の遮断機能

UTM

# RP