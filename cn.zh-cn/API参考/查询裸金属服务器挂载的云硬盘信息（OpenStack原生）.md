# 查询裸金属服务器挂载的云硬盘信息（OpenStack原生）<a name="ZH-CN_TOPIC_0053158658"></a>

## 功能介绍<a name="section61843920"></a>

查询裸金属服务器挂载的云硬盘信息。

## URI<a name="section19724370"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-volume\_attachments

参数说明请参见[表1](#table98221910184910)。

**表 1**  参数说明

<a name="table98221910184910"></a>
<table><thead align="left"><tr id="row198228100493"><th class="cellrowborder" valign="top" width="24.032403240324033%" id="mcps1.2.4.1.1"><p id="p37105578"><a name="p37105578"></a><a name="p37105578"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.692369236923692%" id="mcps1.2.4.1.2"><p id="p52761866"><a name="p52761866"></a><a name="p52761866"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="52.275227522752274%" id="mcps1.2.4.1.3"><p id="p45852771"><a name="p45852771"></a><a name="p45852771"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row482218108494"><td class="cellrowborder" valign="top" width="24.032403240324033%" headers="mcps1.2.4.1.1 "><p id="p58102813"><a name="p58102813"></a><a name="p58102813"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.692369236923692%" headers="mcps1.2.4.1.2 "><p id="p8707407"><a name="p8707407"></a><a name="p8707407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.275227522752274%" headers="mcps1.2.4.1.3 "><p id="p34211353"><a name="p34211353"></a><a name="p34211353"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row082212108498"><td class="cellrowborder" valign="top" width="24.032403240324033%" headers="mcps1.2.4.1.1 "><p id="p42688329"><a name="p42688329"></a><a name="p42688329"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.692369236923692%" headers="mcps1.2.4.1.2 "><p id="p35202648"><a name="p35202648"></a><a name="p35202648"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.275227522752274%" headers="mcps1.2.4.1.3 "><p id="p32842235"><a name="p32842235"></a><a name="p32842235"></a><span id="text8345838143314"><a name="text8345838143314"></a><a name="text8345838143314"></a>裸金属服务器</span><span id="text14345738113312"><a name="text14345738113312"></a><a name="text14345738113312"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section43301605"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/os-volume_attachments
    ```


## 响应消息<a name="section54170131"></a>

-   响应参数

    <a name="table57959838"></a>
    <table><thead align="left"><tr id="row39710134"><th class="cellrowborder" valign="top" width="26.08%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.64%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.28%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row62961510"><td class="cellrowborder" valign="top" width="26.08%" headers="mcps1.1.4.1.1 "><p id="p66717520"><a name="p66717520"></a><a name="p66717520"></a>volumeAttachments</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.64%" headers="mcps1.1.4.1.2 "><p id="p49639570"><a name="p49639570"></a><a name="p49639570"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.28%" headers="mcps1.1.4.1.3 "><p id="p15568903"><a name="p15568903"></a><a name="p15568903"></a><span id="text10651144263320"><a name="text10651144263320"></a><a name="text10651144263320"></a>裸金属服务器</span><span id="text165113429334"><a name="text165113429334"></a><a name="text165113429334"></a></span>挂载信息列表，详情请参见<a href="#table7886611">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  volumeAttachments字段数据结构说明

    <a name="table7886611"></a>
    <table><thead align="left"><tr id="row60727582"><th class="cellrowborder" valign="top" width="26.437356264373562%" id="mcps1.2.4.1.1"><p id="p19987085"><a name="p19987085"></a><a name="p19987085"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.42745725427458%" id="mcps1.2.4.1.2"><p id="p4546697"><a name="p4546697"></a><a name="p4546697"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.135186481351866%" id="mcps1.2.4.1.3"><p id="p32738149"><a name="p32738149"></a><a name="p32738149"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row34544438"><td class="cellrowborder" valign="top" width="26.437356264373562%" headers="mcps1.2.4.1.1 "><p id="p46636132"><a name="p46636132"></a><a name="p46636132"></a>device</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.42745725427458%" headers="mcps1.2.4.1.2 "><p id="p30355189"><a name="p30355189"></a><a name="p30355189"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.135186481351866%" headers="mcps1.2.4.1.3 "><p id="p50116845"><a name="p50116845"></a><a name="p50116845"></a>挂载目录，例如“/dev/vdb”。</p>
    </td>
    </tr>
    <tr id="row48398424"><td class="cellrowborder" valign="top" width="26.437356264373562%" headers="mcps1.2.4.1.1 "><p id="p27958252"><a name="p27958252"></a><a name="p27958252"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.42745725427458%" headers="mcps1.2.4.1.2 "><p id="p25568738"><a name="p25568738"></a><a name="p25568738"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.135186481351866%" headers="mcps1.2.4.1.3 "><p id="p50454834"><a name="p50454834"></a><a name="p50454834"></a>挂载资源ID。</p>
    </td>
    </tr>
    <tr id="row51440330"><td class="cellrowborder" valign="top" width="26.437356264373562%" headers="mcps1.2.4.1.1 "><p id="p5917164"><a name="p5917164"></a><a name="p5917164"></a>serverId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.42745725427458%" headers="mcps1.2.4.1.2 "><p id="p33594135"><a name="p33594135"></a><a name="p33594135"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.135186481351866%" headers="mcps1.2.4.1.3 "><p id="p62498284"><a name="p62498284"></a><a name="p62498284"></a>所属<span id="text194132454338"><a name="text194132454338"></a><a name="text194132454338"></a>裸金属服务器</span><span id="text641384517333"><a name="text641384517333"></a><a name="text641384517333"></a></span>ID。</p>
    </td>
    </tr>
    <tr id="row25613652"><td class="cellrowborder" valign="top" width="26.437356264373562%" headers="mcps1.2.4.1.1 "><p id="p61439917"><a name="p61439917"></a><a name="p61439917"></a>volumeId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.42745725427458%" headers="mcps1.2.4.1.2 "><p id="p51461341"><a name="p51461341"></a><a name="p51461341"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.135186481351866%" headers="mcps1.2.4.1.3 "><p id="p1462819"><a name="p1462819"></a><a name="p1462819"></a>挂载云硬盘ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "volumeAttachment": {
            "device": "/dev/vdb",
            "serverId": "820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa",
            "id": "b53f23bd-ee8f-49ec-9420-d1acfeaf91d6",
            "volumeId": "b53f23bd-ee8f-49ec-9420-d1acfeaf91d6"
        }
    }
    ```


## 返回值<a name="section7610951"></a>

正常返回值：

<a name="zh-cn_topic_0106040941_table753804619176"></a>
<table><thead align="left"><tr id="zh-cn_topic_0106040941_row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0106040941_p19735204616177"><a name="zh-cn_topic_0106040941_p19735204616177"></a><a name="zh-cn_topic_0106040941_p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0106040941_p207355465176"><a name="zh-cn_topic_0106040941_p207355465176"></a><a name="zh-cn_topic_0106040941_p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0106040941_row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0106040941_p13735144611178"><a name="zh-cn_topic_0106040941_p13735144611178"></a><a name="zh-cn_topic_0106040941_p13735144611178"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0106040941_p207351246161711"><a name="zh-cn_topic_0106040941_p207351246161711"></a><a name="zh-cn_topic_0106040941_p207351246161711"></a>服务器已成功处理了请求。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

