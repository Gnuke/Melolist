# 🎵 Melolist

### 🧑‍💻 개발자 소개

신입 개발자 정진욱입니다.

-------

### 💡 프로젝트 소개

Melolist는 다양한 음성 입력 방식을 통해 간편하게 음악 정보를 검색하는 프로젝트입니다.

**Background:**

초기 개발 단계에서는 **AcrCloud API**를 이용한 **Fingerprint 기반 음악 검색** 기능을 먼저 구현하였습니다.  
이후 사용자가 직접 노래를 부르거나 흥얼거리는 방식으로 음악을 찾을 수 있도록 **Humming 기반 검색 기능**을 추가하였습니다.

Humming으로 검색 시 Houndify API를 사용하려 했으나 예상보다 어려움이 많아, **AcrCloud의 두 개의 프로젝트**를 활용하여 Fingerprint 검색과 Humming 검색을 분리하는 방식으로 개발을 진행하였습니다.

-------

### ⏱️ 개발 기간

<details>
  <summary>🗓️ 개발 기간 (상세)</summary>
  <p>
  
#### 🗓️ 2025년 01월 26일 (개발 시작)
- 원격 저장소 연결
- Local Vue 프로젝트 생성
- 환경설정 & 테스트

#### 🗓️ 01월 27일
- `front` 브랜치 생성
- `.gitignore` 추가
- Git 전략 정리
- 가용 API 조사

#### 📆 01월 28일 ~ 02월 03일
- 설 연휴

#### 📆 02월 04일 ~ 09일
- 개인사정

#### 🗓️ 02월 10일
- 녹음 UI 구현

#### 🗓️ 02월 11일
- 디렉토리 구조 리팩토링
- Git 브랜치 병합 후 재생성

#### 📆 02월 12일
- **Back-end**
  - Node.js 서버 구축
  - 음악 검색 요청 API 구현 (ACRCloud API 사용)
- **Front-end**
  - 검색 결과 목록 출력 UI 구현 (ACRCloud 데이터 사용)

#### 📆 02월 13일 ~ 03월 05일
  - **면접 및 취업 준비로 개발 중단**

#### 🗓️ 03월 06일
- **Back-end**
  - AcrCloud API를 이용한 Humming 기반 검색 기능 추가
  - 기존 Fingerprint 기반 검색과 Humming 검색을 분리
- **Front-end**
  - 검색 결과 데이터 시각화 개선
 
#### 🗓️ 03월 07일
- **Back-end**
  - 검색결과 확인을 위한 Youtube Metadata 요청 구현
- **Front-end**
  - 사용자 UI 개선
  </p>
</details>

-------

### 🖥 개발환경

| 항목             | 내용                        |
|-----------------|---------------------------|
| **OS**          | Windows 10 |
| **IDE**         | IntelliJ IDEA         |
| **패키지 매니저** | npm (v10.9.2)                       |
| **빌드 도구**    | Vite (v6.0.5)                      |
| **실행 환경**    | Node.js (v22.13.1)        |

-------

### 🛠️ 기술 스택

| 항목       | 기술/라이브러리   | 버전      | 설명                                                |
|----------|---------------|---------|---------------------------------------------------|
| **Frontend** | Vue.js        | v3.5.13 | 사용자 인터페이스 및 웹 애플리케이션 구축                           |
|          | Wavesurfer.js | v7.9.0  | 오디오 시각화 및 조작                                      |
| **Backend**  | Express.js    | v4.21.2 | Node.js 기반 웹 애플리케이션 프레임워크                         |
|          | Axios         | v1.7.9  | HTTP 요청 라이브러리                                     |
|          | CORS          | v2.8.5  | Cross-Origin Resource Sharing 활성화                 |
|          | form-data     | v4.0.1  | `multipart/form-data` 형식으로 녹음된 데이터를 전송하기 위한 라이브러리 |
|          | AcrCloud API   | v1      | 실제 음악 녹음 검색 기능 및 허밍 검색 기능 제공                      |
| **Dev Tools**| Nodemon       | v3.1.9  | 파일 변경 감지 시 서버 자동 재시작                              |
|          | dotenv        | v16.3.1 | 환경 변수 관리                                          |

-------

### ✨ 주요기능

- 🎧 **Fingerprint 기반 음악 검색** (AcrCloud API)
  - 실제 음악을 녹음하여 검색하는 기능
- 🎤 **Humming 기반 멜로디 검색** (AcrCloud API)
  - 사용자가 직접 노래를 부르거나 흥얼거려 음악을 찾는 기능
- 🦻 **검색 데이터 기반 Youtube 링크 제공** (AcrCloud Metadata API)
  - 응답 받은 데이터를 쿼리로 이용, 메타데이터 요청을 통해 Youtube 링크 제공
- ➕ 추가 예정

--------

### 🔧 개발 도구
**패키지 관리** : npm-check

--------

### ⚙️ 설치 방법

1.  Node.js 및 npm (또는 yarn) 설치

2.  프로젝트 디렉토리로 이동

3.  의존성 설치

```bash
npm install
# 또는
yarn install
```
--------

### 🌱 git 전략

1. 로컬 dev에서 작업 후 origin/dev로 푸시
  
2. GitHub에서 PR을 통해 main에 병합
  
3. 로컬 main을 git pull origin main으로 최신화

4. 필요하면 dev도 main 기준으로 업데이트 (merge or rebase)
