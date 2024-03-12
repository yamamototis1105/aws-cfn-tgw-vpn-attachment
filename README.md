## 概要
　本コードは、TGW VPN Attachmentを作成するCloud Formationテンプレートのサンプルです。<br/>
以下の通り、TGW VPN AttachmentでTGW～EC2(Catalyst 8000v)間を接続します。<br/>

![vpn-topology](https://github.com/yamamototis1105/aws-cfn-tgw-vpn-attachment/assets/114621183/91298bb7-3b00-4bb6-870f-c5984301c4c8)

## 利用方法
### スタック作成時
1. Cloud Formation > スタックへアクセスし、スタックの作成ボタンを押下してください。
1. 「tgw-vpn-attachment.json」をアップロードし、次へボタンを押下してください。
1. スタック名は任意の名称、スタックパラメータは「(Catalyst 8000vのAMI ID)」と「(VPN ConnectionのPSK)」を入力し、次へボタンを押下してください。
1. スタックオプションはデフォルトのままで、次へボタンを押下してください。
1. 送信ボタンを押下してください。
1. VPC > Site-to-Site VPN接続へアクセスし、VPN Connectionを選択のうえ設定をダウンロードしてください。
1. 設定をRouterに投入してください。
<br/>

### スタック削除時
1. Cloud Formation > スタックへアクセスし、スタックを選択のうえ削除ボタンを押下してください。
1. 1度目は失敗で終了しますので、VPC > Transit Gatewayへアクセスし、Transit Gatewayを選択のうえ削除ボタンを押下してください。
1. 2度目は削除失敗リソースをスキップのうえ削除ボタンを押下してください。

## 関連技術
<img src="https://img.shields.io/badge/AWS-Cloud_Formation-blue"></img>


