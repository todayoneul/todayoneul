# 이규한 (Lee Gyuhan)

서울과학기술대학교 컴퓨터공학과에서 컴퓨터비전과 기계학습을 공부하고 있습니다. 배운 내용을 직접 구현해 결과를 확인하고, 기대와 다른 결과가 나오면 데이터와 처리 단계를 나누어 원인을 찾는 방식으로 프로젝트를 진행합니다. 요즘은 카메라 영상과 언어 지시가 로봇의 행동으로 이어지는 과정에 관심을 두고 있습니다.

## 프로젝트

### [Edge-Sign](https://github.com/todayoneul/edge_sign)

도로 주행 영상에서 신호등과 교통표지판을 검출하고 추적한 뒤 종류와 점등 상태를 분류하는 파이프라인입니다. 추론은 브라우저 안에서 ONNX Runtime Web으로 실행하며, [웹 데모](https://huggingface.co/spaces/gyann/edge-sign)로 공개했습니다.

- 주행 영상 8개 시퀀스를 시퀀스 단위로 학습·검증·시험에 나누어 비슷한 프레임이 양쪽에 섞이지 않게 했습니다.
- 검출기 전체를 INT8로 양자화하면 검출이 하나도 나오지 않았습니다. 검출 헤드를 FP32로 남긴 YOLOv8s는 파일 크기가 44.75MB에서 18.00MB로 줄었고 mAP@0.5:0.95는 FP32의 98.7%였습니다.
- INT8의 속도 효과는 실행 환경에 따라 달랐습니다. Windows의 네이티브 CPU와 WebAssembly에서는 최대 2.3배 빨라졌지만 WebGPU에서는 FP32보다 49–89배 느렸습니다.

### [UAV Vision-Language-Action](https://github.com/todayoneul/failure-aware-uav-vla)

문장으로 지시한 물체를 찾아 접근하거나 착륙하는 드론 VLA 모델을 Project AirSim 시뮬레이터에서 학습하고 평가한 개인 프로젝트입니다. 실제 기체 비행은 하지 않았습니다.

- 공개 모델 AeroVLA를 시뮬레이터에 연결해 보니, 좌표로 계산해 넣은 방향 문장을 빼면 13회 모두 첫 판단에서 착륙을 선택했습니다.
- OpenVLA-OFT 방식과 LoRA로 다시 학습한 모델은 봉인한 시험 48개 중 47개를 통과했습니다.
- 입력 영상에 가우시안 블러를 강하게 줄수록 통과 수가 46, 40, 24, 8개로 줄었습니다.
- 다음 단계로 CARLA에서 자연어로 지정한 차량을 따라가는 과제를 준비하고 있습니다.

### [QRC2026](https://github.com/todayoneul/QRC2026)

Quantum Reframing Challenge 2026 본선에 5인 팀으로 참가한 프로젝트입니다. 대회에서 제공한 지식 그래프에서 기업과 기술의 조합을 고르는 최적화 문제를 CP-SAT, Simulated Annealing, QAOA로 풀고 비교했습니다.

- 저는 풀이 방법마다 다른 형식의 답을 원래 문제의 제약조건과 목적함수로 다시 계산하는 공통 검증기와, 양자 계산을 호출할지 판정하는 라우터를 맡았습니다.
- 대회 문제(결정 변수 67개)는 CP-SAT이 최적해임을 증명해 라우터가 양자 계산을 호출하지 않았습니다.
- QAOA는 시뮬레이터에서만 실행했고 실제 양자 하드웨어는 사용하지 않았습니다.

### [HCX05 Disclosure Agent](https://github.com/todayoneul/HCX05-disclosure-agent)

미래에셋증권 AI 페스티벌에서 만든 한국어 기업 공시 질의응답 에이전트입니다. 재무 수치 조회나 비율 계산 같은 정형 질의는 모델을 거치지 않고 도구가 직접 처리하고, 복합 질의만 HyperCLOVA X(HCX-005)가 도구 호출을 조율합니다. 수치 계산에는 Python Decimal을 사용하며, 답변의 수치와 인용이 수집한 근거와 맞지 않으면 답을 내지 않습니다.

### [따릉이 수요 분석](https://github.com/todayoneul/ddarungyee)

서울시 공공자전거 대여 기록을 기상, 상권, 주말 여부와 결합해 수요가 달라지는 조건을 분석한 데이터분석 수업 프로젝트입니다. 상권에 따라 주말 효과의 방향이 달라지는지 검정했고, 스플라인과 GAM으로 기온과 수요의 비선형 관계를 살펴봤습니다.

### 컴퓨터비전 수업 프로젝트

- [카메라 캘리브레이션](https://github.com/todayoneul/my_camera_calibrator): 직접 촬영한 체스보드 영상으로 카메라 특성을 구하고 왜곡을 보정했습니다.
- [AR 카메라 자세 추정과 3D 렌더링](https://github.com/todayoneul/AR_Camera_Pose_Estimation_and_3D_Rendering): 체스보드를 기준으로 카메라의 위치와 방향을 추정해 영상 위에 OBJ 모델을 그렸습니다.
- [파노라마 스티칭](https://github.com/todayoneul/Image_Stitching_And_Panoramic_Blending): 세 장 이상의 사진을 호모그래피 추정과 워핑, 블렌딩으로 이어 붙였습니다.

## 참가 이력

- Quantum Reframing Challenge 2026 본선
- LG Aimers 8기 오프라인 해커톤 본선
- 2026 미래에셋증권 AI 페스티벌
- Kakao PlayMCP ([youth-policy-mcp](https://github.com/todayoneul/youth-policy-mcp))

## 사용 기술

Python, PyTorch, OpenCV, ONNX Runtime, FastAPI, Docker, Git
