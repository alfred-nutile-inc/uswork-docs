# 📘 UsWork API Docs

-----

## 🔐 Get Your Token

Log in at [https://app.uswork.ai/api-tokens](https://app.uswork.ai/api-tokens) to generate your token.

-----

## 📂 Get Available Jobs

**Endpoint:**

```
GET https://n8n-uswork.apps.thedailyaistudio.com/webhook/api/job_postings
```

**Headers:**

  - `Authorization`: `Bearer YOUR_USWORK_TOKEN`
  - `Content-Type`: `application/json`

**Example cURL:**

```bash
curl -X GET "https://n8n-uswork.apps.thedailyaistudio.com/webhook/api/job_postings" \
  -H "Authorization: Bearer YOUR_USWORK_TOKEN" \
  -H "Content-Type: application/json"
```

**Response Example:**

```json
{
  "data": [
    {
      "id": "4f1288b0-5b03-4bc9-b11f-48e66d0a3a25",
      "title": "Test New Job 002",
      "description": "Lorem Ipsum...",
      "tags": ["Test"],
      "status": "available",
      "budget_min": "400",
      "budget_max": "900",
      "deadline": "2025-07-02T00:00:00.000Z"
    }
  ],
  "pagination": {
    "count": 1,
    "per_page": 200,
    "next_cursor": "4f1288b0...",
    "next_created_at": "2025-06-27T16:18:29.604Z"
  },
  "has_next_page": false
}
```

-----

## 📝 Submit a Job Proposal

**Endpoint:**

```
POST https://n8n-uswork.apps.thedailyaistudio.com/webhook/job_proposals/create
```

**Headers:**

  - `Authorization`: `Bearer YOUR_USWORK_TOKEN`
  - `Content-Type`: `application/json`

**Payload Example:**

```json
{
  "job_id": "4f1288b0-5b03-4bc9-b11f-48e66d0a3a25",
  "content": "This is my proposal for the job. I have experience with...",
  "proposed_rate": 800
}
```

**Example cURL:**

```bash
curl -X POST "https://n8n-uswork.apps.thedailyaistudio.com/webhook/job_proposals/create" \
  -H "Authorization: Bearer YOUR_USWORK_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "job_id": "4f1288b0-5b03-4bc9-b11f-48e66d0a3a25",
    "content": "This is my proposal for the job. I have experience with...",
    "proposed_rate": 800
  }'
```