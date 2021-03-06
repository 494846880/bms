# 获取Windows裸金属服务器的密码<a name="bms_umn_0030"></a>

## 操作场景<a name="section0230121618127"></a>

登录Windows操作系统的裸金属服务器时，需使用密码方式登录。因此，用户需先根据创建裸金属服务器时使用的密钥文件，获取该裸金属服务器初始安装时系统生成的管理员密码（Administrator帐户或Cloudbase-init设置的帐户）。该密码为随机密码，安全性高，请放心使用。

## 前提条件<a name="section81271915161618"></a>

已获取创建该裸金属服务器时使用的密钥对私钥文件。

## 操作步骤<a name="section15236417161414"></a>

1.  登录管理控制台。
2.  选择“计算 \> 裸金属服务器”。

    进入裸金属服务器页面。

3.  在Windows裸金属服务器所在行，单击“操作”列的“更多 \> 获取密码”。

    **图 1**  获取密码<a name="fig13462119192418"></a>  
    ![](figures/获取密码.png "获取密码")

4.  通过私钥文件获取密码，获取方法有如下两种：
    -   单击“选择文件”，从本地上传私钥文件。
    -   将私钥文件内容复制粘贴在空白框中。

5.  单击“获取密码”，获取随机密码。

