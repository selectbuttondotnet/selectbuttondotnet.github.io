# selectbuttondotnet.github.io
Organization repository for gameoeuvre.org, a community project of the selectbutton.net forums.

**Instructions for previewing locally on Windows with minimal CLI**

1. Download and install [Ruby](https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-3.1.2-1/rubyinstaller-devkit-3.1.2-1-x64.exe)

When prompted with installation options, press enter.

2. Download and install [GitHub Desktop](https://desktop.github.com/)

3. Clone the repository for gameoeuvre. Mine lives in c:\users\[username]\documents\github\selectbuttondotnet.github.io

4. Open a command prompt and type/execute the following commands:

`gem install jekyll bundler`

`jekyll -v`

The Jekyll version should be ~4.2.2.

5. Navigate to your repository directory in your command prompt with the following command:

cd c:/users/[username]/documents/github/selectbuttondotnet.github.io/docs

6. Install/build Jekyll from the Ruby gemfile instructions with the following command:

`bundle install`

7. Run the local server with the following command:

`bundle exec jekyll serve`

8. Navigate to localhost:4000 in your web browser.