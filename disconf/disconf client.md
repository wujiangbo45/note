# disconf 配置方式

## core:

- 对 zk 的扩展。
  - LockListener 监听执行， required, release, 回调执行。
  - ZooKeeperOperation execute 回调函数执行。
    1. ZNodeName: predix-name 节点名称。
    1. ProtocolSupport 1 执行ZookeeperOperation, 设置retry 重试时间， 定时执行。 2 ensureExists 存在Path 路径配置方式。

- core 配置：
  - Constants 常量配置，disconf-web zk, 相关常量。
  - DisConfigTypeEnum 配置文件， 配置项。

  - DisconfWebPathMgr zk 配置文件路径设置。
  - ZooPathMgr zk 基础配置Item 配置信息。

## 远程获取的 File 配置文件相关信息。

### client spring 客户端集成配置测试方式：

- DisconfMgr disconf client 总入口.
  - register：Registry bean 的注册查找 
    - SimpleRegister 通过Class newInstance 的 Bean的 生成注册方式。
    - SpringRegister get Bean object from springApplicationContext, 如果代理的模式， Aop 获取Source Object 方式。

- RegistryFactory 获取SpringRegister 配置方式。

- user tools IDisconfDataGetter 通过配置文件 获取Mapper 的配置信息。

- DisconfValue 配置文件 properties key-value 的配置方式。

- store file 文件存储Class
