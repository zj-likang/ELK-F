# ELK-F
此项目是  ELK + filebeat 的K8S部署 Charts 
直接下载相应的文件夹 放到 K8s master上 在文件夹对应的目录 使用 helm3 安装

```
安装 es
helm3 install  elasticsearch lsh-mcp-elasticsearch
安装 logstash
helm3 install  logstash lsh-mcp-logstash
安装 filebeat
helm3 install  filebeat lsh-mcp-filebeat
安装 kibana
helm3 install  kibana lsh-mcp-kibana
```

如果使用的是 hlem2 则命令是
 helm install --name elasticsearch lsh-mcp-elasticsearch
其它同上 以helm 开头 --name 指定安装名称  后面参数是文件夹名称
采集所有的K8S pod 标准输出日志，ES以pod 服务名称创建index
