---
layout:     post
title:      Openstack Cinder卷挂载流程
subtitle:   Cinder卷挂载流程 
date:       2019-02-22
author:     BY
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - Openstack
    - Cinder
    - 存储
    - 开源框架
---
# 前言
>Openstack在Q版本开始支持卷多挂载功能，在使用此功能时出现问题，经过对挂载流程的分析，对卷的挂载业务有了进一步的了解
故写下记录

# 简单介绍
卷挂载业务关系到Openstack的两个组件：Nova和Cinder,本文以ISCSI存储连接方式为例做详解
# 代码步骤
1. 接口地址/请求参数
/servers/{server_id}/os-volume_attachments
```
{
    "volumeAttachment": {
        "volumeId": "a26887c6-c47b-4654-abb5-dfadf7d3f803",
        "device": "/dev/vdd"
    }
}
```
# 代码步骤
