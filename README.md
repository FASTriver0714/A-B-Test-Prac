#  A/B 테스트 분석 (Prac)

## 📌 프로젝트 개요

이커머스 상품 리스트 페이지에서 **상품 이미지 태그(베스트·신상품·세일 등) 추가**가 CTR에 유의미한 영향을 미치는지 검증하기 위한 A/B 테스트 분석 프로젝트입니다.  
실습 목적으로 **가상의 더미 데이터**를 직접 생성하여 분석을 진행했습니다.

> 📌 데이터는 노트북 내 가상 데이터 생성 코드로 직접 생성가능.

---

## 🎯 실험 설계

| 구분 | 내용 |
|---|---|
| **Control 그룹** | 기존안 (상품 이미지 태그 미포함) |
| **Test 그룹** | 개선안 (상품 이미지 태그 포함) |
| **목표 지표** | CTR (클릭수 / 조회수) |
| **가드레일 지표** | 상품 조회수 (Views) |
| **샘플 수** | 50,000명 (각 그룹 50%) |
| **세그먼트** | 연령대 (10s / 20s / 30s / 40s) |

---

## 🔍 분석 내용

1. **목표 지표 검증** — Control / Test 그룹 간 CTR 차이 분석 및 t-test 통계 검정
2. **가드레일 지표 확인** — 조회수(Views) 변화 여부 확인 (부정적 영향 없는지 검증)
3. **세그먼트 분석** — 연령대별 CTR·Views·Clicks 차이 비교 및 통계 검정

---

## 📊 사용 기술

| 분류 | 기술 |
|---|---|
| Language | Python |
| 데이터 처리 | pandas, numpy |
| 시각화 | matplotlib, seaborn |
| 통계 검정 | scipy (t-test) |
| 환경 | Jupyter Notebook, Google Colab |
| 대시보드 | Tableau |


---

## 💡 주요 인사이트

- Test 그룹의 CTR이 Control 대비 약 **25% uplift** 발생 (통계적으로 유의미)
- 가드레일 지표인 조회수(Views)는 두 그룹 간 유의미한 차이 없음 → 부정적 영향 없음
- 연령대별 분석 결과, **20대·30대**에서 Test 그룹의 CTR 상승 효과가 더 두드러짐

## 🧾산출물
[대시보드](https://public.tableau.com/views/ABTest_17590500656410/AB?:language=ko-KR&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) ⬅️ Tableau Public
