<div align="center">

<img src="assets/mark.png" width="96" alt="for nav 로고 마크" />
<br />
<img src="assets/wordmark.png" width="260" alt="for nav" />

### 아플 때, 말이 통하지 않아도 길을 잃지 않게

울산의 외국인 근로자를 위한 **다국어 의료 내비게이터**를 만드는 팀 **콘셉타민**입니다.

[![서비스 열기](https://img.shields.io/badge/서비스-www.for--nav.com-45C8C2?style=for-the-badge)](https://www.for-nav.com)
[![앱 화면](https://img.shields.io/badge/근로자_앱-app.for--nav.com-45C8C2?style=for-the-badge)](https://app.for-nav.com)
[![저장소](https://img.shields.io/badge/GitHub-for--nav-24292F?style=for-the-badge&logo=github)](https://github.com/conceptamin/for-nav)

</div>

---

## 🧭 for nav가 하는 일

증상을 **버튼으로** 고르면, 어느 진료과에 가야 하는지·어떤 제도를 쓸 수 있는지·접수할 때 무슨 말을 하면 되는지를 **모국어와 한국어로 함께** 보여 줍니다.

| 기능 | 설명 |
|---|---|
| 🌏 **20개 언어** | 네팔어·러시아어·몽골어·베트남어·싱할라어·우즈베크어·인도네시아어·필리핀어 등. 아랍어는 오른쪽에서 왼쪽으로 |
| 🩺 **진료과 안내** | 명확한 경우는 규칙, 나머지는 학습 모델 두 개의 앙상블로 상위 진료과를 고릅니다 |
| 🗣️ **접수 도우미** | 병원 창구에서 그대로 보여 줄 한국어 문장과 발음 표기 |
| 💬 **센터 상담** | 근로자가 보낸 요청이 센터 접수함에 바로 도착하고, 채팅·번역 자막 통화로 이어집니다 |
| 🚑 **119는 늘 보이게** | 응급 여부를 앱이 판정하지 않습니다. 대신 119 버튼을 모든 화면 아래에 둡니다 |

> 진단이 아니라 **안내**입니다. 질환명은 화면에 내보내지 않습니다.

## 🔀 흐름

```text
버튼으로 증상 고르기
  → 명확한 경우 규칙 (치아 → 치과, 눈 → 안과 …)
  → 진료과 앙상블 (LightGBM + 소형 MLP)
  → LLM이 리포트를 정리·번역
  → 근처 진료 가능한 의원 연결
```

## 🛠️ 만드는 도구

<p>
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/LightGBM-9ACD32?style=flat-square" alt="LightGBM" />
  <img src="https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white" alt="Claude" />
  <img src="https://img.shields.io/badge/WebRTC-333333?style=flat-square&logo=webrtc&logoColor=white" alt="WebRTC" />
</p>

| 폴더 | 내용 |
|---|---|
| [`frontend/`](https://github.com/conceptamin/for-nav/tree/main/frontend) | 근로자 화면(모바일)과 센터 화면(PC) 웹앱 |
| [`app-front/`](https://github.com/conceptamin/for-nav/tree/main/app-front) · [`app/`](https://github.com/conceptamin/for-nav/tree/main/app) | Flutter 앱 안에서 도는 근로자 화면과 앱 껍데기 |
| [`backend/`](https://github.com/conceptamin/for-nav/tree/main/backend) | FastAPI 서버 — 규칙 엔진, 센터 접수함, 상담 채팅·통화 중계 |
| [`modeling/`](https://github.com/conceptamin/for-nav/tree/main/modeling) | 진료과 모델 학습과 평가 |

## 👥 팀

<a href="https://github.com/conceptamin/for-nav/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=conceptamin/for-nav" alt="for-nav 기여자" />
</a>

<div align="center">
<sub>콘셉타민 · for nav</sub>
</div>
