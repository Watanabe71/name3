# プロダクトゴール
 アニメ、漫画のじぶんのおすすめを投稿、共有できるアプリ

gidhub使い方
例
今回の「ランキング機能を作る #3」を例にすると、

1.Issueを作る ← 今ここ
  「ランキング機能を作る」という作業内容を登録する。
2.Issue専用のBranchを作る
  今の画像の右側、Development にある 「Create a branch」 を押す。
  ブランチ名は例えば feature/ranking でOK。
3.作ったBranchでコードを書く
  timeline.html を開いて、さっきのランキング機能などを実装する。
  このとき mainを直接編集せず feature/ranking を編集するのがポイント。
4.ある程度できたらCommitする
  例えばコミットメッセージは、
  ランキング画面を追加
  おすすめ数で並び替える機能を追加
  みたいに「何を変更したか」が分かるようにする。1回で全部CommitしなくてもOK。
5.完成したらPull Request（PR）を作る
  feature/ranking → main に「この変更をmainに入れます」という申請を出す。PRには Closes #3 と書いておくと便利。
6.確認してMergeする
  サイトがちゃんと動くか確認して問題なければ Merge pull request。これでランキング機能が main に入る。Closes #3 を設定していれば、Issue #3も自動でCloseされる。

つまりイメージは、

Issue #3「ランキング機能作ろう」
↓
Branch feature/ranking を作る
↓
そこでコードを書く
↓
Commit
↓
Pull Request
↓
Mergeしてmainに反映
↓
Issue #3 完了



左下の main をクリック
「Create new branch...」 を選ぶ
ブランチ名を feature/ranking にする
作成すると左下が feature/ranking に変わる
その状態で今変更した timeline.html を保存
ブラウザでランキング機能が動くか確認
問題なければ Commit
GitHubに Push
GitHubで Pull Request
最後に mainへMerge
