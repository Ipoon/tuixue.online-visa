
############################################################################
# 制作docker 镜像 sudo docker build -t winchell/visaspider:1.0.0 .
# 导出docker 镜像 sudo docker save > visaspider.tar winchell/visaspider:1.0.0
# 导入docker 镜像 docker load < visaspider.tar
# 运行docker 镜像 docker run -d -p 8888:8888 winchell/visaspider:1.0.0
# 导出环境依赖包 pip freeze > requirements.txt
FROM python
COPY . .
EXPOSE 8888
RUN pip install --no-cache-dir -i https://mirrors.aliyun.com/pypi/simple/ -r requirements.txt
CMD [ "python", "manage.py", "runserver", "0.0.0.0:8888" ]
