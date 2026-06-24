# API 设计

## 接口清单

| 接口 | 方法 | 路径 | 说明 |
|:---|:---|:---|:---|
| 录入 JD | POST | /api/jobs | 上传岗位描述 |
| 查询 JD | GET | /api/jobs | 查询岗位列表 |
| 录入简历 | POST | /api/resumes | 上传简历文本 |
| 执行匹配 | POST | /api/match/analyze | 匹配岗位和简历 |
| 获取结果 | GET | /api/match/{id} | 查看匹配结果 |

## 录入 JD

```http
POST /api/jobs
Content-Type: application/json

{
  "company_name": "帆软",
  "job_title": "后端开发实习生",
  "raw_text": "..."
}
