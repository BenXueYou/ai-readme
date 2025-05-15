### vconsole 环境部署地址：

```
10.19.141.212  hiam@yunyao123
```

dev: 10.19.165.89  root/123456   路径： data1/fe
gn：10.19.123.170  root/TianmuTest 路径：/data/tianmu/fe



功能测试容器化服务器地址：

10.19.123.164/root TianmuTest

kubectl get pods -n tianmu-gn | grep vhatom

 kubectl describe pods pod名称 -n namespace 显示Pod的详细运行信息，排查问题



### hatom-dev环部署境地址

IP：10.19.134.188:22 密码：root/ga@hik123
第一步：连接对应的docker 在 docker exec -it hatom_80 bash  连接到hatom_80   【查看 hatom_80 容器所占的端口号命令: ``` docker port  hatom_80```】
第二步：连接svn svn://admin@10.19.134.188/repository/version/v2  （用户名：admin ,密码：hik@123）在version对应版本下（v2）创建日期目录，放入压缩包到创建的目录
第三步：在shell下的 /opt/versions下执行 ./upgrade 2 2021020401  （第一个参数是版本 第二个参数是目录名称）即可将本地文件拷贝到docker中
第四步：到shell下/opt/versions/日期目录下 复制文件到 www下 cp ./www.zip /usr/share/nginx/html
第五步： cd /usr/share/nginx/html 解压 www文件到www下   命令：unzip www.zip -d www （选择全覆盖）



### 容器化部署服务

IP： 10.19.123.250   root/TianmuTest

kubectl get pods -n tianmu-gn | grep vhatom

### 发布npm包      6.14.11

1、检查并切换源  

> npm config set registry https://registry.npmjs.org/
>
> npm config get registry 

2、登录npm账号密码以及邮箱

> npm login
>
> npm-pbg/helloworld
>
> oa@hikvision.com

3、设置发布版本

> npm version <update_type>

4、发布推送

> npm publish

5、切换本地源

> npm config set registry http://af.hikvision.com.cn/artifactory/api/npm/npm-pbg/

hikyun@aliyun.com/Hikyun~!@345

support.hikyun@hikvision.com/Hikyun~!@345



```bash
h5load-uat.hikyun.com
10.221.36.19
root Hik123!@#
/data/nginx/run/conf/hikyun.com
```



### 关于java环境

1、查询本地tomcat安装位置

```bash
sudo find / -name "tomcat" -type d
```

2、查询本地 tomcat 的版本 

```bash
 # 进入安装的目录
 cd /opt/hikvision/mobileappstore/bin/tomcat
 
 # 查询版本命令
 ./catalina.sh version
 
 # 或Tomcat 8或更高版本 使用以下命令
 ./bin/catalina.sh version -v

```

3、 查询本地 jdk 版本

```bash
java -version
```



vue-loader->compiler-sfc->compiler-dom->comiler-core->runtime-dom->runtime-core

```jsp
          <!-- <c:import url="http://af.hikvision.com.cn/artifactory/usta/prod/kelunapp/3.2.4/20230919153044/privacy.txt" var="remoteContent">
            <c:catch var="catchContent">
              <p>远程资源无法加载，以下是备用内容：</p>
            </c:catch>
          </c:import>
          <c:if test="${not empty remoteContent}">
            <p>远程内容：</p>
            <c:out value="${remoteContent}" />
          </c:if> -->
```



