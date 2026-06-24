# ai-resume-matcher

## 项目背景

我在准备 2027 届暑期实习投递时发现，不同公司的 AI 应用开发、Java 后端、测试开发岗位要求差异很大，手动判断岗位和简历匹配度效率低。因此设计这个项目，用于录入岗位 JD 和简历文本，自动提取技能关键词，输出匹配度、能力差距和学习建议。

## 技术栈

- Java / Spring Boot
- MySQL / MyBatis
- Python 文本处理脚本
- Git / GitHub
- 后续计划：LLM API、Prompt、RAG、Agent

## 核心功能

- 岗位 JD 录入
- 简历文本录入
- 技能关键词提取
- 匹配度评分
- 能力差距分析
- 投递状态管理
- 学习任务生成

## 数据库设计草稿

### job_position

| 字段 | 含义 |
|---|---|
| id | 岗位ID |
| company_name | 公司名称 |
| job_name | 岗位名称 |
| city | 工作城市 |
| job_description | 岗位描述 |
| status | 投递状态 |

### resume_profile

| 字段 | 含义 |
|---|---|
| id | 简历ID |
| content | 简历文本 |
| target_role | 目标岗位 |

### match_result

| 字段 | 含义 |
|---|---|
| id | 匹配结果ID |
| job_id | 岗位ID |
| resume_id | 简历ID |
| score | 匹配分数 |
| missing_skills | 缺失技能 |
| suggestions | 学习建议 |

## API 设计草稿

| 方法 | 路径 | 功能 |
|---|---|---|
| POST | /api/jobs | 新增岗位 |
| GET | /api/jobs | 查询岗位 |
| POST | /api/resumes | 新增简历文本 |
| POST | /api/match/analyze | 分析岗位匹配度 |
| PUT | /api/applications/{id}/status | 更新投递状态 |

## 当前进度

- [x] 项目背景和需求分析
- [x] README 初版
- [ ] 数据库设计
- [ ] Spring Boot 项目初始化
- [ ] 岗位录入接口
- [ ] 匹配评分逻辑
- [ ] GitHub 提交记录

## 面试可讲点

第一版项目不追求复杂模型，而是先把岗位 JD、简历文本、技能关键词和投递记录打通。后续会接入大模型 API，用 Prompt 约束输出为 JSON，再引入 RAG 做岗位知识库检索。
```
