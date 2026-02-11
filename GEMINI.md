# Gemini CLI コンテキスト: github-readme-stats プロジェクト

このドキュメントは、`github-readme-stats` プロジェクトの概要、技術スタック、ビルドと実行方法、および開発規約を Gemini CLI エージェントが理解するためのコンテキストを提供します。

## プロジェクト概要

`github-readme-stats` は、GitHub のプロフィールや README に埋め込むことができる、動的に生成される GitHub 統計カードを提供するプロジェクトです。ユーザー名と各種パラメータに基づいて、GitHub の統計情報 (スター数、コミット数、プルリクエスト数など) を表示する SVG 画像を生成します。

-   **目的**: GitHub ユーザーが自身の活動を視覚的に表現するための統計カードを提供。
-   **主要技術**:
    -   **バックエンド**: Node.js (JavaScript)
    -   **フレームワーク**: Vercel (サーバーレス機能としてのデプロイ)
    -   **テスト**: Jest
    -   **コードフォーマット**: Prettier
    -   **リンティング**: ESLint
-   **アーキテクチャ**:
    Vercel のサーバーレス機能としてデプロイされ、`/api` エンドポイントへのリクエストに応じて動的に統計カードを生成し、SVG 形式で応答します。

## ビルドと実行

プロジェクトの操作は `npm` スクリプトを通じて行われます。

### 依存関係のインストール

```bash
npm install
```

### テスト

-   **全テストの実行 (カバレッジ含む)**:
    ```bash
    npm test
    ```
-   **テストの監視実行 (ファイル変更時)**:
    ```bash
    npm run test:watch
    ```
-   **スナップショットテストの更新**:
    ```bash
    npm run test:update:snapshot
    ```
-   **E2E テストの実行**:
    ```bash
    npm run test:e2e
    ```
-   **ベンチマークテストの実行**:
    ```bash
    npm run bench
    ```

### コードフォーマット

-   **コードの自動フォーマット**:
    ```bash
    npm run format
    ```
-   **コードのフォーマットチェック**:
    ```bash
    npm run format:check
    ```

### リンティング

-   **コードのリンティング実行**:
    ```bash
    npm run lint
    ```

### その他のスクリプト

-   **テーマドキュメントの生成**:
    ```bash
    npm run theme-readme-gen
    ```
-   **テーマのプレビュー**:
    ```bash
    npm run preview-theme
    ```
-   **古いテーマ関連プルリクエストのクローズ**:
    ```bash
    npm run close-stale-theme-prs
    ```
-   **言語 JSON ファイルの生成**:
    ```bash
    npm run generate-langs-json
    ```

## 開発規約

-   **コードスタイル**: Prettier を使用して一貫したコードフォーマットを維持しています。`npm run format` コマンドで自動整形が可能です。
-   **コード品質**: ESLint を使用してコードの潜在的な問題やスタイル違反を検出します。`npm run lint` コマンドで実行できます。
-   **テストプラクティス**: Jest を用いた単体テスト、E2E テスト、スナップショットテスト、ベンチマークテストが広範囲に実施されており、高いコード品質と信頼性を保証しています。
-   **貢献ガイドライン**: `CONTRIBUTING.md`、`CODE_OF_CONDUCT.md`、`SECURITY.md` ファイルが提供されており、外部からの貢献やセキュリティ対策に関する明確なガイドラインが示されています。
-   **Git フック**: Husky と lint-staged を使用し、コミット前にコードのフォーマットとリンティングを自動的に実行することで、リポジトリへのプッシュ前に品質を保証しています。
