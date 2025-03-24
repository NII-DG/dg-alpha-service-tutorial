### データ管理計画を作成する

[前のステップ](./create_project.md)では、本チュートリアルに必要な研究用プロジェクトを作成しました。本ステップでは、そのプロジェクトで扱う研究用のデータ管理計画（DMP）を作成します。本チュートリアルでは、ガバナンスシートを DMP として扱います。ガバナンスシートとは、研究データの管理において守られるべきルールを設定するシートです。適用したいルールを一覧からチェックリスト形式で選択するだけで作成することができます。本ステップで実践する手順を以下に示します。

1. [dg-researchflowsのリポジトリをローカルにダウンロードする](#dg-researchflowsのリポジトリをローカルにダウンロードする)
1. [ファイルをアップロードする](#ファイルをアップロードする)
1. [解析環境を構築する](#解析環境を構築する)
1. [ガバナンスシートを登録する](#ガバナンスシートを登録する)

#### dg-researchflowsのリポジトリをローカルにダウンロードする

[dg-researchflowsのリポジトリ](https://github.com/NII-DG/dg-researchflows)にアクセスします。

| ![](./images/create_dmp_repository_download01.png) |
|---|

ブランチ名が「master」になっていることを確認します。<img src="./images/create_dmp_repository_download_icon.png" width="60">をクリックし、「Download ZIP」をクリックしてZIPファイルを任意の場所にダウンロードします。

| ![](./images/create_dmp_repository_download02.png) |
|---|

ダウンロードしたZIPファイルを解凍します。

#### ファイルをアップロードする

[前のステップ](./create_project.md)で作成したプロジェクトのトップページに戻り、ページ上部の「ファイル」タブをクリックしてファイル管理画面（下図）に遷移します。

| ![](./images/create_dmp_file_management.png) |
|---|

「NII Storage」を選択し、「フォルダのアップロード」をクリックします。

| ![](./images/create_dmp_select_nii_storage.png) |
|---|

[前提作業](#dg-researchflowsのリポジトリをローカルにクローンする)で取得した「dg-researchflows」フォルダ内にある、「data_governance」「data」「.binder」フォルダをそれぞれアップロードします。（所要時間：約5分）

| ![](./images/create_dmp_select_files.png) |
|---|

| ![](./images/create_dmp_uploaded_files01.png) |
|---|

| ![](./images/create_dmp_uploaded_files02.png) |
|---|
#### 解析環境を構築する

研究用プロジェクトの上部にある「アドオン」タブをクリックします。「アドオンを選択」から、「GakuNin Federated Computing Services (Jupyter)」を有効化します。

| ![](./images/create_research_env_enable_addon01.png) |
|---|

| ![](./images/create_research_env_enable_addon02.png) |
|---|

| ![](./images/create_research_env_enable_addon03.png) |
|---|

アドオンを有効化したことにより、ページ上部に「解析」タブが出現します。「解析」タブをクリックします。

| ![](./images/create_research_env_create_env01.png) |
|---|

ページ右側の「`新しい解析環境を作成: https://binder.cs.rcos.nii.ac.jp`」をクリックします。ビルド状況が「ready」になるまでお待ちください。

| ![](./images/create_research_env_create_env02.png) |
|---|

| ![](./images/create_research_env_create_env03.png) |
|---|

この操作により、ページ上部の「私の解析環境」に解析環境が出現します。

| ![](./images/create_research_env_create_env04.png) |
|---|

「起動」にある![](./images/create_research_env_create_env_jupyter_icon.png)アイコンをクリックすることで、作成した解析環境に遷移します。

| ![](./images/create_research_env_create_env05.png) |
|---|

「data_governance」フォルダ、「researchflow」フォルダを開き、「main.ipynb」をクリックし、メインメニューに遷移します。

| ![](./images/create_research_env_create_env06.png) |
|---|

| ![](./images/create_research_env_create_env07.png) |
|---|

| ![](./images/create_research_env_create_env08.png) |
|---|

#### 解析環境の初期セットアップを行う

前節の最後に開かれたメインメニューのページにて、上から順にセルを実行することで処理が進みます。セルの実行方法は Jupyter Notebook における通常のセルの実行方法と同じです。セルの実行が完了すると下図のようになります。

| ![](./images/create_research_env_setup01.png) |
|---|

「サブフロー関係図」の「研究準備」の<img src="./images/create_research_env_setup_prepare_node.png" height="15">をクリックし、研究準備サブフローメニューに遷移します。

| ![](./images/create_research_env_setup02.png) |
|---|

「サブフローメニューを表示する」のコードセルを実行し、サブフローメニューを表示します。

| ![](./images/create_research_env_setup03.png) |
|---|

#### ガバナンスシートを登録する

背景が黄色となっているフロー図に従って操作を行います。「ガバナンスシートを登録する」をクリックし、次のフローに遷移します。

| ![](./images/create_research_env_setup04.png) |
|---|

| ![](./images/create_research_env_setup05.png) |
|---|

「ガバナンスシート登録フォームを表示する」のセルを実行します。「パーソナルアクセストークンを入力してください：」と表示された場合は[パーソナルアクセストークンを発行する](./create_project.md#パーソナルアクセストークンを発行する)で作成したパーソナルアクセストークンを入力します。

| ![](./images/create_research_env_setup06.png) |
|---|

ガバナンスシート登録フォームが表示されます。

| ![](./images/create_research_env_setup07.png) |
|---|

セルの左端にカーソルを合わせると「click to scroll output, double click to hide」と表示されます。セルをクリックしてフォームの全体を表示します。

| ![](./images/create_research_env_setup08.png) |
|---|

データ管理計画としてフェーズに沿った項目にチェックをしていきます。

本チュートリアルではデフォルト値のまま登録します。本ステップ以降、ガバナンスシートはどのタイミングでも修正することができます。

デフォルト値としてチェックされる項目は以下です。

<table>
<thead>
<tr><th>分類</th><th colspan=2>項目名</th></tr>
</thead>
<tbody>
<tr><td rowspan=3>研究プロジェクト情報</td><td colspan=2>研究プロジェクト名</td></tr>
<tr><td colspan=2>研究プロジェクトへの参加研究者</td></tr>
<tr><td colspan=2>研究プロジェクトの URL</td></tr>
<tr><td rowspan=3>ファイル情報</td><td colspan=2>ファイル名</td></tr>
<tr><td colspan=2>作成日</td></tr>
<tr><td colspan=2>URL</td></tr>
<tr><td rowspan=2>コードの再実行性</td><td>再実行性のレベル</td><td>設定しない</td></tr>
<tr><td>再実行検証で利用するファイルバージョン</td><td>最新バージョン</td>
</tbody>
</table>

「保存する」をクリックします。

| ![](./images/create_research_env_setup09.png) |
|---|

「同期中です。しばらくお待ちください。」と表示されますのでしばらくお待ちください。「ガバナンスシートを保存しました。」と表示されたら完了です。

ガバナンスシートは、Gakunin RDMの[NII Storage]配下の[.dg]フォルダに「gov-sheet.json」という名前で保存されます。<br>
**解析環境には保存されませんのでご注意ください。**

| ![](./images/create_research_env_setup10.png) |
|---|

「サブフローメニューを表示する」をクリックし、サブフローメニューへ遷移します。

| ![](./images/create_research_env_setup11.png) |
|---|

サブフローメニューへ遷移後、再度「サブフローメニューを表示する」のコードセルを実行し、サブフローメニューを表示します。

完了したタスクには青いチェックマークが表示されます。ガバナンスシートの登録を実施すると、次のタスクである「解析環境を構築する」が実行可能になります。

| ![](./images/create_research_env_setup12.png) |
|---|

また、ガバナンスシートの設定値を変更することで実験フェーズ以降のサブフローのタスクが増減します。
本チュートリアルではガバナンスシートの「研究プロジェクトへの参加研究者」の設定値で行います。
ガバナンスシート登録フォームを表示し、「研究プロジェクトへの参加研究者」のチェックマークを外して保存します。

| ![](./images/govsheet_hide.png) |
|---|

保存したガバナンスシートで実験サブフローを新規作成します。
作成手順は[実験実行環境を構築する](./carry_out_test_experiment.md#実験実行環境を構築する)を参照してください。

| ![](./images/create_hide_task.png) |
|---|

作成した実験サブフローのサブフローメニューを表示します。

| ![](./images/hide_task.png) |
|---|

「研究プロジェクトへの参加研究者」のチェックを外すと「共同研究者を管理する」タスクが非表示になります。

2025/1/31時点で増減できる項目は「研究プロジェクトへの参加研究者」のみです。

#### まとめ

本ステップではリサーチフローのガバナンスシートを利用したデータ管理計画（DMP）を作成する方法を試しました。試験的な機能ではあるものの、機械可読性（machine actionability）をより強く意識した形での DMP の作成を体験いただきました。

本ステップではリサーチフローからガバナンスシートを作成しましたが、DG-Webを利用して作成することもできます。DG-Webから作成する手順は[（オプション）DG-Webを利用したメタデータ検証](../option_dgweb.md)を参照してください。

本ステップを完了したら[次のステップに進みましょう](./create_research_env.md)。
