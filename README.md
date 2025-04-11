创建路径：.github/workflows/Obfuscate.yml

（此 Action 将在每次 push 到 main 分支和每天凌晨 1 点自动执行，下载最新未混淆的 BPB 源代码（origin.js），并生成混淆后的 `_worker.js` 文件，作为你个人专属的 BPB 代码。）

避免项目名称出现以下内容：edgetunnel、edtunnel、epeius、bpb、cmliu、vless、trojan等。
手动创建项目时的修改项目名称，避免出现上述关键词和与过去已报错1101项目同名的情况。
相关变量

KV空间绑定名称:小写 kv

添加变量：（固定地区IP，告别风控）

UUID（可用官方生成，或自己获取）

TR_PASS

PROXYIP

网址后缀输入：

/panel （直接进入面板设置密码）

/login    (无法正常进入，需要到KV空间设置密码)

查看kV-KV对-密钥：pwd-自定义密码(大小英文加数字)-添加条目

Cloudflare 部署
•创建pages：点击workers和pages，选择pages部署。连接github仓库，选择新建的项目仓库，然后点击部署。
•绑定自定义域名：以防止page分配的域名被屏蔽。
•设置变量：UUID，PROXYIP, TR_PASS
•绑定KV命名空间：名称随便但不能含有bpb等敏感词
•重试部署pages
BPB面板设置
•部署成功后，打开浏览器输入:https://[自定义域名]或者你的项目地址,后面加上/panel检查是否能正常访问BPB面板.
•修改BPB面板密码
•配置BPB面板参数
