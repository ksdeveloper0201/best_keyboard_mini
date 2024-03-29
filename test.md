1 次フェーズでは下記の機能で開発をすることにします。

-   ユーザーアカウント管理
-   商品情報
-   検索機能
-   フィルタリング
-   レスポンシブデザイン
-   管理者機能
-   セキュリティ

また、優先度を考慮し、非機能要件は下記で対応します。

-   パフォーマンス
    -   Next.js の ISR や SSR を採用する
-   信頼性:
    -   システムの高い信頼性が求められる。特にユーザーアカウント管理や注文処理において、データの正確性と完全性を保つ。
-   セキュリティ:
    -   セキュリティについて認証情報は,メールアドレスとパスワードとし、パスワードはハッシュ化された値を DB に保存するものとする。
-   ユーザビリティ:
    -   直感的な操作性とするためカード ui とする想定
    -   SP 版にも対応する
-   ユーザープライバシー:
    -   ユーザーの個人情報やプライバシーに関する法令や規制を遵守し、プライバシーポリシーを作成する。

現状の要件定義の機能・非機能をテーブル形式でわかりやすくまとめてください
