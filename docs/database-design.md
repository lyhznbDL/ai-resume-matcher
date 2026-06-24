# 数据库设计

## 表清单

| 表名 | 说明 |
|:---|:---|
| job_description | 岗位 JD 表 |
| resume | 简历表 |
| skill_keyword | 技能关键词表 |
| match_result | 匹配结果表 |
| user | 用户表 |

## job_description 表

| 字段 | 类型 | 说明 |
|:---|:---|:---|
| id | BIGINT | 主键 |
| company_name | VARCHAR(100) | 公司名称 |
| job_title | VARCHAR(100) | 岗位名称 |
| raw_text | TEXT | JD 原文 |
| created_at | DATETIME | 创建时间 |

## resume 表

| 字段 | 类型 | 说明 |
|:---|:---|:---|
| id | BIGINT | 主键 |
| user_id | BIGINT | 用户ID |
| raw_text | TEXT | 简历原文 |
| created_at | DATETIME | 创建时间 |

## 其他表待补充...
