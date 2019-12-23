houyi模块安装部署说明:

1.部署工具
    houyi模块使用ansible工具自动部署, 
    相关的脚本和配置文件已上传至git houyi-deploy工程:https://git.mesalab.cn/tsg/houyi-deploy
  
2.部署步骤  
    2.1)git下载houyi-deploy.tgz
    2.2)进入houyi-deploy目录, 根据要部署的实际网络环境, 选择合适的hosts文件,
      
        例如,在信息港部署TSG设备, 执行以下命令: 
        ansible-playbook -i hosts.xxg.transparent  houyi-playbook.yml
    2.3)ansible工具会根据预设的playbook自动部署, 部署完成后, 会生成部署状态报告, 
        状态正常包括ok和changed, 如果有failed计数, 请联系开发人员解决。
