# 说明

此项目采用ansible来自动化部署Nextcloud 12.0.0，此程序在ubuntu 16.04版本下测试运行通过

## 使用方法

1. 修改group_vars下的all文件

2. 修改production和stage文件

3. 开始部署

生产环境
`ansible-playbook -K -i production site.yml`

演练环境
`ansible-playbook -K -i stage site.yml`

4. Https支持

此处使用certbot(Let’s Encrypt)来申请免费的证书。

仅能在生产环境运行
`ansible-playbook -K -i production site_https.yml`