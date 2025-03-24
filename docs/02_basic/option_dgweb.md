## （オプション）DG-Webを利用したメタデータ検証

リサーチフローを利用せず、DG-Webを利用してガバナンスシートの作成からメタデータの登録、検証までを一連の流れで実施します。

本ステップで実践する手順を以下に示します。

1. [DG-Webにアクセスする際に学認認証を行う](#DG-Webにアクセスする際に学認認証を行う)
1. [DG-Webを利用する準備を行う](#dg-webを利用する準備を行う)
1. [ガバナンスシートを作成する](#ガバナンスシートを作成する)
1. [メタデータを入力する](#メタデータを入力する)
1. [メタデータを検証する](#メタデータを検証する)
* [DG-Webで作成されるファイルの確認](#dg-webで作成されるファイルの確認)
* [（オプション）検証一覧を表示する](#オプション検証一覧を表示する)
* [まとめ](#まとめ)

### DG-Webにアクセスする際に学認認証を行う
[DS画面](https://web.stg.dg.nii.ac.jp)を表示します。
表示されたらGakuNin RDM IdPまたはOrthrosのIdPを選択します。
本チュートリアルではGakuNin RDM IdPを選択します。

| ![](./get_started/images/option_dgweb_idp_select.png) |
|---|

IdP認証画面でユーザ名とパスワードを入力し、Loginボタンをクリックします。

| ![](./get_started/images/option_dgweb_input_login_info.png) |
|---|

ログインに成功するとDG-Webにアクセスされます。

| ![](./get_started/images/option_dgweb_auth_01.png) |
|---|

### DG-Webを利用する準備を行う

「Token の入力」にて「GRDM Token」の認証を行い、Gakunin RDMと紐づけを行います。

「GRDM Token」の入力フォームに、Gakunin RDMのパーソナルアクセストークンを入力し、「認証」ボタンをクリックします。

※新規でトークンを作成する場合は「[パーソナルアクセストークンを発行する](./get_started/create_project.md#パーソナルアクセストークンを発行する)」を参照してください<br>
※すでに作成済みのトークンを使用する場合は、「osf.full_write」の権限があるトークンを使用してください

| ![](./get_started/images/option_dgweb_auth_02.png) |
|---|

認証が成功すると「認証済み」となります。

「解析基盤の Token」の入力は（オプション）Governed Run 機能を利用した計算実験の再現性の検証で必要となるトークンです。<br>
本ステップでは使用しないためスキップします。

| ![](./get_started/images/option_dgweb_auth_03.png) |
|---|

GRDM Tokenの認証を行うと、「Project 一覧」にご自身がメンバーとなるプロジェクトの一覧が表示されます。

ガバナンスシートを作成するプロジェクトの「ガバナンスシートの入力に進む」をクリックし、ガバナンスシートの作成画面へ遷移します。

| ![](./get_started/images/option_dgweb_auth_04.png) |
|---|

【すでに作成済みの場合】

ガバナンスシートおよびメタデータの入力が完了している場合は、以下のように「〇〇入力済み」と表示されます。クリックすると、それぞれの作成画面に遷移します。

| ![](./get_started/images/option_dgweb_auth_05.png) |
|---|

**【ご注意】**

**ご自身がメンバーとなっているプロジェクトで、権限が「読込み」となっている場合は、ガバナンスシートとメタデータを保存する際に書込みが出来ずエラーとなります。<br>
ご自身で作成したプロジェクト以外で入力を行う場合は、事前にプロジェクトのメンバー権限をご確認ください。**

| ![](./get_started/images/option_dgweb_pj_authority.png) |
|---|

### ガバナンスシートを作成する

「ガバナンスシートの入力に進む」（または「ガバナンスシート入力済み」）をクリックすると、ガバナンスシート作成画面へ遷移します。

DG-Webでは、よく使われるルールの組み合わせをプリセットルールとしていくつか用意しております。

本ステップではプリセットルールを使用してガバナンスシートを作成します。

プリセットルールを使用しない、またはプリセットルールに加えて個別でルールをカスタマイズすることもできます。
その場合は「個別ルールを設定する」でカスタマイズしてください。

| ![](./get_started/images/option_dgweb_governanceseat_01.png) |
|---|

「プリセットルールを使う」の「個人・チーム内で利用」にチェックします。
チェック後は個別ルールを設定せずそのまま「メタデータ入力へ進む」をクリックしてメタデータ作成画面へ遷移します。

| ![](./get_started/images/option_dgweb_governanceseat_02.png) |
|---|

公開レベルプリセット「個人・チーム内で利用」をチェックした場合は「個別ルールを設定する」の以下の項目が自動的にチェックまたは選択されます。

<table>
<thead>
<tr><th>分類</th><th colspan=2>項目名</th></tr>
</thead>
<tbody>
<tr><td rowspan=4>研究プロジェクト情報</td><td colspan=2>研究プロジェクト名</td></tr>
<tr><td colspan=2>研究プロジェクトへの参加研究者</td></tr>
<tr><td colspan=2>研究プロジェクトの URL</td></tr>
<tr><td colspan=2>研究プロジェクトのライセンス</td></tr>
<tr><td rowspan=4>ファイル情報</td><td colspan=2>ファイル名</td></tr>
<tr><td colspan=2>作成日</td></tr>
<tr><td colspan=2>URL</td></tr>
<tr><td colspan=2>ハッシュ値：SHA-256</td></tr>
<tr><td rowspan=3>人物情報</td><td colspan=2>氏名</td></tr>
<tr><td colspan=2>所属</td></tr>
<tr><td colspan=2>メールアドレス</td></tr>
<tr><td>機関情報</td><td colspan=2>機関名</td></tr>
<tr><td>資金配分機関情報</td><td colspan=2>資金配分機関名</td></tr>
<tr><td rowspan=2>コードの再実行性</td><td>再実行性のレベル</td><td>設定しない</td></tr>
<tr><td>再実行検証で利用するファイルバージョン</td><td>最新バージョン</td>
</tbody>
</table>

### メタデータを入力する

「メタデータ入力へ進む」（または「メタデータ入力済み」）をクリックすると、メタデータの入力画面へ遷移します。

| ![](./get_started/images/option_dgweb_metadata_01.png) |
|---|

各研究支援機関（FA）や所属の学術機関などから指定されているルールに従ってメタデータの入力を行います。

本ステップでは以下の項目に値を入力します。

<table>
<thead>
<tr><th colspan=2>項目名</th><th>値</th></tr>
</thead>
<tbody>
<tr><td colspan=3><b>研究に関するメタデータの入力</b></td></tr>
<tr><td colspan=2>プロジェクト名</td><td>チュートリアルプロジェクト</td></tr>
<tr><td colspan=2>プロジェクトの説明</td><td>チュートリアル用のプロジェクト</td></tr>
<tr><td colspan=2>プロジェクトの分野</td><td>（プルダウンから選択）ライフサイエンス</td></tr>
<tr><td colspan=2>プロジェクトのリンク</td><td>http&#58;//tutorial.ac.jp/pj/2024/tutorial/</td></tr>
<tr><td colspan=2>プロジェクトのRAiD</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>プロジェクトの開始日</td><td>（空欄とします）</td></tr>

<tr><td colspan=3><b>プロジェクトメンバー</b></td></tr>
<tr><td colspan=2>名前</td><td>研究太郎</td></tr>
<tr><td colspan=2>メールアドレス</td><td>taro_k@tutorial.ac.jp</td></tr>
<tr><td colspan=2>ORCID ID</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>e-Rad 研究者番号</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>所属先（名前）</td><td>チュートリアル研究所</td></tr>
<tr><td colspan=2>所属先（住所）</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>所属先（ROR ID）</td><td>（空欄とします）</td></tr>

<tr><td colspan=3><b>プロジェクトに紐づくDMP</b></td></tr>
<tr><td colspan=2>データ番号</td><td>1</td></tr>
<tr><td colspan=2>データの説明</td><td>チュートリアル用の実験</td></tr>
<tr><td rowspan=7>データの作成者</td><td>名前</td><td>研究太郎</td></tr>
<tr><td>メールアドレス</td><td>taro_k@tutorial.ac.jp</td></tr>
<tr><td>ORCID ID</td><td>（空欄とします）</td></tr>
<tr><td>e-Rad 研究者番号</td><td>（空欄とします）</td></tr>
<tr><td>所属先（名前）</td><td>チュートリアル研究所</td></tr>
<tr><td>所属先（住所）</td><td>（空欄とします）</td></tr>
<tr><td>所属先（ROR ID）</td><td>（空欄とします）</td></tr>

<tr><td rowspan=7>データ管理者</td><td>名前</td><td>管理次郎</td></tr>
<tr><td>メールアドレス</td><td>jiro_k@tutorial.ac.jp</td></tr>
<tr><td>ORCID ID</td><td>（空欄とします）</td></tr>
<tr><td>e-Rad 研究者番号</td><td>（空欄とします）</td></tr>
<tr><td>所属先（名前）</td><td>チュートリアル研究所</td></tr>
<tr><td>所属先（住所）</td><td>（空欄とします）</td></tr>
<tr><td>所属先（ROR ID）</td><td>（空欄とします）</td></tr>

<tr><td rowspan=3>データ管理機関</td><td>名前</td><td>チュートリアル研究所</td></tr>
<tr><td>住所</td><td>（空欄とします）</td></tr>
<tr><td>ROR ID</td><td>（空欄とします）</td></tr>

<tr><td rowspan=3>データのライセンス情報</td><td>名前</td><td>（空欄とします）</td></tr>
<tr><td>URL</td><td>（空欄とします）</td></tr>
<tr><td>コピーライト表記</td><td>（空欄とします）</td></tr>

<tr><td rowspan=11>データのアクセス権情報</td><td>conditionOfAccess</td><td>未選択</td></tr>
<tr><td>dataAvailable</td><td>（空欄とします）</td></tr>
<tr><td>dataAccessRequirements</td><td>（空欄とします）</td></tr>
<tr><td>概要サイズ</td><td>（空欄とします）</td></tr>
<tr><td>連絡先</td><td>（空欄とします）</td></tr>
<tr><td>データの生成方法</td><td>（空欄とします）</td></tr>
<tr><td>データのフォーマット</td><td>（空欄とします）</td></tr>
<tr><td>DMP種別・フォーマット名</td><td>（空欄とします）</td></tr>
<tr><td>DMPフォーマット提供機関（名前）</td><td>DMPフォーマット提供機関名</td></tr>
<tr><td>DMPフォーマット提供機関（住所）</td><td>（空欄とします）</td></tr>
<tr><td>DMPフォーマット提供機関（ROR ID）</td><td>（空欄とします）</td></tr>

<tr><td colspan=3><b>プロジェクトへの研究資金提供機関</b></td></tr>
<tr><td colspan=2>Funder ID</td><td>http&#58;//dx.doi.org/12.34567/123456789012</td></tr>
<tr><td colspan=2>名前</td><td>研究資金提供機関名</td></tr>
<tr><td colspan=2>住所</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>ROR ID</td><td>（空欄とします）</td></tr>

<tr><td colspan=3><b>プロジェクトが利用した研究費または研究資金プログラムの情報</b></td></tr>
<tr><td colspan=2>名前</td><td>研究資金プログラムtutorial</td></tr>
<tr><td colspan=2>説明</td><td>チュートリアル用研究資金プログラム</td></tr>
<tr><td colspan=2>体系的課題番号</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>URL</td><td>（空欄とします）</td></tr>
<tr><td rowspan=4>研究資金提供機関</td><td>Funder ID</td><td>http&#58;//dx.doi.org/12.34567/123456789012</td></tr>
<tr><td>名前</td><td>研究資金提供機関名</td></tr>
<tr><td>住所</td><td>（空欄とします）</td></tr>
<tr><td>ROR ID</td><td>（空欄とします）</td></tr>

<tr><td colspan=3><b>プロジェクト配下のファイル全てに共通するライセンス情報</b></td></tr>
<tr><td colspan=2>名前</td><td>チュートリアル研究所</td></tr>
<tr><td colspan=2>URL</td><td>http&#58;//tutorial.ac.jp/</td></tr>
<tr><td colspan=2>コピーライト表記</td><td>© 2024 tutorial research institute</td></tr>

<tr><td colspan=3><b>プロジェクト配下のファイル全てに共通するアクセス権情報</b></td></tr>
<tr><td colspan=2>conditionOfAccess</td><td>未選択</td></tr>
<tr><td colspan=2>dataAvailable</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>dataAccessRequirements</td><td>（空欄とします）</td></tr>

<tr><td colspan=3><b>プロジェクト配下のファイル</b></td></tr>
<tr><td colspan=2>名称</td><td>チュートリアルプロジェクトファイル</td></tr>
<tr><td colspan=2>説明</td><td>チュートリアルのプロジェクトファイル</td></tr>
<tr><td colspan=2>ファイルの分野</td><td>（プルダウンから選択）ライフサイエンス</td></tr>
<tr><td colspan=2>ファイルの作成日</td><td>2024-08-01</td></tr>
<tr><td colspan=2>ファイルの最終更新日</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>バージョン</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>MIMEフォーマット</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>SHA-256ハッシュ</td><td>92689dd92b4c5244b3ca9453fb0075d00837ebbafc03c45943ab8859ca4ac735</td></tr>
<tr><td colspan=2>ファイルサイズ</td><td>（空欄とします）</td></tr>
<tr><td rowspan=7>ファイルの作成者</td><td>名前</td><td>研究太郎</td></tr>
<tr><td>メールアドレス</td><td>taro_k@tutorial.ac.jp</td></tr>
<tr><td>ORCID ID</td><td>（空欄とします）</td></tr>
<tr><td>e-Rad 研究者番号</td><td>（空欄とします）</td></tr>
<tr><td>所属先（名前）</td><td>チュートリアル研究所</td></tr>
<tr><td>所属先（住所）</td><td>（空欄とします）</td></tr>
<tr><td>所属先（ROR ID）</td><td>（空欄とします）</td></tr>
<tr><td colspan=2>GRDMにおけるファイルパス</td><td>/data/tutorial/</td></tr>
<tr><td colspan=2>ファイルのURL</td><td>https&#58;//rdm.nii.ac.jp/1a2b3/</td></tr>
<tr><td colspan=2>DOI</td><td>（空欄とします）</td></tr>
</tbody>
</table>

項目への入力が完了後、「検証へ進む」をクリックします。
「送信中」となりますので、画面が切り替わるまでしばらくお待ちください。

| ![](./get_started/images/option_dgweb_metadata_02.png) |
|---|

### メタデータを検証する

「検証へ進む」をクリックすると検証が自動的に実行され、検証結果画面に遷移します。

検証結果に表示された "id" が検証IDです。<br>
"status" が ”success” となっていれば検証が成功となります。

| ![](./get_started/images/option_dgweb_validation_success.png) |
|---|

"status" が ”failure” となってしまった場合、よくあるケースとしてメタデータに入力漏れがある可能性があります。<br>
"isValid" が false となっている箇所の "message" の内容を確認後、メタデータ入力画面に戻り該当箇所のメタデータを入力して再度検証を実施してください。

| ![](./get_started/images/option_dgweb_validation_failure_01.png) |
|---|

| ![](./get_started/images/option_dgweb_validation_failure_02.png) |
|---|

### DG-Webで作成されるファイルの確認

DG-Webで作成したガバナンスシートやメタデータ、検証結果は、Gakunin RDMの選択したプロジェクトの[NII Storage]配下の[.dg]フォルダに保存されます。

| ファイル名 | 説明 |
|:--|:--|
| gov-sheet.json | ガバナンスシートのファイルです。<br>ガバナンスシートの作成画面で「メタデータ入力へ進む」をクリックすると作成・更新されます。 |
| metadata.json | メタデータのファイルです。<br>メタデータの入力画面で「検証へ進む」をクリックすると作成・更新されます。 |
| validation-[検証ID].json | 検証の詳細が記載されたファイルです。<br>メタデータの入力画面で「検証へ進む」をクリックすると作成されます。 |
| validation-index.json | 検証結果の一覧ファイルです。<br>検証IDと検証のステータスが羅列して記載されています。<br>メタデータの入力画面で「検証へ進む」をクリックすると作成されます。 |

| ![](./get_started/images/option_dgweb_file.png) |
|---|

### （オプション）検証一覧を表示する

Project 一覧の対象プロジェクトの「検証一覧」をクリックすると、今までに実施した検証を一覧で確認することができます。

| ![](./get_started/images/option_dgweb_validation_list_01.png) |
|---|

検証IDと結果が表示されます。<br>
検証の詳細を確認する場合は検証IDをクリックしてください。検証結果画面に遷移します。

| ![](./get_started/images/option_dgweb_validation_list_02.png) |
|---|

### まとめ

本ステップではDG-Webを利用したガバナンスシートの作成からメタデータの入力、検証を実施しました。ガバナンスシートの登録から検証までを一連の流れで簡単に操作することができます。検証のみを実施したい際にご活用ください。

## 移動用リンク

* [基本編の本編](./get_started_with_dg_service.md)
* [メタデータの状態の検証を行う](./get_started/validate_metadata.md)
* [基本編のまとめ](./summary.md)


