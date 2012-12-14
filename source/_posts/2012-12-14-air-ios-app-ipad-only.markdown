---
layout: post
title: "如何air生成的app只支持ipad"
date: 2012-12-14 09:57
comments: true
categories: air,ios,flash
---

打开项目中的app配置文件 ***-app.xml, 找到：

        <InfoAdditions><![CDATA[
			<key>UIDeviceFamily</key>
			<array>
				<string>1</string>
				<string>2</string>
			</array>
		]]></InfoAdditions>

其中1代表iPhone,iPod touch. 2代表ipad，根据需要注释掉不需要的就可以了。
