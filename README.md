# confd_nacos

1.对nacos的访问，加上username和password参数；

2.监听时间间隔改为30s；

3.自动refresh时间间隔改为1分钟

程序来源

  1：https://github.com/nacos-group/confd/archive/v0.18.0.tar.gz

  2: https://github.com/nacos-group/nacos-sdk-go/archive/v0.3.1.tar.gz

  注意版本。

  把2里的程序，覆盖到1的vendor/nacos-group/nacos-sdk-go。

  然后修改：

  backends/client.go

  backends/nacos/client.go

  vendor/nacos-group/nacos-sdk-go/clients/config_client/cofnig_client.go

  vendor/nacos-group/nacos-sdk-go/clients/config_client/cofnig_proxy.go

  vendor/github.com/nacos-group/nacos-sdk-go/common/security/security_proxy.go


编译：

将程序拷贝到 $GOPATH/src/github.com/kelseyhightower 目录，然后执行make。