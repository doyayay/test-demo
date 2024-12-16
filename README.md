# 샘플 API 데이터 저장소

## 소개
이 저장소는 개발 및 테스트 목적으로 사용할 수 있는 샘플 API 데이터를 제공합니다.

## 데이터 구조
- `data/users.json`: 사용자 프로필 데이터
- `data/products.json`: 상품 정보
- `data/orders.json`: 주문 데이터

## 설치 방법
```bash
git clone https://github.com/yourusername/sample-api-data.git
cd sample-api-data
```

## API 엔드포인트
기본 URL: `https://api.example.com`

### 사용 가능한 엔드포인트:
- GET /api/v1/users - 사용자 목록 조회
- GET /api/v1/products - 상품 목록 조회
- POST /api/v1/orders - 새로운 주문 생성

## 테스트
```bash
# 단위 테스트 실행
npm run test

# 통합 테스트 실행
npm run test:integration
```

## 기여 방법
1. 저장소를 포크합니다
2. 새로운 브랜치를 생성합니다 (`git checkout -b feature/AmazingFeature`)
3. 변경사항을 커밋합니다 (`git commit -m '새로운 기능 추가'`)
4. 브랜치에 푸시합니다 (`git push origin feature/AmazingFeature`)
5. Pull Request를 생성합니다

## 라이선스
MIT License
