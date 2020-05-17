# 自动化打包发布测试脚本

## config.json
```json
{
  "project_path": "/Users/jiaozenglian/Documents/ADreamClusive2/ADreamClusiveModel/工程文件所在目录",
  "project_name": "ADreamClusiveModel",
  "scheme_name": "ADreamClusiveModel",
  "export_ipa_path": "/Users/jiaozenglian/Desktop/ipa包导出目录",
  "git_project_branch_name": "git分支名称：打包前会自动拉取远程分支最新内容",
  "comments" : "这里是打包说明，上传到蒲公英时需要的内容（一行简短说明即可）",
  "email_config": {
    "subject": "这里是邮件标题",
    "host": "smtp.qq.com",
    "to_user": [
        "2506513065@qq.com"
    ],
    "mail_user_name": "2472780140@qq.com",
    "password": "kzwvjasknbouecbb",
    "body": "这里写邮件内容"
  }
}
```

## 打包命令

如果python2.x环境执行失败，建议升级到python3.x使用

```
python ./autoBuildTool.py
```

这时可以悠闲的去抽支烟。。。。

## 其他

1. 准备好一个本地repo作为专门打包使用（与工作repo分开，便于打包时不影响你继续开发）；
2. 将config.json中的工程目录指向这个repo
3. 每次自动打包前，会先去远程拉取打包分支最新内容

注意⚠️：此脚本只是用于工作方便，解放你的双手，并没有进行过多容错处理；所以使用时务必配置正确，发生错误造成打包失败或其他后果概不负责。