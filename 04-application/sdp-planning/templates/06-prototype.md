# 6단계: 레이아웃 구성 (프로토타입)

> 제품명: [제품명 입력]
> 작성일: [YYYY.MM.DD]
> 작성자: [이름]

---

## HTML 기본 구조

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>KISONA — [제품명] 상세페이지</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.4.9/dist/web/variable/pretendardvariable.min.css">
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Noto+Sans+KR:wght@100;300;400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --point-500: #5e81ac;
      --base-100: #1e293b;
      --base-80: #1e293bcc;
      --base-60: #1e293b99;
      --silver: #c8cfd8;
      --red: #f43f5e;
      --white: #ffffff;
      --bg-alt: #f4f7fb;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Pretendard Variable', sans-serif;
      color: var(--base-100);
      background: var(--white);
      max-width: 860px;
      margin: 0 auto;
    }

    /* Typography */
    .h1 { font-size: 28px; font-weight: 700; line-height: 1.4; }
    .h2 { font-size: 22px; font-weight: 600; line-height: 1.4; }
    .h3 { font-size: 18px; font-weight: 500; line-height: 1.5; }
    .body { font-size: 15px; font-weight: 400; line-height: 1.7; color: var(--base-80); }
    .caption { font-size: 12px; font-weight: 400; line-height: 1.5; color: var(--base-60); }
    .data { font-family: 'DM Sans', sans-serif; font-size: 14px; font-weight: 500; }

    /* Section */
    .section { padding: 60px 40px; }
    .section-alt { background: var(--bg-alt); }

    /* Image Placeholder */
    .img-placeholder {
      width: 100%;
      aspect-ratio: 16/9;
      background: linear-gradient(135deg, var(--bg-alt), var(--silver));
      border: 1px solid #e5e7eb;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--base-60);
      font-size: 14px;
    }
  </style>
</head>
<body>
  <!-- 섹션들을 여기에 배치 -->
</body>
</html>
```

---

## 프로토타입 제작 규칙

1. **860px 고정폭** — body에 max-width: 860px
2. **Pretendard 단일 폰트** (영문 데이터만 DM Sans)
3. **풀폭 이미지** — img 태그에 width: 100%
4. **CSS 변수 사용** — 컬러는 :root 변수 참조
5. **이미지 플레이스홀더** — 실제 사진 전 그라데이션 박스 사용

---

## 스크롤 애니메이션 (선택)

```javascript
const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
    }
  });
}, { threshold: 0.1 });
reveals.forEach(el => observer.observe(el));
```

---

## 테스트 체크리스트

### 기능
- [ ] 860px 폭 정상 표시
- [ ] 이미지 플레이스홀더 비율 정상
- [ ] 스크롤 애니메이션 동작 (적용 시)
- [ ] 폰트 로딩 정상

### UX
- [ ] 텍스트 가독성
- [ ] 섹션 간 여백 일관성
- [ ] CTA 위치 적절
- [ ] 전체 흐름 자연스러움

### 성능
- [ ] HTML 파일 크기 적절 (< 200KB)
- [ ] 외부 리소스 최소화

---

## 피드백 수집

| 항목 | 피드백 | 반영 여부 |
|------|--------|----------|
| 전체 흐름 |  |  |
| 텍스트 톤 |  |  |
| 비주얼 방향 |  |  |
| CTA 위치 |  |  |

---

## 다음 단계

- [ ] 7단계: 레이어 구성 (디자인 완성)
- [ ] 실제 제품 사진 교체
- [ ] 최종 카피 확정
