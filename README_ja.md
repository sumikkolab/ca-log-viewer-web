<h1 align="center">CA Log Viewer</h1>

<p align="center">
  Conditional Access のサインインログを、現場で読める。Windows デスクトップでローカル処理。
</p>

<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows%2010%2F11-blue" />
  <img alt=".NET 8" src="https://img.shields.io/badge/.NET-8.0-purple" />
  <img alt="License" src="https://img.shields.io/badge/license-Proprietary-lightgrey" />
</p>

<p align="center">
  <a href="README.md">English version</a>
</p>

---

## 概要

**CA Log Viewer** は、Microsoft Entra ID のサインインログを Microsoft Graph 経由で取得し、**Conditional Access (CA) 関連の項目** (CA 評価結果 / 適用ポリシー / 端末準拠状態) を現場の管理者が読みやすい UI と HTML 監査レポートで可視化する Windows デスクトップアプリです。

- **ローカル処理のみ**: Microsoft Graph 以外への外部送信なし
- **PII 保護**: UPN 平文を DB に保存せず、表示は DPAPI 短期暗号化キャッシュ (TTL 7 日) 経由
- **HTML 監査レポートに 3 軸集約表**: ユーザー別 / アプリ別 / ポリシー別 (上位 20 + 他)
- **日本語 / 英語 UI**: 完全多言語対応
- **デモモード**: 110 件 / 6 シナリオ、`*.example` ドメイン + RFC 5737 IP のみ (Microsoft Store 配布版には含まれません)

## クイックリンク

- 🌐 製品ページ: <https://ca-log-viewer.sumikkolab.com/>
- 📖 マニュアル: <https://ca-log-viewer.sumikkolab.com/manual/>
- 🔒 プライバシーポリシー: <https://ca-log-viewer.sumikkolab.com/privacy-policy.html>
- 📋 利用規約: <https://ca-log-viewer.sumikkolab.com/terms-of-use.html>
- 🛟 サポート: <https://ca-log-viewer.sumikkolab.com/support.html>

## 主な機能

- Microsoft Graph 経由で Entra ID サインインログ取得 (委任認証、`AuditLog.Read.All`)
- Conditional Access 評価結果の分類
- サインインごとの適用ポリシー一覧
- 端末準拠状態
- 統一フィルタ: 期間 / ユーザー / CA 状態 / 判定 / 端末 / 特殊条件、複数選択 OR 対応
- 詳細パネル 7 ブロック + 結論 (6 段階優先順位)
- HTML 監査レポート + 集約表 (ユーザー別 / アプリ別 / ポリシー別、上位 20 + 他)
- CSV 出力
- デモモード (実テナント不要)
- 日本語 / 英語 UI 完全対応

## 必要な Microsoft Graph 権限

- `AuditLog.Read.All`
- `Policy.Read.ConditionalAccess`
- `User.Read.All`

## ステータス

リリース準備中。Microsoft Store への公開を準備しています。

## 連絡先

メール: support@sumikkolab.com

---

&copy; 2026 Sumikko Lab
