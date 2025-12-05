# 問題一覧

## 状況１

```
Z:\muzudho-github.com\muzudho\exercises>git add README.md                                     
warning: safe.directory ''%(prefix)///TAKAHASHI-NAS/Share/muzudho-github.com/muzudho/exercises'' not absolute
fatal: detected dubious ownership in repository at '//TAKAHASHI-NAS/Share/muzudho-github.com/muzudho/exercises'
'//TAKAHASHI-NAS/Share/muzudho-github.com/muzudho/exercises' is owned by:
        (inconvertible) (S-1-5-21-857659277-616080319-1060950140-2002)
but the current user is:
        TAKAHASHI-PC/muzud (S-1-5-21-2230578036-862650600-2215440739-1001)
To add an exception for this directory, call:

        git config --global --add safe.directory '%(prefix)///TAKAHASHI-NAS/Share/muzudho-github.com/muzudho/exercises'
```

* VSCode の 左のサイドメニューから［Source Control］をクリック。  
* ［Manage Unsafe Repositories］ボタンをクリック。  
* 一覧から、当該フォルダー名をクリック。

```shell
## git のローカル・リポジトリーの作成
git init
                Initialized empty Git repository in //TAKAHASHI-NAS/Share/muzudho-github.com/muzudho/exercises/.git/

## git の設定の一覧
git config --global --get-all safe.directory

## ## git の設定の safe.directory 区画に追加、または ...
## git config --global --unset safe.directory //TAKAHASHI-NAS/Share/muzudho-github.com/muzudho/exercises

## git の設定を vi エディターの編集モードで編集
git config --global --edit

        ## 抜粋
        [safe]
            directory = //TAKAHASHI-NAS/Share/muzudho-github.com/muzudho/exercises

git add README.md
```
