---
lab:
    title: '不公平を検出して軽減する'
---
# 不公平を検出して軽減する

多くの場合、機械学習モデルは意図的でないバイアスをカプセル化し、不公平が生じる可能性があります。たとえば、患者が糖尿病の検査を受けるべきかどうかを予測する機械学習モデルは、ある年齢層では他の年齢層よりも正確に予測します。その結果、患者集団の一部が適切な予防的健康診断を受けられなかったり、不必要な臨床検査を受けたりすることになります。

## 開始する前に

まだ行っていない場合は、*[Azure Machine Learning Workspace を作成する](01-create-a-workspace.md)* の演習を完了して、Azure Machine Learning ワークスペースとコンピューティング インスタンスを作成し、この演習に必要なノートブックのクローンを作成してください。

## Jupyter を開く

Azure Machine Learning Studio の **ノートブック** ページを使用してノートブックを実行することもできますが、*Jupyter* のような、より完全な機能を備えたノートブック開発環境を使用する方が生産性が高いことが多いです。

1. [Azure Machine Learning Studio](https://ml.azure.com)で、ワークスペースの **コンピューティング** ページを表示し、**コンピューティング インスタンス** タブで、まだ実行されていないコンピューティング インスタンスを起動します。
2. コンピューティング インスタンスの実行時に、**Jupyter** リンクをクリックして、新しいブラウザー タブで Jupyter のホーム ページを開きます。

## Fairlearn と Azure Machine Learning を使用して不公平を検出する

この演習では、モデルの公平性を評価するためのコードをノートブックで提供します。

1. Jupyter ホーム ページで、ノートブック リポジトリを複製した **Users/mslearn-dp100** フォルダーを参照し、**不公平を検出する** ノートブックを開きます。
2. 次に、Notebook 内の注意事項を読み、各コード セルを順番に実行します。
3. ノートブック内のコードの実行が終了したら、**ファイル** メニューの **閉じて停止** をクリックして閉じ、Python カーネルをシャットダウンします。その後、すべての Jupyter ブラウザー タブを閉じます。

## クリーンアップ

Azure Machine Learning での作業が終わったら、Azure Machine Learning Studio の **コンピューティング** ページで、**コンピューティング インスタンス** タブを選択し、**停止**をクリックしてシャットダウンします。それ以外の場合は、次のラボ用に実行したままにします。
