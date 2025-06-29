---
sidebar_position: 1
---

# API

First get your token log into [https://app.uswork.ai/api-tokens](https://app.uswork.ai/api-tokens) and get your token.



## Get Available Jobs

GET request to:


### Headers

```http
Authorization: Bearer YOUR_USWORK_TOKEN
Content-Type: application/json
```

### Example cURL

```bash
curl -X GET "https://your-api-url.com/api/resource" \
  -H "Authorization: Bearer YOUR_USWORK_TOKEN" \
  -H "Content-Type: application/json"
```

### Response

```json
[
    {
        "data": [
            {
                "id": "4f1288b0-5b03-4bc9-b11f-48e66d0a3a25",
                "title": "Test New Job 002",
                "description": "y. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.\n\nWhy do we use it?\nIt is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy. Various versions have evolved over the years, sometimes by accident, sometimes on purpose (injected humour and the like).\n\n\nWhere does it come from?\nContrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of \"de Finibus Bonorum et Malorum\" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, \"Lorem ipsum dolor sit amet..\", comes from a line in section 1.10.32.\n\nThe standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from \"de Finibus Bonorum et Malorum\" by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham.\n\nWhere can I get some?\nThere are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words which don't look even slightly believable. If you are going to use a passage of Lorem Ipsum, you need to be sure there isn't anything embarrassing hidden in the middle of text. All t",
                "tags": [
                    "Test"
                ],
                "status": "available",
                "created_by": "22980e21-2746-4269-ac3c-30febc6adb3d",
                "budget_min": "400",
                "budget_max": "900",
                "deadline": "2025-07-02T00:00:00.000Z",
                "created_at": "2025-06-27T16:18:29.604Z",
                "updated_at": "2025-06-27T16:18:29.604Z"
            }
        ],
        "pagination": {
            "count": 1,
            "per_page": 200,
            "next_cursor": "4f1288b0-5b03-4bc9-b11f-48e66d0a3a25",
            "next_created_at": "2025-06-27T16:18:29.604Z"
        },
        "has_next_page": false
    }
]
```

## POST Proposal

## Create Job Proposal

POST request to:

```
https://n8n-uswork.apps.thedailyaistudio.com/webhook/job_proposals/create
```

### Headers

```http
Authorization: Bearer YOUR_SUPABASE_JWT_TOKEN
Content-Type: application/json
```

### Example Payload

```json
{
  "job_id": "4f1288b0-5b03-4bc9-b11f-48e66d0a3a25",
  "content": "This is my proposal for the job. I have experience with...",
  "proposed_rate": 800
}
```

### Example cURL

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

