# mirror-framework

A test scenario generation framework that **finitely enumerates test scenarios**
through domain definition and relation patterns.

Inspired by routing path computation in network algorithms,  
the core idea is: **"test scenarios can be derived by SQL-style enumeration."**

---

## About This Repository

Test scenario generation is work that tends to depend on individual experience and intuition.  
This framework formalizes that process into a finite, reproducible pipeline:  
**domain definition → boolean operation → pattern enumeration.**

What distinguishes it from conventional decision tables or CPP (cause-effect graphs)  
is that input value domains are **structured through a network routing design analogy**,  
and it includes an **explicitly defined operational model that separates the roles of human, AI, and program.**

---

## Documents

### 1. [Theory, Design Philosophy, and Role Separation](./docs/01_theory.md)

The core ideas behind the Mirror Framework.

- The claim that test scenarios can be finitely enumerated from domain and relation patterns
- How test data is generated through boolean operations
- How YAML conversion enables structured input to AI
- A role model that clearly separates human, AI, and programmatic processing

### 2. [Input Value Pattern Catalog](./docs/02_input-patterns.md)

A systematic classification of input values required for test design.

- Numeric types (integers, decimals, dates, boundary values, signed numbers)
- String types (full-width, half-width, control characters, special characters)
- HTML encoding and injection-aware classifications
- Assigning boolean flags to each pattern enables AI-driven enumeration

### 3. [E2E Screen Transition Extension](./docs/03_e2e-transition.md)

A methodology for extending the Mirror Framework — strong in unit testing —  
into integration and system testing.

- Screen transition computation inspired by optical network path design (airport EPS routing)
- Full path enumeration using adjacency tables + LEFT JOIN
- Automatic test phase classification via path cost (0=unit, 1~n=integration, max=system)
- Includes a sample adjacency table built from an actual design document

---

## About the `schemas/` Directory

The `schemas/` directory contains YAML schema definitions of the structures described in each document.  
These serve as input formats for AI-driven test scenario generation.

---

## Related Repository

- [playwright-framework-guide](https://github.com/earthHa11Queen/playwright-framework-guide)  
  Design philosophy for Playwright E2E test automation — the intended implementation target of this framework.

---

## License

[CC BY-SA 4.0](./LICENSE)

This repository handles design philosophy and documentation rather than code,  
so the Creative Commons Attribution-ShareAlike license applies.  
When citing, adapting, or redistributing, please credit the original author  
and apply the same license.

---

---

# mirror-framework（日本語）

テストシナリオをドメインとリレーションのパターンで有限的に算出する、テスト設計フレームワークです。

ネットワークルーティングアルゴリズムの経路計算から着想しており、
「テストシナリオはSQLで算出できる」という思想を中核に置いています。

---

## このリポジトリについて

テストシナリオの生成は、経験や勘に依存しがちな作業です。
本フレームワークは、その作業を **ドメイン定義 → boolean演算 → パターン算出** という
有限かつ再現可能なプロセスとして定式化します。

既存のデシジョンテーブルやCPP（原因結果グラフ）との違いは、
**入力値のドメインをネットワーク経路設計のアナロジーで構造化している**点と、
**人・AI・プログラムの役割を明確に分離した運用モデル**を持っている点にあります。

---

## ドキュメント

### 1. [思想と理論および役割分担](./docs/01_theory.md)

鏡の原理の核心となる考え方を解説します。

- テストシナリオはドメインとリレーションのパターンで有限的に算出できるという主張
- boolean演算によるテストデータ生成の仕組み
- YAML形式への変換による、AIへの構造化渡し方
- 人・AI・プログラム処理の役割分担モデル

### 2. [入力値パターンカタログ](./docs/02_input-patterns.md)

テスト設計で必要となる入力値の体系的な分類カタログです。

- 数値系（整数・小数・日付・境界値・符号）
- 文字列系（全角・半角・制御文字・特殊文字）
- HTMLエンコード・インジェクション系の考慮分類
- 各パターンにboolean設定することでAIが演算可能な形式になります

### 3. [E2E画面遷移拡張](./docs/03_e2e-transition.md)

単体テストに強い鏡の原理を、結合・総合テストに拡張する方法論です。

- 光ネットワーク経路設計（空港内EPSルーティング）から着想した画面遷移演算
- 隣接テーブル＋Left Joinによる全経路の算出モデル
- パスコスト（0=単体、1〜最大値=結合、最大値=総合）によるテスト工程の自動分類
- 実際の設計書から作成した隣接テーブルのサンプル付き

---

## schemasについて

`schemas/` ディレクトリには、各ドキュメントで解説している構造をYAMLスキーマとして定義したファイルを格納しています。AIにテストシナリオを生成させる際の入力フォーマットとして使用します。

---

## 関連リポジトリ

- [playwright-framework-guide](https://github.com/earthHa11Queen/playwright-framework-guide)  
  Playwright E2Eテスト自動化システムの設計ガイドライン。  
  本フレームワークの実装先となる Playwright フレームワーク設計思想を扱います。

---

## ライセンス

[CC BY-SA 4.0](./LICENSE)

本リポジトリはコードではなく設計思想・ドキュメントを扱うため、
Creative Commons（表示 - 継承）ライセンスを採用しています。
引用・改変・再配布の際は原著者の表示と同一ライセンスの適用をお願いします。
