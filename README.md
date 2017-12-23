# zabbix_template_tcp

TCP Connection Status Template for Zabbix ~> 3.4.

Necessary "Dependent Item". Put userparameter_tcp.conf in Include-UserParameter's Directory and Put json_item_tcp.sh in /var/lib/zabbix .

- ZABBIX 3.4用 TCP Connection Statusのテンプレートです。
- UserParameterのワインライナーで…をするには少々複雑すぎたたのでラッパースクリプトを挟んでJSONを取得して依存アイテムに入れてます。
- CentOS用のをデフォルトにしています。FreeBSDではbash入れてjson_item_tcp.sh.freebsdを使ってください。
- Linuxはprocファイルシステムから集計しているのでnet-tools入れる必要はありません。あれのnetstatは遅いので5桁コネクションで5秒以上かかってタイムアウトします。
- UNKNOWNは計算しようと思いましたが面倒なので今のところ0です。

このテンプレートはMIT Licenseです。
