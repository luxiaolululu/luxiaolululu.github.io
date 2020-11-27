# init
```
git submodule update --init
npm install
npm run server
```
# about branch

- master: 主分支

- pages: hexo deploy 分支

- temp: 临时commit分支

# create a new post

``` bash
$ hexo new post "My New Post" # post is template
```

# deploy

`npm run deploy` then goto https://aholulu.bitbucket.io/


# about theme

submodule: `git submodule add https://github.com/litten/hexo-theme-yilia.git themes/yilia`

`cp theme_config.yml themes/yilia/_config.yml`