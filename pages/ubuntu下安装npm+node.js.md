title:: ubuntu下安装npm+node.js

- title:: ubuntu下安装npm+node.js
- 一、从NodeSource安装Node.js和npm
  NodeSource是一家致力于提供企业级Node支持的公司。它维护一个包含多个Node.js版本的APT存储库。如果您的应用程序需要特定版本的Node.js，请使用此存储库。
- 在撰写本文时，NodeSource存储库提供以下版本：
  v16.x-最新的稳定版本。
  v14.x-最新的稳定版本。
  v13.x
  v12.x-最新的LTS版本。
  v10.x-先前的LTS版本。
- 附：github操作链接：https://github.com/nodesource/distributions
  二、我们将安装Node.js版本16.x
  1.以具有sudo特权的用户身份运行以下命令，以下载并执行NodeSource安装脚本
  curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
  1
  2.启用NodeSource存储库后，安装Node.js和npm
  sudo apt-get install -y nodejs
  1
  3.通过打印它们的版本来验证Node.js和npm是否已成功安装
  node --version  # v16.14.0
  1
  npm --version  # v8.3.1
  ————————————————
  版权声明：本文为CSDN博主「ch_atu」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
  原文链接：https://blog.csdn.net/weixin_47513022/article/details/123105523