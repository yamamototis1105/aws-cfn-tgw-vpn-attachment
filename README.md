## 概要
　本コードは、TGW VPN Attachmentを作成するCloud Formationテンプレートのサンプルです。<br/>
以下の通り、TGW VPN AttachmentでTGW～EC2(Catalyst 8000v)間を接続します。<br/>

![vpn-topology](https://github.com/yamamototis1105/aws-cfn-tgw-vpn-attachment/assets/114621183/91298bb7-3b00-4bb6-870f-c5984301c4c8)

## 利用方法
* スタック作成時
  * Cloud Formationへアクセスし、「tgw-vpn-attachment.json」をアップロードしてください。
  * スタックパラメータとして、EC2(Catalyst 8000v)のAMI ID、VPN ConnectionのPSKを入力してください。
  * スタックオプションはデフォルトのままで、確認のうえ送信ボタンを押下してください。
  * VPCへアクセスし、VPN Connectionを選択のうえコンフィグをダウンロードし、Routerへ投入してください。
<br/>

* スタック削除時
  * Cloud Formationへアクセスし、スタックを選択のうえ削除ボタンを押下してください。
  * スタック削除が失敗するため、VPCへアクセスし、TGWのみ手動で削除してください。

## 関連技術
<img src="https://img.shields.io/badge/AWS-Cloud_Formation-blue"></img>


