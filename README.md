# Docker Maven for Keqin
[![Openjdk-16](https://github.com/keqin-inc/docker-maven/actions/workflows/openjdk-16.yml/badge.svg)](https://github.com/keqin-inc/docker-maven/actions/workflows/openjdk-16.yml)

## 介绍

- 该 Docker 镜像基于官方 Maven 版本，区别为默认使用了阿里云 Maven 镜像 <https://maven.aliyun.com>。
- 主要用于封装开发环境
- 生产环境中直接运行 openjdk 镜像打包版本。
- 后续将增加更多环境变量配置支持，例如内置企业内部 Maven 制品库。

## 用法

```yaml
java:
    image: keqin/maven
    working_dir: /app
    volumes: 
        - ./src:/app
    ports:
        - 8080:8080
    entrypoint: mvn spring-boot:run
```

## 版本

[`3-openjdk-16,3,latest,3-openjdk,openjdk`](openjdk-16/Dockerfile)
