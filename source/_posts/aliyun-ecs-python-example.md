---
layout: posts
date: 2018-12-27 00:38:36
title: python sdk 操作aliyun的ecs
categories: python
tags: 
- python
- aliyun
comments: true
---


### python sdk方式操作aliyun ECS:
    pip install aliyun-python-sdk-core
    pip install aliyun-python-sdk-ecs
    
    参考：
        https://develop.aliyun.com/tools/sdk?#/python

#### aliyun SDK:
    SDK:
        https://github.com/aliyun/aliyun-openapi-python-sdk
    
    use example:
        https://github.com/aliyun/aliyun-openapi-python-sdk#use-python-sdk 
        
        
#### python demo:
```python
from aliyunsdkcore import client
AccessKeyID="access_key_id"
AccessKeySecret="access_key_secret"
RegionId="region_id"

clt = client.AcsClient(AccessKeyID,AccessKeySecret,RegionId)

import aliyunsdkecs
help(aliyunsdkecs)  #ls -ltr /usr/lib/python2.7/site-packages/aliyunsdkecs/request/v20140526/

from aliyunsdkecs.request.v20140526 import DescribeInstancesRequest
DescribeInstancesReq = aliyunsdkecs.request.v20140526.DescribeInstancesRequest.DescribeInstancesRequest()

DescribeInstancesReq.get_InstanceIds()
DescribeInstancesReq.set_ImageId(ImageId = 'xxxx')
DescribeInstancesReq.set_InstanceName(InstanceName = 'yyyy')

ret = json.loads(clt.do_action_with_exception(DescribeInstancesReq))
print ret

```





~~完~~
