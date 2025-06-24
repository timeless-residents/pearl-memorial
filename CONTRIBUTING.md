# Contributing to Pearl Memorial

## GitHub Flow ブランチ戦略

このプロジェクトではGitHub Flowを採用し、コードの安全性と品質を保っています。

### ブランチ構成

- **main** - プロダクション環境のコード（保護されています）
- **develop** - 開発用のメインブランチ
- **feature/** - 新機能開発用のブランチ
- **bugfix/** - バグ修正用のブランチ
- **hotfix/** - 緊急修正用のブランチ

### 開発フロー

1. **新機能の開発**
   ```bash
   # developブランチから新しいfeatureブランチを作成
   git checkout develop
   git pull origin develop
   git checkout -b feature/your-feature-name
   ```

2. **変更のコミット**
   ```bash
   git add .
   git commit -m "Add: 機能の説明"
   git push origin feature/your-feature-name
   ```

3. **プルリクエストの作成**
   - GitHub上でdevelopブランチへのプルリクエストを作成
   - レビューを受ける
   - 承認後、マージ

4. **リリース準備**
   - developブランチからmainブランチへのプルリクエストを作成
   - 十分なテスト後、マージ

### コミットメッセージ規約

- `Add:` 新機能追加
- `Fix:` バグ修正
- `Update:` 機能改善
- `Remove:` 機能削除
- `Refactor:` リファクタリング
- `Doc:` ドキュメント更新

### 重要なルール

1. **mainブランチへの直接プッシュは禁止**
2. **すべての変更はプルリクエスト経由**
3. **コードレビューを必須とする**
4. **定期的にバックアップを取る**

### データ保護のベストプラクティス

- 重要な変更前には必ずブランチを作成
- 定期的にリモートリポジトリにプッシュ
- タグを使用して重要なバージョンを記録
- 複数人での作業時は頻繁にコミュニケーション

## 緊急時の対応

万が一データが失われた場合：

1. GitHubのリポジトリページで履歴を確認
2. 必要に応じて過去のコミットから復元
3. ローカルの`.git`フォルダが残っていれば、そこから復元可能