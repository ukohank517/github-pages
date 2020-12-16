# github-pages[WIP]

Here shows the way you can run this application in local environment.

## Install Jekyll

[参考資料](https://jekyllrb.com/docs/installation/macos/)

手順：

0. prepare command `ruby`, but in my mac OSX, even I've already had the command by mac itself, I have to install the ruby again. You can skip this step first, if you got some error when you use gem, you can come back this step to install ruby again.

    ```bash
    $ brew install ruby # install ruby
    ```


    ```bash
    ### update settings to bash profile
    echo '########### geb ############' >> ~/.bash_profile
    echo '# brew ruby' >> ~/.bash_profile
    echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile
    echo '# For compilers to find ruby you may need to set:' >> ~/.bash_profile
    echo 'export LDFLAGS="-L/usr/local/opt/ruby/lib"' >> ~/.bash_profile
    echo 'export CPPFLAGS="-I/usr/local/opt/ruby/include"' >> ~/.bash_profile
    echo '# For pkg-config to find ruby you may need to set:' >> ~/.bash_profile
    echo 'export PKG_CONFIG_PATH="/usr/local/opt/ruby/lib/pkgconfig"' >> ~/.bash_profile
    ```

1. Install the bundler and jekyll gems:

    ```
    gem install --user-install bundler jekyll
    ```

2. Get your Ruby version:

    ```
    $ ruby -v
    ruby <version> (2019-04-16 revision 67580) [universal.x86_64-darwin19]
    ```

3. Append your path file with the following, replacing the X.X with the first two  digits of your Ruby version:

    ```
    echo 'export PATH="$HOME/.gem/ruby/<version>/bin:$PATH"' >> ~/.bash_profile
    ```

4. Check that `GEM PATHS`: points to your home directory:

    ```
    gem env
    ```

5. Install dependency packages
    ```bash
    $ gem install --user eventmachine -v '1.2.7' --source 'https://rubygems.org/'
    ```

## copy repository and build it locally

1. use git to clone repository

    ```bash
    $ git clone git@github.com:ukohank517/github-pages.git # clone repository
    ```

2. start local server

    ```bash
    $ bundle install # init dependency package
    $ bundle exec jekyll serve # start server
    ```
3. see the local page

    Open your browser, access URL `http://127.0.0.1:4000` to see the page
