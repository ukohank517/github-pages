# github-pages[WIP]

ローカル環境で起動する方法

## Jekyllインストール

[参考資料](https://jekyllrb.com/docs/installation/macos/)

1. Install the bundler and jekyll gems:

  ```
  gem install --user-install bundler jekyll
  ```

2. Get your Ruby version:

  ```
  $ ruby -v
  ruby 2.6.3p62 (2019-04-16 revision 67580) [universal.x86_64-darwin19]
  ```

3. Append your path file with the following, replacing the X.X with the first two  digits of your Ruby version:

  ```
  echo 'export PATH="$HOME/.gem/ruby/2.6.0/bin:$PATH"' >> ~/.bash_profile
  ```

4. Check that `GEM PATHS`: points to your home directory:

  ```
  gem env
  ```

## 必要なパッケージをインストール

```
sudo gem install eventmachine -v '1.2.7' --source 'https://rubygems.org/'
bundle install
```

## 環境構築する




