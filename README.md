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
用github action了
1. 推送到gh-pages分支
2. 推送到cos

# about theme

submodule: `git submodule add https://github.com/luxiaolululu/hexo-theme-yilia.git themes/yilia`

fork from 原来的yilia主题，然后修改了config文件


# 图片显示
参考文章： https://blog.csdn.net/xjm850552586/article/details/84101345
需要替换js文件
`cp ./node_modules_tmp/hexo-asset-image-index.js ./node_modules/hexo-asset-image/index.js`