## 설치 방법

### Android

```
dependencies {
    implementation 'com.fashionapp:analytics-sdk:1.0.0'
}
```

### iOS

```swift
// CocoaPods
pod 'FashionAnalytics', '~> 1.0.0'

// Swift Package Manager
dependencies: [
    .package(url: "https://github.com/fashionapp/analytics-ios.git", from: "1.0.0")
]
```

## SDK 초기화

### Android

```kotlin
class MyApplication : Application() {
    override fun onCreate() {
        super.onCreate()
        FashionAnalytics.initialize(
            context = this,
            apiKey = "YOUR_API_KEY",
            userId = "USER_ID"
        )
    }
}
```

### iOS

```swift
import FashionAnalytics

@main
class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
        FashionAnalytics.initialize(
            apiKey: "YOUR_API_KEY",
            userId: "USER_ID"
        )
        return true
    }
}
```

## 이벤트 트래킹

### Android

```kotlin
// 제품 조회
FashionAnalytics.trackEvent("view_product", mapOf(
    "product_id" to "123",
    "product_name" to "청바지",
    "category" to "하의"
))

// 장바구니 추가
FashionAnalytics.trackEvent("add_to_cart", mapOf(
    "product_id" to "123",
    "quantity" to 1,
    "price" to 29900
))

// 구매 완료
FashionAnalytics.trackEvent("purchase", mapOf(
    "order_id" to "ORDER_123",
    "total_amount" to 29900,
    "products" to listOf(
        mapOf(
            "product_id" to "123",
            "quantity" to 1,
            "price" to 29900
        )
    )
))
```

### iOS

```swift
// 제품 조회
FashionAnalytics.trackEvent("view_product", properties: [
    "product_id": "123",
    "product_name": "청바지",
    "category": "하의"
])

// 장바구니 추가
FashionAnalytics.trackEvent("add_to_cart", properties: [
    "product_id": "123",
    "quantity": 1,
    "price": 29900
])

// 구매 완료
FashionAnalytics.trackEvent("purchase", properties: [
    "order_id": "ORDER_123",
    "total_amount": 29900,
    "products": [
        [
            "product_id": "123",
            "quantity": 1,
            "price": 29900
        ]
    ]
])
```

## 사용자 속성 설정

### Android

```kotlin
FashionAnalytics.setUserProperties(mapOf(
    "age" to 25,
    "gender" to "female",
    "favorite_category" to "의류"
))
```

### iOS

```swift
FashionAnalytics.setUserProperties([
    "age": 25,
    "gender": "female",
    "favorite_category": "의류"
])
```

## 주요 이벤트 목록

| 이벤트명 | 설명 | 주요 속성 |
| --- | --- | --- |
| view_product | 제품 상세 조회 | product_id, product_name, category |
| add_to_cart | 장바구니 추가 | product_id, quantity, price |
| remove_from_cart | 장바구니 제거 | product_id |
| purchase | 구매 완료 | order_id, total_amount, products |
| search | 검색 | keyword, category |
| login | 로그인 | method |
| signup | 회원가입 | method |
