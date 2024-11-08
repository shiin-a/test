##### ※「@」はブランチ名に置換する。
### ローカルにダウンロード
```
git init
git commit --allow-empty -m "."
git fetch git@github.com:shiin-a/test.git @
```

### レポジトリに追加する方法
```
git init
git commit --allow-empty -m "empty commit"
#その後いつも通りコミット
git checkout -b @
git push git@github.com:shiin-a/test.git HEAD
```

### squashする方法
```
git rebase -i 【empty commmitのコミットID】
```

### 検索方法
```
# ファイルコンテンツを検索したい場合
git grep 【検索したい文字列】 $(検索したいブランチ名)

# ファイル名を検索したい場合
for branch in $(検索したいブランチ名); do
  echo  "Branch: $branch"
  git ls-tree -r $branch
  echo  "---------------------------"
done
```
