### 数据库逻辑结构设计

本系统的数据结构遵循关系型数据库基本设计原则，根据系统的功能要求，数据库的表结构如下：

#### 系统信息表 info

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | infoname | varchar | 45 | 否 | 否 | 信息名称 |
| 2 | incocontent | varchar | 512 | 否 | 否 | 信息内容 |

#### 所有用户表 user

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | userid | varchar | 255 | 是 | 否 | 用户序号 |
| 2 | username | varchar | 255 | 是 | 否 | 用户名称 |
| 3 | userpwd | varchar | 255 | 是 | 否 | 用户密码 |
| 4 | userfullname | varchar | 255 | 是 | 否 | 用户全称 |
| 5 | usersex | varchar | 255 | 是 | 否 | 用户性别 |
| 6 | usermobile | varchar | 255 | 是 | 否 | 用户电话 |
| 7 | useremail | varchar | 255 | 是 | 否 | 用户邮箱 |
| 8 | usercreatedt | varchar | 255 | 是 | 否 | 用户创建日期 |
| 9 | userstatus | varchar | 255 | 是 | 否 | 用户状态 |
| 10 | userpic | longblob | 0 | 是 | 否 | 用户头像 |
| 11 | userofrole | varchar | 255 | 是 | 否 | 用户所在分组 |
| 12 | unitproperty01 | varchar | 255 | 是 | 否 | 预留字段 |
| 13 | unitproperty02 | varchar | 255 | 是 | 否 | 预留字段 |
| 14 | unitproperty03 | varchar | 255 | 是 | 否 | 预留字段 |
| 15 | unitproperty04 | varchar | 255 | 是 | 否 | 预留字段 |
| 16 | unitproperty05 | varchar | 255 | 是 | 否 | 预留字段 |

#### 用户角色分组表 role

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | roleid | varchar | 255 | 是 | 否 | 分组序号 |
| 2 | rolename | varchar | 255 | 是 | 否 | 分组名称 |
| 3 | roledesc | varchar | 255 | 是 | 否 | 分组降序 |
| 4 | rolecreatedt | varchar | 255 | 是 | 否 | 创建分组的日期 |
| 5 | rolestatus | varchar | 255 | 是 | 否 | 分组状态 |
| 6 | rolerightbasic | text | 0 | 是 | 否 | 分组正确的要素 |
| 7 | rolerightpage | text | 0 | 是 | 否 | 分组正确的页码 |
| 8 | rolerightwritepoint | text | 0 | 是 | 否 | 分组与操作点的权限屏蔽 |
| 9 | roleright1 | text | 0 | 是 | 否 | 分组权限预留字段1 |
| 10 | roleright2 | text | 0 | 是 | 否 | 分组权限预留字段2 |
| 11 | roleright3 | text | 0 | 是 | 否 | 分组权限预留字段3 |
| 12 | roleright4 | text | 0 | 是 | 否 | 分组权限预留字段4 |
| 13 | roleright5 | text | 0 | 是 | 否 | 分组权限预留字段5 |
| 14 | unitproperty01 | varchar | 255 | 是 | 否 | 预留字段 |
| 15 | unitproperty02 | varchar | 255 | 是 | 否 | 预留字段 |
| 16 | unitproperty03 | varchar | 255 | 是 | 否 | 预留字段 |
| 17 | unitproperty04 | varchar | 255 | 是 | 否 | 预留字段 |
| 18 | unitproperty05 | varchar | 255 | 是 | 否 | 预留字段 |

#### 文件存储表 file

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | fileid | varchar | 255 | 否 | 否 | 文件序号 |
| 2 | filename | varchar | 255 | 否 | 否 | 文件名称 |
| 3 | filedescription | varchar | 255 | 是 | 否 | 文件描述 |
| 4 | fileupdatetime | timestamp | 0 | 是 | 否 | 文件更新时间 |
| 5 | reserve01 | varchar | 255 | 是 | 否 | 文件存储01 |
| 6 | reserve02 | varchar | 255 | 是 | 否 | 文件存储02 |
| 7 | reserve03 | varchar | 255 | 是 | 否 | 文件存储03 |
| 8 | reserve04 | varchar | 255 | 是 | 否 | 文件存储04 |
| 9 | reserve05 | varchar | 255 | 是 | 否 | 文件存储05 |
| 10 | fileblob | longblob | 0 | 是 | 否 | 传送文件缓存 |

#### 设备操作记录表 operation_reord

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | RecordTime | timestamp | 0 | 否 | 否 | 记录时间 |
| 2 | user | varchar | 128 | 否 | 否 | 用户名称 |
| 3 | OptRemark | varchar | 256 | 否 | 否 | 记录信息 |

#### 点值缓冲区表 pointbuffer

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | time | timestamp | 0 | 否 | 否 | 采集时间 |
| 2 | pointname | varchar | 255 | 否 | 否 | 点名 |
| 3 | pointvalue | varchar | 256 | 否 | 否 | 点值 |

#### 实时数据输入表 realtimedata_input

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | time | timestamp | 0 | 否 | 否 | 采集时间 |
| 2 | pointname | varchar | 64 | 否 | 否 | 点名 |
| 3 | pointvalue | varchar | 256 | 否 | 否 | 点值 |

#### 实时数据输出表 realtimedata_output

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | pointname | varchar | 64 | 否 | 是 | 点名 |
| 2 | pointvalue | varchar | 256 | 否 | 否 | 点值 |

#### 登录用户表 user

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | username | varchar | 64 | 否 | 是 | 用户名称 |
| 2 | userhost | varchar | 64 | 否 | 否 | 用户主机 |
| 3 | priority | int | 10 | 否 | 否 | 优先权 |
| 4 | usertype | varchar | 64 | 否 | 是 | 用户类型 |
| 5 | time | timestamp | 0 | 否 | 否 | 登录时间 |

#### 报警配置表 warning_config

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | HHEnable | int | 10 | 是 | 否 | 高高限是否可用 |
| 2 | HEnable | int | 10 | 是 | 否 | 高限是否可用 |
| 3 | LEnable | int | 10 | 是 | 否 | 低限是否可用 |
| 4 | LLEnable | int | 10 | 是 | 否 | 低低限是否可用 |
| 5 | HHLimit | double | 0 | 是 | 否 | 高高限 |
| 6 | HLimit | double | 0 | 是 | 否 | 高限 |
| 7 | LLimit | double | 0 | 是 | 否 | 低限 |
| 8 | LLLimit | double | 0 | 是 | 否 | 低低限 |
| 9 | pointname | varchar | 255 | 否 | 否 | 点名 |
| 10 | HHwarninginfo | varchar | 255 | 是 | 否 | 高高限报警信息 |
| 11 | Hwarninginfo | varchar | 255 | 是 | 否 | 高限报警信息 |
| 12 | Lwarninginfo | varchar | 255 | 是 | 否 | 低限报警信息 |
| 13 | LLwarninginfo | varchar | 255 | 是 | 否 | 低低限报警信息 |
| 14 | boolwarning | int | 11 | 是 | 否 | 布尔报警 |
| 15 | boolwarninginfo | varchar | 255 | 是 | 否 | 布尔报警信息 |
| 16 | boolwarninglevel | int | 11 | 是 | 否 | 布尔报警等级 |
| 17 | unitproperty01 | varchar | 255 | 是 | 否 | 预留字段 |
| 18 | unitproperty02 | varchar | 255 | 是 | 否 | 预留字段 |
| 19 | unitproperty03 | varchar | 255 | 是 | 否 | 预留字段 |
| 20 | unitproperty04 | varchar | 255 | 是 | 否 | 预留字段 |
| 21 | unitproperty05 | varchar | 255 | 是 | 否 | 预留字段 |

#### 报警记录表 warning_record

| 序号 | 字段名称 | 字段类型 | 大小 | 允许为空 | 是否主键 | 备注 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | time | timestamp | 0 | 否 | 否 | 记录时间 |
| 2 | code | int | 10 | 否 | 否 | 代码 |
| 3 | info | varchar | 1024 | 否 | 否 | 报警信息 |
| 4 | level | int | 10 | 否 | 否 | 报警等级 |
| 5 | endtime | timestamp | 0 | 否 | 否 | 结束时间 |
| 6 | confirmed | int | 10 | 否 | 否 | 确认状态 |
| 7 | confirmeduser | varchar | 2000 | 否 | 否 | 确认的用户名 |
| 8 | bindpointname | varchar | 255 | 是 | 否 | 绑定的点名 |



