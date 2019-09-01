## 监控、报警
````
# prometheus官网 https://prometheus.io/download/
# mysqld_exporter:支持对mysql的监控
````

## 安装 prometheus

````
# https://github.com/prometheus/prometheus/blob/master/documentation/examples/prometheus.yml
# 从上面下载的模版配置文件，--config.file指向的路径自定义，增加job_name prometheus即可添加新的监控
# 默认地址：http://127.0.0.1:9000

$: brew install prometheus
$: brew services start prometheus
$: prometheus --config.file=/usr/local/etc/prometheus/prometheus.yml
````

## 安装 mysql_exporter
````
#网址： https://prometheus.io/download/
#下载：mysqld_exporter-0.12.1.darwin-amd64.tar.gz
#默认地址：http://127.0.0.1:9104

# 默认读取的mysql配置文件~/.my.conf
# vim ~/.my.conf
   [client]
      host=127.0.0.1
      port=6379
      user=root
      password=root
# 在prometheus中添加配置
# vim /usr/local/etc/prometheus/prometheus.yml
     -job_name: 'mysql'
      static_configs:
       - targets: ['127.0.0.1:9104']
          labels:
            instance: sys
#双击：mysqld_exporter
````

## 安装 grafana

```
$: brew install grafana
$: brew services start grafana
# 默认地址:http://127.0.0.1:3000/
```
## 安装 sentry


```
# python 安装，还有点问题，有空再改吧。
$: sudo easy_install pip
$: sudo easy_install nose
$: sudo easy_install tornado
$: pip install -U virtualenv
$: virtualenv /www/sentry/
$: source /www/sentry/bin/activate
$: pip install -U sentry --ignore-installed six
# docker 安装
```


