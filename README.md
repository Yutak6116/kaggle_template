# Kaggle Notebook-Only Minimal Template

## 使い方

1. VS Code → Dev Containers で `.devcontainer/cpu`（Mac）または `.devcontainer/gpu`（Windows GPU）を開く。
2. `notebooks/000_setup.ipynb` を実行して、コンペ名設定 → データ DL→ 基本チェック。
3. `010_eda.ipynb` で EDA。
4. `020_train.ipynb` で学習（分類/回帰の超最小実装）。
5. `030_infer_submit.ipynb` で推論＆提出 CSV を作成。

## 前提

- Kaggle API: `~/.kaggle/kaggle.json`（権限 600）。
- 依存は Notebook 内セル or Dockerfile で固定。

```
<repo-root>/
├── .devcontainer/
│   ├── cpu/
│   │   ├── Dockerfile
│   │   └── devcontainer.json
│   └── gpu/
│       ├── Dockerfile
│       └── devcontainer.json
├── .gitignore
├── README.md
├── notebooks/
│   ├── 000_setup.ipynb           # 競技名設定・依存導入・データDL
│   ├── 010_eda.ipynb             # EDA
│   ├── 020_train.ipynb           # 学習（分類/回帰 自動判別の最小実装）
│   └── 030_infer_submit.ipynb    # 推論＆submission.csv出力
├── input/                        # Kaggleデータ (Git無視)
├── working/                      # 中間物・モデル (Git無視)
└── submissions/                  # 提出ファイル
```
