# Github Actions + Github Pages

使用 Github Actions 部署一个静态前端页面

主要用到了 Github Actions 中的别人写的好的动作

```yml
#  https://github.com/crazy-max/ghaction-github-pages
	- name: Deploy to GitHub Pages
      uses: JamesIves/github-pages-deploy-action@3.7.1
      with:
          ACCESS_TOKEN: ${{ secrets.ACCESS_TOKEN }}
          # 部署到 gh-pages 分支
          BRANCH: gh-pages
          # 部署目录当前目录
          FOLDER: .
```

共两步，先配置 main.yml，再配置 ACCESS_TOKEN，就可以
先配置 ACCESS_TOKEN

### 使用场景
如果我要做 css 效果、做一个 Demo 供别人看，最好是放在网站上，其中 GitHub Page 是最好的选择
做好 Github Actions，就能做到即写即看，而且能一直保留到 GitHub 关门

因为俺之前用 Github Page 配置过调整到我的个人wiki页，所以即使这样跳转成功，也还是找不到页面
http://fe.azhubaby.com/github-actions-github-pages/

所以只能放在另一个自己的二级域名上,github.azhubaby.com