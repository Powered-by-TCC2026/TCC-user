# TCC-user

このリポジトリは、顔認識とメンバーカード自動発行システムのプロジェクトです。

## 概要

- Webカメラから新しい顔を検出した際、自動で“本物風”会員カード画像を発行します。
- カードには顔写真・氏名・会員番号・有効期限・QRコード（パスワード付きURL）・注意書きが含まれます。
- カード画像へのアクセスには個別パスワード認証が必要です。
- GitHub Pagesでカード画像のWeb確認が可能です。

##ページ

- [認証付きカード画像表示ページ](https://anyufuku.github.io/TCC-user/index.html)

## 使い方

1. `member_card_camera.py` を実行し、顔認識およびカード画像を自動発行します。
2. `cards/` フォルダに生成されたカード画像・QRコード画像が保存されます。
3. 会員はQRコードからWebページ（例: `index.html?file=USER001.png&pw=xxxxxx`）にアクセスし、カード画像を閲覧できます。

## ディレクトリ構成例

```
TCC-user/
├── member_card_camera.py      # メインの顔認識・カード発行スクリプト
├── index.html                 # GitHub Pagesの認証付きカード画像表示ページ
├── card.html                  # （用途に応じて追加可能なサブページ例）
├── cards/                     # 発行済みカード画像・QR画像
│   └── password.json          # カードごとのパスワード管理
├── faces/                     # 登録済み顔画像
├── logs/                      # 利用ログ
├── template2.png              # カードテンプレート画像
├── LICENSE                    # ライセンス（MIT）
└── README.md                  # このファイル
```

## 必要なライブラリ

- Python 3.x
- face_recognition
- OpenCV (cv2)
- Pillow
- qrcode

インストール例:
```
pip install face_recognition opencv-python pillow qrcode
```
## ライセンス

MITライセンス

---

ご意見・ご要望はIssueまたはPull Requestでお気軽にどうぞ！
