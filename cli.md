```bash
git add .
# 将修改直接合并到上一个commit，并且使用上次的提交信息
git commit --amend --no-edit
git reflog
git reset HEAD@{index}
git show {hash}
git checkout {hash} -- {file path}
git revert {hash}
```

在Mac os下使用Clashx的代理时，配置命令行的代理
```bash
// 打开
$ vi ~/.zshrc

// 插入
alias proxy='export all_proxy=http://127.0.0.1:7890'
alias unproxy='unset all_proxy'

// 使用
$ source ~/.zshrc

// 测试
curl cip.cc
```

直接修改第三方库之后需要patch一下包
```bash
$ yarn patch-package *
```

检查依赖包是否有使用
```bash
$ npx depcheck
```

webp格式统一转换
```bash
$ for file in *
> do
> cwebp -q 80 "$file" -o "${file%.png}.webp"
> done
```

使用淘宝镜像
```bash
npm config set registry https://registry.npmmirror.com
yarn config set registry https://registry.npmmirror.com
```
