<div align="center">

# 이규한 | Lee Gyuhan

### AI/ML · Computer Vision · LLM Systems · Optimization

모델을 학습하는 것에서 끝나지 않고, **데이터 → 모델링 → 검증 → 최적화 → 배포**까지 이어지는 AI 시스템을 만드는 데 관심이 있습니다.

</div>

---

## 👋 About Me

컴퓨터공학을 공부하는 학부생으로, 실제 문제를 **재현 가능하게 정의하고 정량적으로 검증하는 과정**을 중요하게 생각합니다.

- 🔭 관심 분야: **AI/ML Systems, Computer Vision, LLM/RAG, Agent, Optimization**
- ⚡ 제한된 연산 자원에서 동작하는 **Efficient / On-device AI**에 관심이 있습니다.
- 🧠 LLM을 단순 생성 모델이 아니라 **검색, 도구 사용, 검증을 포함한 시스템**으로 설계하는 데 관심이 있습니다.
- 📊 모델 정확도뿐 아니라 **latency, memory, constraint satisfaction, reproducibility**까지 함께 평가하려고 합니다.
- 🛠️ 아이디어와 실험을 실제 동작하는 데모와 배포 가능한 파이프라인으로 연결하는 것을 좋아합니다.

---

## 🚀 Featured Projects

### 🚦 [Edge-Sign](https://github.com/todayoneul/edge_sign)
**초경량 On-device 교통표지판·신호등 인식 시스템**

검출 → 추적 → 인식 전체 파이프라인을 구성하고, 각 단계의 양자화 민감도와 실제 배포 runtime을 비교했습니다.

- YOLO 기반 detection, ByteTrack tracking, 표지판·신호등 recognition 파이프라인 구성
- 단계별 quantization 실험을 통해 정확도·모델 크기·추론 속도를 함께 비교
- 실측 INT8 모델 **11.7 MB**, CPU **56.3 FPS** 달성
- ONNX, WebGPU, Docker를 활용한 실시간 데모 및 배포 환경 구성
- 인식 결과를 LLM 기반 scene Q&A와 연결

**Tech:** PyTorch · ONNX · OpenCV · WebGPU · Quantization · Computer Vision

---

### ⚛️ [QRC2026 — Evidence-Grounded Quantum Strategic Portfolio Optimizer](https://github.com/todayoneul/QRC2026)
**Quantum Reframing Challenge 2026 본선 프로젝트**

기업·기술 Knowledge Graph를 제한된 예산과 다양한 비즈니스 제약 아래에서 선택하는 문제로 정의하고, Classical / Quantum 접근을 동일한 검증 기준으로 비교했습니다.

- Knowledge Graph 기반 기업·기술 조합 문제를 constrained optimization으로 모델링
- **CP-SAT · Simulated Annealing · QAOA** 비교 실험
- 고전 해법으로 충분한 경우 양자를 호출하지 않는 **Quantum No-call Router** 설계
- 후보해를 원 목적함수와 hard constraints 기준으로 다시 확인하는 **Common Validator** 구성
- QUBO / Ising formulation, Safe Presolve, reduced kernel, QAOA simulation 실험

**Tech:** Qiskit · QAOA · OR-Tools · CP-SAT · Optimization · Knowledge Graph

---

### 🧭 [Youth Policy Navigator](https://github.com/todayoneul/youth-policy-mcp)
**청년 정책 검색·자격 판정을 위한 MCP Server**

Kakao PlayMCP 공모전을 위해 청년 정책을 검색하고, 사용자의 조건에 따라 지원 가능 여부와 판단 근거를 반환하는 MCP 서버를 개발했습니다.

- 공공 정책 데이터와 Contextual BM25를 결합한 검색
- 나이·지역·소득·취업 상태를 기반으로 한 deterministic eligibility check
- 부족한 정보를 다시 질문하고 저장한 뒤 재판정하는 agentic loop 설계
- SQLite 기반 memory와 Docker / remote MCP 실행 환경 구성

**Tech:** MCP · Python · BM25 · SQLite · Docker · Agentic AI

---

### 📷 Computer Vision & 3D Geometry

Computer Vision의 기본 원리를 직접 구현하며 camera geometry와 image processing을 학습했습니다.

- [AR Camera Pose Estimation & 3D Rendering](https://github.com/todayoneul/AR_Camera_Pose_Estimation_and_3D_Rendering)
- [Image Stitching & Panoramic Blending](https://github.com/todayoneul/Image_Stitching_And_Panoramic_Blending)
- [Camera Calibration](https://github.com/todayoneul/my_camera_calibrator)

**Tech:** OpenCV · Camera Geometry · Homography · Pose Estimation · Image Processing

---

## 🏆 Activities & Competitions

| 활동 | 내용 |
|---|---|
| **Quantum Reframing Challenge 2026** | 예선 통과 및 본선 진출 · KG 기반 조합 최적화 · CP-SAT / SA / QAOA |
| **2026 미래에셋 AI Festival** | 기업 공시 데이터 기반 retrieval · correction history · grounded AI agent 구축 |
| **Kakao PlayMCP 공모전** | 청년 정책 검색·자격 판정 MCP 서버 개발 |
| **LG Aimers 8기** | AI 교육 과정 수료 및 Offline Hackathon 참가 · LLM / Physical AI 문제 해결 |
| **U300 학생창업 프로젝트** | 팀 내 전공자로서 LLM 및 IT 기술 이해를 바탕으로 서비스 기획·협업 경험 |

---

## 🔍 관심 분야 | Research & Engineering Interests

### Efficient AI / On-device Inference
Quantization · ONNX · Runtime Optimization · Edge Deployment

### LLM Systems & Agents
RAG · Retrieval · Grounding · MCP · Tool Use · Evaluation

### Computer Vision
Detection · Tracking · Recognition · 3D Geometry

### Optimization
CP-SAT · Metaheuristics · QUBO · QAOA · Classical-Quantum Hybrid

---

## 🛠 Tech Stack

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

### AI / Computer Vision
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white)

### Systems / Tools
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Qiskit](https://img.shields.io/badge/Qiskit-6929C4?style=flat-square)

---

## 🌱 Current Focus

현재는 아래 질문들을 중심으로 프로젝트와 학습을 이어가고 있습니다.

- 제한된 자원에서 AI 모델을 **더 작고 빠르게** 만들 수 있는가?
- LLM이 답을 생성할 때 **근거와 검증 가능성**을 어떻게 보장할 수 있는가?
- 복잡한 business constraints가 있는 문제를 **최적화 문제로 정확하게 모델링**할 수 있는가?
- 연구·실험 결과를 실제 사용 가능한 **AI system / service**로 어떻게 연결할 수 있는가?

궁극적으로는 모델 하나의 성능을 넘어,  
**문제를 정의하고 → 데이터를 구성하고 → 모델을 만들고 → 검증하고 → 배포하는 전체 과정을 이해하는 AI 엔지니어 / 연구자**를 목표로 하고 있습니다.

---

<div align="center">

**GitHub:** [@todayoneul](https://github.com/todayoneul)

</div>
