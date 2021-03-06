# 項目の出現回数

**summary.py** を実行すると **python/data/stats.txt** に項目の出現回数が書かれます。

同じ内容がJSONファイルとして **python/data/stats.json** にも書かれます。

出現回数は報告書の種類別、会計基準別、コンテスト別に集計されます。

報告書の種類は、有価証券報告書か四半期報告書です。

会計基準は、**Japan GAAP** 、 **IFRS**  、 **US GAAP** のいずれかです。

コンテストは、[コンテキスト](context.md)をご覧ください。

以下はstats.txtの例で、 **有価証券報告書** の **Japan GAAP** の **当期連結期間** に現れた項目の情報が書かれています。

```
--------------------------------------------------------------------------------
報告書      : 有価証券報告書
--------------------------------------------------------------------------------

------------------------------------------------------------
会計基準    : Japan GAAP
------------------------------------------------------------

----------------------------------------
コンテキスト: コンテキスト: 当期連結期間
----------------------------------------
	"jppfs_cor:DepreciationSGA", # 減価償却費 | 減価償却費、販売費及び一般管理費 | monetaryItemType | 6314
```

最後の行の意味は以下のとおりです。

```eval_rst
======================  ===================================
項目                     値
======================  ===================================
項目のID                 jppfs_cor:DepreciationSGA
ラベル                   減価償却費
冗長ラベル                減価償却費、販売費及び一般管理費
型                       monetaryItemType
出現回数                  6314
======================  ===================================
```

※ 上記の減価償却費は損益計算書の減価償却費ですが、キャッシュ・フロー計算書の減価償却費は冗長ラベルが「減価償却費、営業活動によるキャッシュ・フロー」になっています。
