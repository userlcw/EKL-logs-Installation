# EKL-logs-Installation
本项目用于内网快速部署ELK日志平台，通过Filebeat采集多台服务器的系统日志与Docker容器日志并统一汇聚到主节点检索展示。
主节点192.168.1.107运行docker-elk，Kibana入口：http://192.168.1.107:5601。
采集节点采集/var/log与/var/lib/docker/containers/*/*-json.log，经192.168.1.107:5044发送到Logstash。
在Kibana创建logs- * Data View后，可在Discover按source_node/host等字段筛选查看，实现集中化与快速排障。
