# Reliability Checklist - FIT4110 Lab 03

Checklist completed for the IoT Ingestion contract test suite.

## 1. Functional tests

- [x] Co test cho endpoint health.
- [x] Co test happy path cho endpoint chinh.
- [x] Co kiem tra status code 2xx.
- [x] Co kiem tra field quan trong trong response.
- [x] Co it nhat 1 test doc du lieu danh sach hoac chi tiet.

## 2. Auth tests

- [x] Co test thieu token.
- [x] Co test sai token hoac token rong.
- [x] Endpoint public duoc khai bao ro neu khong can auth.
- [x] Test the hien dung expected status 401/403 tren local service. Tren mock, auth middleware that duoc ghi chu la khong duoc Prism chung minh.

## 3. Negative tests

- [x] Co test thieu field bat buoc.
- [x] Co test sai kieu du lieu.
- [x] Co test sai enum hoac gia tri ngoai mien.
- [x] Loi tra ve theo cung mot error model `ProblemDetails`.

## 4. Boundary tests

- [x] Co test min/max hoac du lieu sat nguong.
- [x] Co test limit/pagination neu endpoint co danh sach.
- [x] Co test payload lon hoac metadata thieu.
- [x] Co ghi chu ky vong xu ly du lieu bien.

## 5. Reliability tests co ban

- [x] Co kiem tra response time cho local-only non-functional test.
- [x] Co mo ta timeout mong muon trong CI bang `wait-on --timeout 30000`.
- [x] Co ghi chu retry/idempotency/rate limit qua response `429 Too Many Requests` trong OpenAPI contract.
- [x] Co consumer-side smoke test voi mock AI Vision.

## 6. Evidence

- [x] Collection export JSON.
- [x] Environment mock export JSON.
- [x] Environment local export JSON.
- [x] Newman report XML/HTML.
- [x] Test-case matrix da dien.
- [x] Bien ban handshake da dien.
