# 新建项目 blog，上传到 GitHub

## 步骤
### 新建项目 blog
1. 输入 `rails new blog -d postgresql`
1. 输入 `cd blog`
1. 输入 `git init`
1. 输入 `git add .`
1. 输入 `git commit -m "init"`
1. 输入 `rails g scaffold post title:string content:text`
1. 输入 `rake db:create`
1. 输入 `rake db:migrate`
1. 填入

** `config/routes.rb`
```
Rails.application.routes.draw do
  resources :posts
  root "posts#index"
end
```

![](https://ws1.sinaimg.cn/large/006tNc79ly1fgpdqtoroyj30m804t74y.jpg)

### 移除敏感的 config/database.yml
1. 输入 `cp config/database.yml config/database.yml.example`
1. 输入 `git rm config/database.yml`
1. 填入

** `.gitignore`
```
# Ignore Byebug command history file.
.byebug_history
config/database.yml
```

![](https://ws2.sinaimg.cn/large/006tNc79ly1fgpdrgobs1j30m80fmjtl.jpg)

1. 输入 `git add .`
1. 输入 `git add -u`
1. 输入 `git commit -m "move config/database.yml"`

### 移除敏感的 config/secrets.yml
1. 输入 `cp config/secrets.yml config/secrets.yml.example`
1. 输入 `git rm config/secrets.yml`
1. 填入

** `.gitignore`
```
# Ignore Byebug command history file.
.byebug_history
config/database.yml
config/secrets.yml
```

![](https://ws2.sinaimg.cn/large/006tNc79ly1fgpds3osztj30lg09gjs9.jpg)

1. 输入 `git add .`
1. 输入  `git commit -m "move secrets"`

### 上传到 Github
去 github 新建一个项目

![](https://ws1.sinaimg.cn/large/006tNc79ly1fgpdsvretoj30m806xq3y.jpg)

![](https://ws4.sinaimg.cn/large/006tNc79gy1fgpdtcf6h9j30m80hd777.jpg)

1. 输入 `git remote add origin git@github.com:ＸＸＸＸＸＸＸ/blog.git`
1. 输入 `git push -u origin master`
