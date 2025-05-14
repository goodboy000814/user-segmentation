# Customer Segmentation using K-Means, PCA, and FAMD

## 📌 프로젝트 개요
본 프로젝트는 **고객 데이터를 기반으로 K-Means 클러스터링**을 수행하여 고객을 유형별로 세분화하고, **PCA와 FAMD를 통한 차원 축소 및 시각화**를 통해 각 군집의 특성을 분석하는 것을 목표로 함.
마케팅 타겟팅, 맞춤형 서비스 제공, 고객 관리 전략에 유용한 인사이트를 얻고자 함.

## 🗂️ 데이터셋 설명
- **데이터 출처**: 내부 고객 데이터
- **데이터 파일명**: `segmentation data.csv`
- **관측치 수**: 2000 obs
- **주요 변수**
  - `Sex`: 성별 (categorical,0=남성, 1=여성)
  - `Marital Status`: 혼인 여부 (categorical,0=single, 1=non-single)
  - `Education`: 교육 수준 (categorical,0,1,2,3)
  - `Occupation`: 직업군 (categorical,0,1,2)
  - `Settlement Size`: 거주지 규모 (categorical,0,1,2)
  - `Income`: 연 소득 (numerical)
  - `Age`: 나이 (numerical)
  - **기타 수치 및 범주형 변수 포함**

## 🛠️ 사용 기술 및 라이브러리
- Python 3.x
- pandas, numpy, scipy
- prince (FAMD)
- matplotlib, seaborn

## 🔍 프로젝트 진행 과정
1. **데이터 로드 및 전처리**
   - CSV 파일 불러오기
   - 결측치 및 이상치 확인
2. **EDA (탐색적 데이터 분석)**
   - 변수별 기술 통계 확인
   - 변수 간 상관관계 분석
3. **데이터 표준화**
   - `StandardScaler` 적용
4. **차원 축소**
   - PCA: 수치형 변수에 적용
   - FAMD: 범주형+수치형 혼합 데이터셋에 적용
5. **클러스터링**
   - Elbow Method로 K 값 결정
   - K-Means 클러스터링 실행
6. **결과 분석**
   - 각 클러스터의 인구통계적 특성 분석
   - 클러스터별 변수 차이 시각화 (2D, 3D plot)
   - 군집별 주요 insight 도출

## 참고자료
- [Step by Step Customer Segmentation using K-Means in Python](https://medium.com/@ugursavci/step-by-step-customer-segmentation-using-k-means-and-pca-in-python-5733822295b6) 을 기반으로 작성됨.



