# scikit-learn
<scikit-learn机器学习常用算法及编程实践，黄永昌，机械工业出版社>源码及数据
http://www.hzbook.com/index.php/Book/search.html?k=scikit-learn%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0
# 用法
* 下载工程
```
# git clone https://github.com/ravihuang/scikit-learn.git
```
* 下载datasets（在release中）
```
# cd scikit-learn
# curl -LO <datasets.tgz>
# tar xzvf datasets.tgz
```
* 启动polynote server：
```
# pwd
/root


# more docker-compose.yml
version: '3'
services:
  polynote:
    image: ${REPO:-docker.io}/testerq/polynote
    container_name: polynote
    restart: always   
    environment:
      - PYSPARK_ALLOW_INSECURE_GATEWAY=1
      - GRANT_SUDO=yes
    ports:
      - 8192:8192
      - 4040-4050:4040-4050
    volumes:
      - /root/scikit-learn:/opt/polynote/notebooks

# docker-compose up -d
```
* login使用
http://<ip>:8192/
