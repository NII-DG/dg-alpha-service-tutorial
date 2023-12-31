### テスト実験を行う

本ステップでは、本サービスにおける実験実行環境利用の「HelloWorld」としてテスト実験環境を構築し、NumPy を利用する簡単な計算を行います。本ステップで実践する手順を以下に示します。

1. [実験実行環境を構築する](#実験実行環境を構築する)
1. [実験の初期セットアップを行う](#実験の初期セットアップを行う)
1. [実験の制約や進め方を確認する](#実験の制約や進め方を確認する)
1. [ノートブックを作成して計算を実行する](#ノートブックを作成して計算を実行する)
1. [実験結果を研究用リポジトリに同期する](#実験結果を研究用リポジトリに同期する)
1. [実験を終了し、実験実行環境を削除する](#実験を終了し、実験実行環境を削除する)
1. [実験を再開する](#実験を再開する)

#### 本ステップを実施する前に

**本チュートリアルに基づき実施されている研究内で稼働中の実験実行環境がある場合、それらの環境上での作業と衝突する可能性があります**。それを避けるため、それらの環境を全て研究用リポジトリに同期したうえで停止し、削除しておくことをお勧めします。

#### 実験実行環境を構築する

研究フロートップページの研究フロー図中にある「実験を行う」をクリックします。それにより実験実行環境構築用ノートブック（下図）に遷移します。

![](./images/research_flow_launch_an_experiment.png)

遷移先のノートブックにて上から順にセルを実行します。「1. 実験実行環境の作成」セクションの最後の実行結果に現れる「実験実行環境を作成」ボタンをクリックします（下図）。

![](./images/research_flow_launch_an_experiment_after_all_execution.png)

それにより、コード付帯機能を利用する実験実行環境の構築が開始されます（下図）。実験実行環境の構築には 5 ~ 10 分程度かかる場合があります。

![](./images/research_flow_building_an_experiment.png)

環境構築後、自動的に実験フロートップページ（下図）に遷移します。このページでは実験実行環境における共通フローの他、実験フロー図を表示できます。

![](./images/research_flow_exp_top_page.png)

実験中は主に実験フロー図（下図。「[(先行利用)データガバナンス機能の概要](https://support.rdm.nii.ac.jp/usermanual/58/)」より引用）を利用します。

![](./images/img5808_exp_flow.png)

#### 実験の初期セットアップを行う

実験フロートップページにて上から順にセルを実行します。そうして現れた実験フロー図にある「初期セットアップを行う」をクリックし、初期セットアップ用ノートブック（下図）に遷移します。

![](./images/research_flow_exp_setting.png)

「共通メニュー」セクションのセルを実行すると、以下の項目を含むプルダウンメニューを利用できます。必要に応じてご利用ください。

* 研究リポジトリ名・実験パッケージ名を確認する
    * 初期セットアップ実行前は実験パッケージ名が `-` となっております。
* 実験フロートップページに遷移する
* GIN-forkに遷移する

それでは初期セットアップを進めます。まずは「1. 事前準備」セクションのセルを実行します。そのセルを実行後、以下の情報が求められますので、それぞれ入力して「入力を完了する」ボタンをクリックしてください（下図参照）。

|項目|値|
|:---|:---|
| GIN-fork ユーザー名 | ご自身の GIN-fork アカウント名 |
| パスワード | 上記アカウント名に対応するパスワード |
| 実験パッケージ名 | hello_world |
| テストコードフォルダ | 用意しない |
| CIツール用フォルダ | 用意しない |

![](./images/research_flow_exp_setting_inputting_pre_setting.png)

アカウント認証に成功すると、下図のようにボタンの表示が変わります。

![](./images/research_flow_exp_setting_after_authentication.png)

事前準備完了後、残りのセルを上から順に実行します。「4. 実験フロートップページへ」セクション中のセルを実行すると「実験フロートップページに遷移する」ボタンが現れます（下図）。

![](./images/research_flow_exp_setting_after_all_execution.png)

このボタンをクリックして実験フロートップページに遷移します。実験フロートップページにて「共通メニュー」セクションのセルを再実行し、プルダウンメニューから「研究リポジトリ名・実験パッケージ名を確認する」を選択すると、先ほど入力した実験パッケージ名（hello_world）が表示されます（下図）。また、実験フロー図を更新すると、実験フロー図中の「初期セットアップを行う」に「済」の印が付きます。

![](./images/research_flow_exp_top_page_common_menu_after_setting.png)

※もしセルが凍結（freeze）されており実行できない場合は、解凍したいセルを選択後、ノートブックのツールバーにある「unfreeze selected cells」ボタンクリックしてください（下図参照）。

![](./images/research_flow_exp_top_page_common_menu_before_unfreezing.png)

実験の初期セットアップが完了した時点で、研究用リポジトリの「container list」中の「experiment container」グループに実験実行環境が追加されます。実験の途中で実験実行環境にアクセスしているページを閉じてしまっても、そのリストから対象環境にアクセスして実験を再開することが可能です。

#### 実験の制約や進め方を確認する

実験フロートップページの実験フロー図中の「実験の制約や進め方を確認する」をクリックすると、本サービスを利用する実験の制約や進め方を確認するページ（下図）にアクセスすることができます。必要に応じてご活用ください。なお、実験フロートップページに戻りたい場合は、そのノートブックの最後のセルを実行することで現れる「実験フロートップページに遷移する」ボタンをクリックしてください。

![](./images/research_flow_exp_procedure.png)

#### ノートブックを作成して計算を実行する

実験フロートップページのメニューバーのうち「File」をクリックし、プルダウンメニューを表示します。プルダウンメニュー中の「Open...」をクリックし、別タブで開かれる Jupyter Notebook ページに遷移します（下図参照）。

![](./images/research_flow_exp_top_page_file_menu.png)

このページにて、「root（フォルダマーク）」→「experiments」→「hello_world」の順にクリックして実験用ディレクトリに遷移します（下図参照）。

![](./images/jupyter_notebook_exp_hello_world.png)

実験用ディレクトリには以下のファイルおよびディレクトリが存在します。

|項目|種類|説明|
|:---|:---|:---|
| input_data | ディレクトリ | 実験で利用する入力データを格納することが想定されているディレクトリです。 |
| output_data | ディレクトリ | 実験の結果として出力されるデータを格納することが想定されているディレクトリです。 |
| source | 実験のソースコードを格納することが想定されているディレクトリです。 |
| README.md | この実験パッケージ内で行われる実験や利用されるデータの説明等を記述するファイルです。 |
| Snakefile | モニタリング機能が再現性を検証する際に参照する実験手順を記述するファイルです。 |

source ディレクトリに移動し、ページ右上にある「New」プルダウンメニューを開きます。その中の「Python3 (ipykernel)」をクリックすると、新しくノートブック `Untitled.ipynb` が作成され、別タブで開かれます（下図参照）。

![](./images/jupyter_notebook_exp_source_new.png)

このノートブックは通常の Jupyter Notebook のそれと同じように操作することが可能です。ノートブックページの左上にノートブックの名前が表示されています。その名前をクリックし、`hello_world` に変更します。

最初のセルで NumPy モジュールをインポートして正弦関数を計算してみましょう。以下のコードをセルに入力し、そのセルを実行します：

```python
import numpy as np

x = np.linspace(0., np.pi, 100)
y = np.sin(x)
```

続いて matplotlib を利用して先ほど計算した正弦関数をプロットします。別のセルを作成し、以下のコードをそのセルに入力し、実行します：

```python
import matplotlib.pyplot as plt
% matplotlib inline

plt.figure(figsize=(6,5))
plt.plot(x, y)
plt.title("hello world!")
plt.xlabel("x")
plt.ylabel("y = sin(x)")
```

もう一つ別のセルを作成します。そのセルの中で計算結果（`x` と `y`）を `output_data` ディレクトリ内に NumPy 形式で保存します：

```python
np.save("../output_data/hello_world_x.npy", x)
np.save("../output_data/hello_world_y.npy", y)
```

テスト実験は以上となります。上記手順通りにテスト実験を実施すると、`hello_world.ipynb` は下図のような状態になっているはずです。

![](./images/jupyter_notebook_exp_notebook_hello_world_after_experiment.png)

#### 実験結果を研究用リポジトリに同期する

実験結果を研究用リポジトリに同期する場合、次の二つの方法があります。

* 実験を途中保存する。
* 実験終了時に保存する。

今回は頻繁に発生すると考えられる途中保存を実行します。

実験フロートップページ実験フロー図中の「実験の途中保存」をクリックし、途中保存用ノートブック（下図）に遷移します。

![](./images/research_flow_exp_save.png)

共通メニューは適宜ご利用ください。「1. 作業ログメッセージの入力」セクションのセルを実行すると、コミットメッセージの入力が求められます。今回は「hello world」と入力し、「入力完了」ボタンをクリックします（下図参照）。

![](./images/research_flow_exp_save_inputting_commit_message.png)

続いて「2. 保存準備」セクションのセルを実行します。その後「3. GIN-forkに実行結果を同期」セクションのセルを実行します。下図のように「データ同期が完了しました。」が表示されたら同期成功です。

![](./images/research_flow_exp_save_success_in_sync.png)

最後に「4. 実験フロートップページへ」セクションのセルを実行し、現れる「実験フロートップページに遷移する」ボタンをクリックして実験フロートップページに遷移します。

この時点で研究用リポジトリの `./experiments/hello_world` ディレクトリ内の `output_data` および `source` の中に先ほどのテスト実験で作成した以下のファイルが保存されていることを確認してみましょう。

* `output_data` 内
    * `hello_world_x.npy`
    * `hello_world_y.npy`
* `source` 内
    * `hello_world.ipynb`

#### 実験の説明を記述する

その実験がどのようなものであったかを実験後に理解できるようにするために、実験の説明を残しておくことが重要です。その説明が実験パッケージと一緒に保存されていれば、なお理解しやすくなるでしょう。もちろん、実験で用いた Jupyter notebook ファイルそのものに記述するのも良いでしょう。ここでは実験パッケージ内の `README.md` に実験の説明を残すという方法を採用します。

実験フロートップページにある実験フロー図中の「実験の説明を記述する」をクリックし、説明記述用のノートブック（下図）に遷移します。

![](./images/research_flow_exp_describe_exp.png)

共通メニューは適宜ご利用ください。「1-1. 記述準備」セクションのセルを実行します。表示される「`README.md`編集画面に遷移する」ボタンをクリックし、編集画面に遷移します（下図）。

![](./images/jupyter_notebook_exp_hello_wowld_edit_readme.png)

実験の説明の書き方は研究プロジェクトによって異なります。実際に本サービスを利用してご自身の研究を行う場合は、その研究プロジェクトの作法に沿って記述することが望ましいです。本チュートリアルでは、以下の方針に従って実験用の `README.md` を作成します。

* 見出し１に実験パッケージ名を入れる。
* 以下の構成で見出し２を入れる。
    * 実験概要
    * source
    * input_data
    * output_data
* 「実験概要」見出しに実験の概要を記述する。
* 「source」見出しに、`source` ディレクトリに含まれるソースコードをリストアップする。各ソースコードに説明を加える。
    * ソースコードがない場合は「ソースコードはありません。」を記述する。
* 「input_data」見出しに、`input_data` ディレクトリに含まれる入力データをリストアップする。各データに説明を加える。
    * データがない場合は「入力データはありません。」を記述する。
* 「output_data」見出しに、`output_data` ディレクトリに含まれる実験結果データをリストアップする。各データに説明を加える。
    * データがない場合は「出力データはありません。」を記述する。

このテスト実験では次のように説明文を作成してみます。

```markdown
# hello_world

## 実験概要

この実験は「NII データガバナンス機能　機能評価試験版サービス用チュートリアル」の[「基本編：テスト実験を行う」](https://github.com/hirakinii/dg-alpha-service-tutorial/blob/main/docs/02_basic/get_started/carry_out_test_experiment.md)
に沿って行われました。

## source

* `hello_world.ipynb`
    * NumPy を用いて正弦関数を計算し、プロットします。

## input_data

入力データはありません。

## output_data

以下の実験結果が含まれております。

* `hello_world_x.npy`
    * 角度に対応する値が含まれています。
    * 値の単位はラジアンです。
    * `np.load` 関数を利用することで読み込むことが可能です。
* `hello_world_y.npy`
    * `hello_world_x.npy` に含まれる値を `np.sin` 関数に入力して計算された値が含まれています。
    * 値の単位はありません。
    * `np.load` 関数を利用することで読み込むことが可能です。

```

以上の文を入力した後、`README.md` 編集画面中のメニューバーから「File」→「Save」をクリックして更新内容を保存します。なお、Jupyter Notebook のキーボードショートカットを利用して更新内容を保存することも可能です。

更新内容の保存後、`README.md` 編集画面を閉じて説明記述用のノートブックに移動します。そして「2. GIN-forkに実行結果を同期」セクションのセルを実行します。「データ同期が完了しました。」が表示されたら同期成功です。

最後に「3. 実験フロートップページへ」セクションのセルを実行し、現れる「実験フロートップページに遷移する」ボタンをクリックして実験フロートップページに遷移します。

#### Snakefileに実験手順を記述する

2023/8/30 時点では Snakefile を利用した検証を行うことはできませんが、Snakefile に関する勉強も兼ねてファイルの内容を修正します。

実験フロートップページにある実験フロー図中の「Snakefileに実験手順を記述する」をクリックし、実験手順記述用のノートブック（下図）に遷移します。

![](./images/research_flow_exp_describe_snakefile.png)

共通メニューは適宜ご利用ください。「1-1. 記述準備」セクションのセルを実行すると、二つのボタンが表示されます。

* 実験パッケージのSnakefileファイル編集画面に遷移する
* Snakefileの記述マニュアルに遷移する

Snakefileの記述マニュアルは適宜ご参照下さい。「実験パッケージのSnakefileファイル編集画面に遷移する」ボタンをクリックし、編集画面に遷移します（下図）。

![](./images/jupyter_notebook_exp_hello_world_edit_snakefile.png)

このテスト実験では `source/hello_world.ipynb` をソースコードとして二つの実験結果（`hello_world_x.npy`、`hello_world_y.npy`）を生成しました。そのことを考慮して Snakefile を以下のように記述します。

```
rule hello_world:
    output:
        "output/hello_world_x.npy"
        "output/hello_world_y.npy"
    notebook:
        "source/hello_world.ipynb"
```

以上の文を入力して更新内容を保存します。その後 Snakefile の編集画面を閉じて実験手順記述用のノートブックに移動します。そして「2. GIN-forkに実行結果を同期」セクションのセルを実行します。「データ同期が完了しました。」が表示されたら同期成功です。

最後に「3. 実験フロートップページへ」セクションのセルを実行し、現れる「実験フロートップページに遷移する」ボタンをクリックして実験フロートップページに遷移します。

#### 実験を終了し、実験実行環境を削除する

実験を終了するとき、再現性の確保や再実験を行う場合に備えて、その実験が行われた環境構成を保存しておくことが望ましいです。本サービスではそれらの操作がボタンクリックのみで完結します。

実験フロー図中の「実験を終了する」をクリックし、実験終了用ノートブック（下図）に遷移します。

![](./images/research_flow_exp_finish.png)

このノートブック内でセルを上から順に実行します。「2-1. 当実行環境の確認」セクションのセルの実行後に、現在実験を行っている環境のタグが表示されます。JupyterHub のサーバー管理ページ（下図）に遷移し、そのタグに対応する環境を stop & delete します。これにて実験実行環境を削除できます。

![](./images/jupyter_hub_servers.png)

※実験実行環境削除後、実験実行環境にはアクセスできなくなります。そのため実験フロー用ノートブックを開いているページにて下図のように「Dead kernel」ダイアログが表示される場合があります。この表示を無視して当該ノートブックを閉じていただいて問題ございません。

![](./images/research_flow_exp_dead_kernel_dialog.png)

#### 実験を再開する

本ステップの最後に、実験を再開する手順を示します。研究用リポジトリの「container list」の「experiment container」グループにある「rebuild」ボタン（下図）をクリックし、実験実行環境用のコンテナを構築します。

![](./images/container_list_after_deletion_of_exp_hello_world.png)

そのコンテナの構築の完了後、自動的に再実験用のページ（下図）に遷移します。

![](./images/research_flow_rebuild_container_exp.png)

共通メニューは適宜ご利用ください。「1. 事前準備」セクションのセルを実行します。出力されるフォームに以下の情報を入力して「入力を完了する」ボタンをクリックします（下図参照）。そのボタンの文字が「入力を受け付けました。次の手順へお進みください。」に変われば認証成功です。


![](./images/research_flow_rebuild_container_exp_inputting_setting.png)

「2. 初期セットアップ」セクションのセルを実行します。続いて「3. 実行結果をGIN-forkに同期」セクションのセルを実行します。「データ同期が完了しました。」が表示されたら同期成功です。

「4. 実験フロートップページへ」セクションのセルを実行し、現れるボタンをクリックして実験フロートップページに遷移します。遷移先である実験フロートップページの「共通メニュー」セクションのセルを実行し、現れるプルダウンメニューから「研究リポジトリ名・実験パッケージ名を確認する」を選択します。その結果として現れる実験パッケージ名が、ご自身が選択したものと同じであることを確認してください。

後はこれまでに示したような手順で再実験を行うことが可能です。

#### まとめ

本ステップではリサーチフローを利用して、実験実行環境の構築、実験実施、実験の終了までの手順を試しました。

本ステップを完了したら[次のステップに進みましょう](./carry_out_main_experiment.md)。
