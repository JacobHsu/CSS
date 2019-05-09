# CSS


[NIPPON COLORS](http://nipponcolors.com/)（日本の伝統色）

# hexo

[hexo-theme-doc-seed](https://github.com/zalando-incubator/hexo-theme-doc-seed)  
`git clone https://github.com/zalando-incubator/hexo-theme-doc-seed.git`  
remove dir `.git`  
rename hexo-theme-doc-seed  dir `doc`  

doc/_config.yaml  
```js
# URL
root: /CSS

deploy:
  type: git
  repository: https://github.com/JacobHsu/CSS
  branch: gh-pages
```

`$doc> npm install`  
`$doc> hexo g`   public  
`$doc> hexo d`  

## Note

`$hexo d` ERROR Deployer not found: git  
> npm install hexo-deployer-git --save  

實在不行，就把它刪掉，然後重新生成和部署。
`rm -rf .deploy_git`  
`hexo g`  
`hexo d`  