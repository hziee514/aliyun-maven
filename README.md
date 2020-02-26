# aliyun-maven

## 构建发布镜像

```bash
# 切换到对应版本目录
cd 3-jdk-8
# 根据Dockerfile构建镜像并打上标签
docker build --tag registry.cn-hangzhou.aliyuncs.com/fullj/aliyun-maven:3-jdk-8 .
# 登陆私有镜像仓库
docker login --username=xxxx registry.cn-hangzhou.aliyuncs.com
# 推送到镜像仓库
docker push registry.cn-hangzhou.aliyuncs.com/fullj/aliyun-maven:3-jdk-8
```

## 使用此镜像打包应用

```bash
mvn --settings /settings.xml clean package
```

