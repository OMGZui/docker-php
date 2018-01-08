FROM nginx:alpine

# 复制本地配置文件到nginx
ADD nginx.conf /etc/nginx/

# 添加www-data用户
RUN adduser -D -H -u 1000 -s /bin/bash www-data

# 执行nginx命令
CMD [ "nginx" ]

# 暴露端口
EXPOSE 80 443
