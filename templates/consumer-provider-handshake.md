# Consumer-Provider Handshake

## Thong tin chung

- Lab: FIT4110 Lab 03
- Ngay: 2026-06-02
- Provider team: team-vision
- Consumer team: team-iot
- Provider service: AI Vision
- Consumer service: IoT Ingestion contract test suite

## Contract

- Contract file: contracts/ai-vision.openapi.yaml
- Mock base URL: http://localhost:4011
- Auth method: Bearer token from Postman environment variable `authToken`
- Endpoint duoc test: POST /detect

## Smoke test

### Request

```http
POST /detect
Authorization: Bearer {{authToken}}
Content-Type: application/json
```

```json
{
  "camera_id": "CAM01",
  "image_url": "https://example.com/frame.jpg"
}
```

### Expected response

```json
{
  "detection_id": "DET001",
  "camera_id": "CAM01",
  "label": "person",
  "confidence": 0.91,
  "risk_level": "medium"
}
```

## Ket qua

- [x] Consumer goi mock thanh cong.
- [x] Consumer parse duoc field can dung: `detection_id`, `label`, `confidence`.
- [x] Consumer hieu loi 4xx/5xx provider tra ve qua `ProblemDetails` trong contract.
- [x] Co Newman report: reports/newman-report-mock.xml va reports/newman-report.html.

## Ghi chu thay doi hop dong

| Noi dung | Truoc | Sau | Nguoi dong y |
|---|---|---|---|
| Lab 03 smoke contract | Chua co bang chung chay mock AI Vision | Them consumer-side smoke test `POST {{aiVisionMockUrl}}/detect` | team-iot, team-vision |

## Xac nhan

- Provider representative: team-vision
- Consumer representative: team-iot
