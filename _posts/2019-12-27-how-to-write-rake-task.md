---
layout: blog
title: rake taskの書き方
---

定期実行batchなど作成する時、rake taskで作成することが多いと思います。（他にはrails runner）
基本の書き方は知ってたけど、しょうもないところで詰まったのでメモ

## 目次
- 作成方法
- 作成したrakeファイルの確認
- 実行
- :environmentとは
- 終わりに


### 作成方法

rails gコマンドで作成します。ファイル直書きでも作成出来ますが、コマンド使った方がミスもないし何かと便利。
```
$ rails g task task_name
```

すると`lib/tasks/task_name.rake`が生成されます。
```
namespace :task_name do
end
```

タスクのブロック内に処理を実装していきます。
```
namespace :task_name do
  desc "処理の説明"
  task rake_sample: :environment do
    puts "Hello, World"
  end
end
```

これで完成。後述するが、`:environment`が無いと`app`で定義した関数が使えない。
なので`:environment`を指定するケースの方が多いと思う。.

### 作成したrakeファイルの確認

```
$ rake -vT

rake annotate_routes                                # Adds the route map to routes.rb
rake app:template                                   # Applies the template supplied by LOCATION=(/path/to/template) or URL
rake app:update                                     # Update configs and some other initially generated files (or use just update:configs or update:bin)
rake assets:clean[keep]                             # Remove old compiled assets
rake assets:clobber                                 # Remove compiled assets
rake assets:environment                             # Load asset compile environment
...
# この後も延々とrake taskが並ぶ。`db:migrate`とかもrake task
```

### 実行

```
$ rake task_name:rake_sample
Hello World
```

### `:environment`とは

結論から言うと、`:environment`はRailsのアプリケーションコードを読み込むタスク。
`:environment`が無ければ`app`で定義したクラス・メソッド（例えばmodel）を呼び出すことは出来ない。
こちらの記事で分かりやすく解説してくれているので詳細はこちらを参照。
[Railsにおけるrakeタスクの:environmentについて](https://qiita.com/FumiyaShibusawa/items/11035fc640bb36a615ad)
