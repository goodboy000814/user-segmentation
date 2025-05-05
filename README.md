# Customer Segmentation using K-Means, PCA, and FAMD

## 📌 프로젝트 개요
본 프로젝트는 **고객 데이터를 기반으로 K-Means 클러스터링**을 수행하여 고객을 유형별로 세분화하고, **PCA와 FAMD를 통한 차원 축소 및 시각화**를 통해 각 군집의 특성을 분석하는 것을 목표로 합니다.

마케팅 타겟팅, 맞춤형 서비스 제공, 고객 관리 전략에 유용한 인사이트를 제공합니다.

## 🎯 문제 정의
기업의 고객 데이터를 분석하여 **소득, 소비 패턴, 인구통계학적 변수** 등을 고려한 **고객군 세분화**를 수행합니다. 이를 통해 각 군집의 특징을 파악하고, 실질적 비즈니스 전략에 활용 가능한 정보를 도출합니다.

## 🗂️ 데이터셋 설명
- **데이터 출처**: 내부 고객 데이터
- **데이터 파일명**: `segmentation data.csv`
- **관측치 수**: (index 포함) 약 900명
- **주요 변수**
  - `Sex`: 성별 (0=남성, 1=여성)
  - `Marital Status`: 혼인 여부 (0=single, 1=non-single)
  - `Education`: 교육 수준 (0~3)
  - `Occupation`: 직업군 (0~2)
  - `Settlement Size`: 거주지 규모 (0~2)
  - `Income`: 연 소득
  - `Age`: 나이
  - `Spending`: 소비 점수
  - **기타 수치 및 범주형 변수 포함**

## 🛠️ 사용 기술 및 라이브러리
- Python 3.x
- pandas, numpy, scipy
- scikit-learn
- prince (FAMD)
- matplotlib, seaborn

> **팁:** `prince` 패키지는 FAMD(Factor Analysis of Mixed Data) 적용 시 필요합니다. 설치 시 `pip install prince` 명령어를 사용하세요.

## 🔍 프로젝트 진행 과정
1. **데이터 로드 및 전처리**
   - CSV 파일 불러오기
   - 범주형 변수 매핑
   - 결측치 및 이상치 확인
2. **EDA (탐색적 데이터 분석)**
   - 변수별 기술 통계 확인
   - 변수 간 상관관계 분석
   - 변수별 분포 시각화
3. **데이터 표준화**
   - `StandardScaler` 적용
4. **차원 축소**
   - PCA: 수치형 변수에 적용
   - FAMD: 혼합형 변수에 적용
5. **클러스터링**
   - Elbow Method로 K 값 결정
   - K-Means 클러스터링 실행
6. **결과 분석**
   - 각 클러스터의 인구통계적 특성 분석
   - 클러스터별 변수 차이 시각화 (2D, 3D plot)
   - 군집별 주요 insight 도출

## 🏆 주요 결과
- 최적의 클러스터 수: **4개**
- 각 클러스터 특성:
  - **Cluster 0**: 고소득, 중년층, 소비 점수 낮음
  - **Cluster 1**: 저소득, 젊은층, 소비 점수 높음
  - **Cluster 2**: 중소득, 고연령, 안정적 소비
  - **Cluster 3**: 다양한 연령대, 고소득, 소비 점수 평균
- PCA/FAMD를 통한 차원 축소 시 **군집 간 시각적 분리 가능**

## 🚀 실행 방법
1. 이 저장소를 클론합니다.
   ```bash
   git clone https://github.com/사용자명/저장소명.git

# Customer Segmentation using K-Means, PCA, and FAMD

이 프로젝트는 고객 데이터를 기반으로 **PCA (주성분 분석)**, **FAMD (혼합 데이터 요인 분석)**, **K-Means Clustering**을 활용하여 고객 세분화를 수행한 Python 분석 노트북입니다.

## 📌 프로젝트 개요

- **데이터**: 수치형 및 범주형 데이터 혼합
- **주요 기법**:
  - PCA를 통한 수치형 변수 차원 축소
  - FAMD를 통한 수치형 + 범주형 변수 혼합 차원 축소
  - K-Means로 군집화
- **분석 목적**: 고객 세그먼트 이해 및 데이터 시각화

## 📂 파일 구성

- `customer_segmentation_kmeans-PCA,FAMD.ipynb` : 주석 추가된 분석 노트북
- `README.md` : 프로젝트 설명 문서

## 🏃 실행 방법

1. 필요한 라이브러리 설치:

```bash
pip install pandas matplotlib seaborn scikit-learn prince
