# 자기소개
- 이름: 김예서
- 소속: 서강대학교 영미어문/컴퓨터공학 복수전공
- 2021년~2026년 재학중, 2027년 2월(8월) 졸업 예정
<br>

# 진행 프로젝트
## 1. CV 팀 프로젝트 (멋쟁이사자처럼): 2025.12~2026.02
### i. 주행 중 동적/정적 물체 3D 객체탐지<br>
- https://github.com/kimys0925/3D_objectdetection<br>
- 차세대 3D 객체 탐지 알고리즘인 CenterPoint를 구현하고 성능을 분석한 프로젝트입니다.
기존 Anchor-based 모델인 PointPillars의 한계를 극복하기 위해 Anchor-free, Heatmap-based 방식의 효율성을 검토했습니다.
제한된 데이터셋인 nuScenes v1.0-mini 환경에서 모델이 공간 정보를 어떻게 학습하고 일반화하는지 분석했습니다.

### ii. 배터리 불량 검출 Segmentation 프로젝트<br>
- https://github.com/jueuni135-spec/segmentation_factory<br>
- 본 프로젝트는 배터리 생산 공정에서 발생할 수 있는 불량을 이미지 기반으로 검출하기 위한 Semantic Segmentation 프로젝트입니다.
AI-Hub의 배터리 불량 이미지 데이터를 활용하여 정상/불량 이미지와 결함 마스크를 분석하고, 실제 제조 공정에서 활용 가능한 결함 탐지 모델을 구현하는 데 초점을 맞췄습니다.

- 프로젝트 내에서는 데이터셋 선정 과정에 참여하여 기존 샘플 데이터의 한계를 검토하고, 정상/불량 데이터 비율과 라벨 신뢰도를 고려해 학습에 적합한 데이터 구성을 선택했습니다. 또한 JSON Annotation을 Pixel 기반 Mask로 변환하는 전처리 흐름을 바탕으로, 모델 학습에 적합한 데이터 구조를 정리했습니다.

- 모델 측면에서는 SegFormer와 Attention U-Net 계열 모델의 성능 개선을 담당했습니다. 특히 Attention U-Net에 MobileNetV3 Encoder를 적용해 모델을 경량화하고, Hybrid Loss, Focal Tversky Loss, Deep Supervision 등의 방법을 실험하며 결함 영역에 대한 탐지 성능을 높이는 방향으로 고도화를 진행했습니다. 이를 통해 제조 현장에서 요구되는 정밀도와 실시간 적용 가능성 사이의 균형을 고민해볼 수 있었습니다. <br>

### iii. 열화 예지보전 멀티모달 프로젝트 (⭐해당 프로젝트는 본인이 데이터셋과 주제를 선정하여 진행하였음)<br>
- https://github.com/lim1004567/AICV03_Multimodal-Predictive-Maintenance<br>

- 본 프로젝트는 제조 현장에서 사용되는 이송장치인 OHT와 AGV의 열화 상태를 예측하기 위한 멀티모달 예지보전 프로젝트입니다.
열화상 이미지와 센서 시계열 데이터를 함께 활용하여 장비의 현재 상태뿐 아니라 30초 후 위험도를 예측하고, 이를 실시간 대시보드로 시각화하는 것을 목표로 진행했습니다.<br>

- 프로젝트 초반에는 직접 주제와 데이터셋을 선정하고, 제조 현장 내 설비 이상 감지와 예지보전의 필요성을 바탕으로 문제를 정의했습니다. 이후 열화상 이미지와 센서 데이터를 함께 처리할 수 있는 멀티모달 구조가 필요하다고 판단하여, 관련 가이드 논문을 선정하고 모델 구조를 분석했습니다. <br>

- 구현 단계에서는 가이드 논문에 근거하여 Multimodal Transformer 기반의 베이스라인 모델을 구현하고, 이미지 패치 토큰과 센서 시계열 토큰을 하나의 시퀀스로 융합하여 Self-Attention을 통해 두 데이터 간의 관계를 학습하도록 설계했습니다.<br>
   
## 2. 서강대 캡스톤디자인 팀 프로젝트: 2026 상반기

### IRIS (Industrial Robot Inspection & Safety System)

**산업안전 자율점검 및 대피 안내 로봇 시스템**

**GitHub**

- 팀: [https://github.com/A3C2-capstone-safety-robot/Industry-safety-robot](https://github.com/A3C2-capstone-safety-robot/Industry-safety-robot)
- 개인: [https://github.com/kimys0925/Industry-safety-robot](https://github.com/kimys0925/Industry-safety-robot)



### 프로젝트 개요

산업 시설 내 안전사고 예방을 위한 자율점검 및 대피 안내 로봇 시스템 개발. 열화상 카메라 기반 과열 감지, 나방 탐색 알고리즘 기반 가스 누출원 추적, 가우시안 플룸 모델 기반 동적 대피 경로 산출 및 LLM 사고 보고 기능을 통합. ROS2와 Unity 기반 디지털 트윈 환경에서 시스템 동작 검증.

### 기술 스택

ROS2, Nav2, Python, Unity

### 담당 업무

- ROS2·Nav2 기반 자율주행 모듈 개발 및 Unity 가상 로봇 간 통신 연동
- 공장 구조 및 설비 배치 변화에 대응하는 순찰 지점 기반 동적 경로 생성 방식 설계
- 과열·가스 누출 등 위험 유형별 판단 및 대응 로직 구현
- ROS2 Topic 기반 자율주행, 대피 안내, 관제 대시보드 및 LLM 사고 보고 모듈 연동
- 위험 시나리오별 시스템 통합 테스트 및 검증

### 성과

- 공장 구조 변화에 대응할 수 있는 시스템 확장성 확보
- 서강대학교 캡스톤디자인 경진대회 장려상 수상

---

## 3. NAVER Cloud & AI 부트캠프 1기: 2026.07 \~ 2026.08

### 교육 내용

- VPC 기반 클라우드 네트워크 설계
- Public/Private Subnet 구성 및 ACG 기반 접근 제어
- DB 이중화 및 로드밸런서를 활용한 고가용성 인프라 설계
- CLOVA Studio 기반 LLM 튜닝, 프롬프트 체이닝 및 AI API 연동
- Sliding Window 기반 데이터 처리 및 토큰 관리

### 팀 프로젝트: YouTalk

**유튜브 영상 자막 기반 RAG 챗봇 서비스 개발 및 NAVER Cloud 배포**

### 프로젝트 개요

유튜브 영상 자막을 기반으로 영상 분석 및 질의응답 기능을 제공하는 RAG 챗봇 서비스 개발. 영상 분석과 채팅 응답 서버를 분리하고, 보안성과 운영 효율성을 고려한 클라우드 인프라 구축 및 서비스 배포.

### 기술 스택

Python, RAG, PostgreSQL, NAVER Cloud, Kubernetes, GitHub Actions

### 담당 업무

- 백엔드 개발 및 API·Worker·Chat 서버 분리
- Cache DB 및 PostgreSQL 연동
- VPC 기반 클라우드 인프라 구축 및 배포 참여
- Kubernetes 운영 및 GitHub Actions 기반 자동 배포 환경 활용
- TTS 병렬 처리 및 캐싱을 통한 응답 성능 개선

### 성과

- TTS 응답 속도 순차 처리 대비 2.3배 개선
- NAVER Cloud 환경 서비스 배포
- NAVER Cloud AI 프로젝트 대상 수상

---

## 4. 서강대 캡스톤디자인 팀 프로젝트: 2026 하반기 (진행 중)

### 스마트 홈 안심 방범문

**4D Imaging AI 레이더 기반 주거 침입 및 이상행동 감지 시스템**

### 프로젝트 개요

4D Imaging AI 레이더(RETINA-4SN)를 활용해 현관 주변 인원의 이동 방향, 속도, 체류 시간 등을 분석하고 위험 상황을 판단하는 홈 보안 시스템 개발. 위험 감지 시 카메라 촬영 및 모바일 앱 알림을 제공하며, 다양한 아파트 구조에 적용할 수 있는 시스템 구축을 목표로 함.

### 기술 스택

Python, RETINA-4SN, Scikit-learn, Raspberry Pi, FastAPI, PostgreSQL, Flutter

### 주요 개발 내용 및 담당 업무

- 레이더 포인트 클라우드 데이터 수집·전처리 및 CSV 변환
- 이동 궤적 시각화·분석을 통한 행동 패턴 정의
- Decision Tree 기반 위험 상황 분류 알고리즘 개발
- Raspberry Pi 기반 카메라 촬영 기능 구현
- 3D 레이더 감지 영역 시뮬레이터 개발 및 아파트 구조별 감지 사각지대를 최소화하는 설치 위치 분석
- 현관 위치 및 복도 방향에 따른 상황 분류 기준 보정 기능 개발 중
- FastAPI 서버 및 모바일 앱과 연계한 실시간 위험 감지·촬영·알림 시스템 통합 진행 중


- 역할: 자율주행 / 센서 시뮬레이션
- 기술: Unity, C#, ROS2, ROS-TCP-Connector, SLAM Toolbox, Nav2
- 기여:
  - Unity 기반 로봇 수동 조작 기능 구현
  - Physics.Raycast 기반 LiDAR 센서 시뮬레이션 구현
  - ROS2 `/scan` 토픽 publish 구조 설계
  - SLAM Toolbox 및 Nav2 연동을 위한 센서 데이터 구조 설계
