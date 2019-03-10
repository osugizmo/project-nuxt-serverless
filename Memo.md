# Memo

# VSCodeでmdプレビュー
### サイドバイサイド
- Win
［Ctrl］＋［K］→［V］

- Mac
［Command］＋［K］→［V］

### 別タブ
- Win
 ［Ctrl］＋［Shift］＋［V］

- Mac
［Shift］＋［Command］＋［V］

# Git コマンドチートシート(個々の内容は下方に記載)

## ログを見やすくする
```bash
git log --graph --all --format="%x09%an%x09%h %d %s"
```

## 以下を実行すると「git tree」で表示できる
```bash
git config --global alias.tree 'log --graph --all --format="%x09%C(cyan bold)%an%Creset%x09%C(yellow)%h%Creset %C(magenta reverse)%d%Creset %s"'
```

# プレフィックス

## 通常版
- fix：バグ修正
- hotfix：クリティカルなバグ修正
- add：新規（ファイル）機能追加
- update：機能修正（バグではない）
- change：仕様変更
- clean：整理（リファクタリング等）
- disable：無効化（コメントアウト等）
- remove：削除（ファイル）
- upgrade：バージョンアップ
- revert：変更取り消し

## スニペット

```
[prefix] 変更内容の要約（タイトル、概要）

refs #1 変更した理由（内容、詳細）
```

# 用例集

## オプションやフラグ、メニューを追加した

- Add -enable-experimental-nested-generic-types frontend flag
- Add --main-process flag to run specs in the main process
- Add Throws flag and ThrowsLoc to AbstractFunctionDecl
- Add "event" parameter for "click" handler of MenuItem
- Add File &gt; Exit menu on Windows

## ファイルを追加した

- Add npm start script
- Add build script
- Add SkUserConfig.h with blank SkDebugf macro

## メソッドや機能を追加した

- Add TypeLowering::hasFixedSize()
- Add overflow scrolling
- Add convenience API for demangling
- Add a typealias to avoid a build ordering dependency between projects
- Add a helper method mayHaveOpenedArchetypeOperands to SILInstruction

## 実装を別のものへ切り替えた

- Use args.resourcePath instead of args.devResourcePath
- Use arrays instead of while loops
- Use auto instead of repeating explicit class names
- Use weak pointer instead of manual bookkeeping
- Change all uses of 'CInt' to 'Int32' in the SDK overlay
- Change Integer#year to return a Fixnum instead of a Float to improve consistency

## 新しく何かに対応した/機能上の制約を取り払った

- Add support for closure contexts to readMetadataFromInstance()
- Add support for activating and deactivating package-specific keymaps
- Add support for launching HTML files directly
- Add support for allocators that require tensors with zero
- Make it possible to call `reflect` multiple times
- Make it possible to set a data type for variables that come out of constants
- Allow atom-pane to be shrunk independently of its contents' width
- Allow null TextEditorComponent::domNode during visibility check

## 何かを使うようにした

- Use const for util require
- Use FoldingSetNode for ProtocolType
- Use unique text editor title in window and tab titles
- Use an empty object if metadata is ~null
- Use target_link_libraries for fat executable dependencies
- Use existing flatMapToOptionalTests dataset

## より好ましい実装に改良した

- Make the clone function more generic
- Make IO faster for v8 compile cache
- Make model constructor argument to addViewProvider optional
- Make Browser::Quit more robust
- Make Menu.getApplicationMenu() public
- Improve incompatible native module error message
- Improve readability of multi-line command
- Improve folds behavior when duplicating lines
- Improve deprecated message on webPreferences options

## 何かを出来ない/しないようにした

- Don't bail reading a metadata instance if swift_isaMask isn't available
- Don't exit until the parent asks for an instance
- Don't include Parent pointer in Nominal/BoundGeneric TypeRef uniquing
- Don't use MatchesExtension for matching filters
- Don't use ES6 class for AutoUpdater windows class
- Don't use MatchesExtension for matching filters
- Avoid `distinct` if a subquery has already materialized
- Avoid infinite recursion when bad values are passed to tz aware fields

## オブジェクトの内容や挙動を確認しやすくした

- Emit capture descriptors in their own section
- Emit field metadata for @objc classes
- Emit reflection info for protocols

## Assertを追加した

- Add assert for role with app name in label
- Add assertions for no available bookmark
- Add asserts for properties

## 不要なコードを除去した

- Remove some dead code
- Remove some unused enum declaration
- Remove unused variable
- Remove unnecessary line feeds
- Remove trailing whitespace
- Remove debug statement
- Remove redundant mapType{Into,OutOf}Context() calls

## コードを移動した

- Move function signature analysis to a Util
- Move markInvalidGenericSignature() to a method on TypeChecker
- Move diagnostic for stored properties in protocols from type checking to validation
- Move Doxygen converter into a proper MarkupASTNode visitor
- Move Module require to top

## 名前を修正した

- Rename environment -&gt; environmentHelpers
- Rename watchProjectPath to watchProjectPaths
- Rename generic arguments
- s/grammarName/grammar
- fullVersion -&gt; writeFullVersion

## 小さなバグやタイポを修正した, 警告を潰した

- Fix typos
- Fix a typo
- Fix a test
- Fix typo in DevTools Extensions tutorial
- Fix DownloadingState typo
- Fix includes order
- Fix mistake in tvOS availability
- Fix cpplint warnings
- Fix wrong markdown
- Add missing return
- Add missing period in comment

## バグや好ましくない挙動を修正した

- Fix a memory leak in FSO
- Fix lifetime issues in ManagedBuffer.value
- Fix mangling for nested generic types
- Fix memory corruption in another circularity check
- Fix thread-unsafety in Process.Argument initialization
- Fix "Object has been destroyed" error in "page-title-updated" event
- Make Error.prepareStackTrace read-only (again)
- Make string slicing tests standalone
- Make sure showing success dialogs works correctly
- Make sure to emit closure bodies only once
- Make sure all native resources get freed on exit
- Make sure temp file will be cleaned up when base::Move fails

## テスト、コメント、ドキュメントを追加した

- Add tests for pending pane items
- Add validation test for projecting existentials
- Add a basic test for opening an editor in largeFileMode if &gt;= 2MB
- Add specs for moveSelectionLeft()
- Add failing spec for Menu.buildFromTemplate
- Add comment about map key/values
- Add TODO about blinkFeatures -&gt; enableBlinkFeatures
- Add a design-decisions section to the CONTRIBUTING guide
- Add style.less examples
- Add docs for app.getLocale()
- Add documentation for --proxy-bypass-list

## テストを削除した

- Remove a redundant test
- Remove an empty test

## テスト、コメントを修正した

- Fix comment
- Fix outdated comment
- Fix failing specs on Windows
- Fix PersistentVector test for powerpc64{le}
- Update specs for deferred activation hooks
- Update successor/predecessor in validation tests
- Update some tests to use LifetimeTracked instead of hand-rolled canaries

## ドキュメントを修正した

- Update README.md
- Update docs for marker callback
- Update documentation for mark*Position
- Update link to solarized-dark-syntax
- Improve documentation of `ses.cookies.set()`
- Improve readability in CSRF section of guide
- Improve spec description


# Git設定

### Git ユーザー設定 グローバル
```bash
git config --global user.name "osugizmo"
git config --global user.email "osugizmo@email.local"
```

### Git ユーザー設定 プロジェクトローカル
```bash
git config --local user.name "osugizmo"
git config --local user.email "osugizmo@email.local"
```

### Git Editor設定(vimに設定)
```bash
git config --global core.editor 'vim -c "set fenc=utf-8"'
```

### リポジトリ作成後リモートへプッシュ
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/osugizmo/project-name.git
git push -u origin master
```

### クローン
```bash
git clone https://github.com/osugizmo/project-name.git
```

### リモートから変更取得
```bash
git pull
```
or
```bash
git fetch
git merge origin/master
```

### Git Commiter変更
```bash
git commit --amend
```

### Git Author 変更
```bash
git commit --amend --author="osugizmo <osugizmo@email.local>"
git rebase --continue
git log --pretty=full
git push origin HEAD    #Push済ならgit push -f origin HEAD
```

### ファイルの登録(ステージング)
```bash
git add <ファイル名>
```

### ファイルの変更や追加をコミット
```bash
git commit -m "コミットメッセージ"
```

### ローカルの変更を確認する
```bash
git status
```
### リモートとローカルのファイルの差分を抽出する
```bash
git diff <ファイル名>
```

### commitの変更履歴をみる
```bash
git log
```

### 指定したcommitの変更点を見る
```bash
git show <コミットのハッシュ値>
```

### リモートにプッシュ
```bash
git push origin <ブランチ名>
```

### addの取り消し
```bash
git reset HEAD <ファイル名>
```

### commitの取り消し
```bash
git reset --hard HEAD^
```
--hard：コミット取り消し＋ワークディレクトリの内容も変更
--soft：コミットのみを取り消し
HEAD^：直前のコミット
HEAD~{n} ：n個前のコミット

### commitの打ち消し
```bash
git revert <コミットのハッシュ値>
```

### コミットメッセージの修正
```bash
git commit --amend "新しいコミットメッセージ"
```
### pushの取り消し
```bash
git reset --hard <戻したいコミットのハッシュ値>
git push -f
```

### ローカルでブランチを作成
```bash
git branch <ブランチ名>
```

### ローカルでブランチを切り替え
```bash
git checkout <ブランチ名>
```

### ブランチ作成 & 切り替え
```bash
git branch -b <ブランチ名>
```

### ブランチ名の変更
```bash
git branch -m <古いブランチ名> <新しいブランチ名>
```

### ブランチの削除
```bash
git branch -d <ブランチ名>
```

### ローカルのブランチをリモートに反映
```bash
git push -u origin <ローカルのブランチ名>
```

### リモートのブランチをローカル持ってくる
```bash
git branch <ブランチ名> origin/<ブランチ名>
```

### リモートのブランチをローカル持ってくる & 切り替え
```bash
git checkout -b <ブランチ名> origin/<ブランチ名>
```

### 全てのブランチを確認する
```bash
git branch -a
```

### ブランチを比較する
```bash
git diff <ブランチ名> <ブランチ名>
```

### ブランチをマージする
```bash
git merge <ブランチ名>
```

### fast-forwardの関係であっても必ずマージコミットを作る

```bash
git merge --no-ff <ブランチ名>
```
※ mergeの場合は分岐元で実行する為

### ブランチをリベースする
```bash
git rebase <ブランチ名>
```
※ rebaseの場合は分岐先のブランチで実行

### 変更点を一旦退避させる
```bash
git stash save
```

### 退避した作業の一覧を見る
```bash
git stash list
```

### 退避した作業を戻す
```bash
git stash apply <stash名>
```

### 退避した作業を消す
```bash
git stash drop <stash名>
```

### 退避した作業をすべて消す

```bash
git stash clear
```

### ファイル削除
```bash
git rm -f  <ファイル名>
```

### ファイルリネーム
```bash
git mv <元のファイル名> <変えたいファイル名>
```

### ファイルを最新のコミットの状態に戻す
```bash
git checkout HEAD <ファイル名>
```

### ファイルを指定コミットまで戻す
```bash
git checkout <コミットのハッシュ値> <ファイル名>
```

### .gitignore を無視して追加する
```bash
git add -f <ファイル名>
```

### ディレクトリだけ登録(.gitkeepをディレクトリに作成する)
```bash
touch <ディレクトリ名>/.gitkeep



