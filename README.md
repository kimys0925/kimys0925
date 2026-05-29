# 자기소개
- 이름: 김예서
- 소속: 서강대학교 영미어문/컴퓨터공학 전공
- 2021년~2026년 재학중, 2027년 2월 졸업 예정
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
1. 팀 깃헙
- https://github.com/A3C2-capstone-safety-robot/Industry-safety-robot
2. 개인 깃헙
- README: https://github.com/kimys0925/Industry-safety-robot
<img width="1011" height="184" alt="image" src="https://github.com/user-attachments/assets/5fdc3d42-29bd-40a3-9edf-fadc661e15ff" />

- Unity와 ROS2를 활용한 산업 안전 순찰 로봇 시뮬레이션 프로젝트입니다. <br>
- 개요: 본 프로젝트는 산업 시설 내 안전사고를 예방하고자 지능형 자율 점검 및 대피 안내 로봇 시스템을 구현한다.
열화상 카메라 기반 설비 과열 감지, 나방 탐색 알고리즘을 활용한 능동적 가스 누출원 추적, 가우시안 플룸 모델 기반 동적 대피 경로 산출 등 다양한 안전 점검 기능을 단일 로봇 플랫폼에 통합한다. ROS 2와 Unity 기반의 디지털 트윈 환경에서 로봇의 자율 순찰 및 위험 감지 성능을 검증하며, LLM을 활용한 지능형 상황 보고 기능으로 실시간 대응 능력을 높인다. 이를 통해 사람이 직접 접근하기 어려운 위험 구역의 안전 점검을 자동화하고, 사고 발생 시 신속한 대피를 지원하는 통합 시스템, 통칭 Industrial Robot Inspection & Safety System, 약칭‘IRIS’를 개발하고 제안한다.

- 역할: 자율주행 / 센서 시뮬레이션
- 기술: Unity, C#, ROS2, ROS-TCP-Connector, SLAM Toolbox, Nav2
- 기여:
  - Unity 기반 로봇 수동 조작 기능 구현
  - Physics.Raycast 기반 LiDAR 센서 시뮬레이션 구현
  - ROS2 `/scan` 토픽 publish 구조 설계
  - SLAM Toolbox 및 Nav2 연동을 위한 센서 데이터 구조 설계
