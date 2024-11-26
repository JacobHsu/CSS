# CSS


[NIPPON COLORS](http://nipponcolors.com/)（日本の伝統色）



| STYLING OPTION     | WHERE?                   | HOW?                  | SCOPE           | BASED ON |
|---------------------|--------------------------|-----------------------|-----------------|----------|
| 👉 Inline CSS       | JSX elements            | `style` prop          | JSX element (Local) | CSS      |
| 👉 CSS or Sass file | External file           | `className` prop      | Entire app (Global, causes problems) | CSS |
| 👉 CSS Modules      | One external file per component | `className` prop | Component       | CSS      |
| 👉 CSS-in-JS        | External file or component file | Creates new component | Component       | JavaScript |
| 👉 Utility-first CSS `tailwindcss`| JSX elements            | `className` prop      | JSX element     | CSS      |


# hexo

`$ hexo s`

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

`hexo s`  

`$hexo d` ERROR Deployer not found: git  
> npm install hexo-deployer-git --save  

實在不行，就把它刪掉，然後重新生成和部署。
`rm -rf .deploy_git`  
`hexo g`  
`hexo d`  
