# Gemini CLI

[![Gemini CLI CI](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml/badge.svg)](https://github.com/google-gemini/gemini-cli/actions/workflows/ci.yml)

![Gemini CLI 스크린샷](./docs/assets/gemini-screenshot.png)

이 저장소는 Gemini CLI를 포함하고 있습니다. Gemini CLI는 도구에 연결하고, 코드를 이해하며, 워크플로우를 가속화하는 명령줄 AI 워크플로우 도구입니다.

Gemini CLI로 할 수 있는 것들:

- Gemini의 1M 토큰 컨텍스트 윈도우 내외에서 대규모 코드베이스를 쿼리하고 편집할 수 있습니다.
- Gemini의 멀티모달 기능을 사용하여 PDF나 스케치에서 새로운 앱을 생성할 수 있습니다.
- 풀 리퀘스트 쿼리나 복잡한 리베이스 처리와 같은 운영 작업을 자동화할 수 있습니다.
- [Imagen, Veo 또는 Lyria를 사용한 미디어 생성](https://github.com/GoogleCloudPlatform/vertex-ai-creative-studio/tree/main/experiments/mcp-genmedia)을 포함한 새로운 기능을 연결하기 위해 도구와 MCP 서버를 사용할 수 있습니다.
- Gemini에 내장된 [Google Search](https://ai.google.dev/gemini-api/docs/grounding) 도구로 쿼리를 근거에 기반하게 할 수 있습니다.

## 빠른 시작

1. **사전 요구사항:** [Node.js 버전 18](https://nodejs.org/en/download) 이상이 설치되어 있는지 확인하세요.
2. **CLI 실행:** 터미널에서 다음 명령을 실행하세요:

   ```bash
   npx https://github.com/google-gemini/gemini-cli
   ```

   또는 다음으로 설치하세요:

   ```bash
   npm install -g @google/gemini-cli
   gemini
   ```

3. **색상 테마 선택**
4. **인증:** 프롬프트가 나타나면 개인 Google 계정으로 로그인하세요. 이를 통해 Gemini를 사용하여 분당 최대 60개의 모델 요청과 하루 최대 1,000개의 모델 요청을 할 수 있습니다.

이제 Gemini CLI를 사용할 준비가 되었습니다!

### 고급 사용 또는 증가된 한도:

특정 모델을 사용하거나 더 높은 요청 용량이 필요한 경우 API 키를 사용할 수 있습니다:

1. [Google AI Studio](https://aistudio.google.com/apikey)에서 키를 생성하세요.
2. 터미널에서 환경 변수로 설정하세요. `YOUR_API_KEY`를 생성된 키로 바꾸세요.

   ```bash
   export GEMINI_API_KEY="YOUR_API_KEY"
   ```

Google Workspace 계정을 포함한 다른 인증 방법은 [인증](./docs/cli/authentication.md) 가이드를 참조하세요.

## 예제

CLI가 실행되면 셸에서 Gemini와 상호작용을 시작할 수 있습니다.

새 디렉토리에서 프로젝트를 시작할 수 있습니다:

```sh
cd new-project/
gemini
> 제공할 FAQ.md 파일을 사용하여 질문에 답변하는 Gemini Discord 봇을 작성해주세요
```

또는 기존 프로젝트로 작업할 수 있습니다:

```sh
git clone https://github.com/google-gemini/gemini-cli
cd gemini-cli
gemini
> 어제 들어간 모든 변경사항에 대한 요약을 제공해주세요
```

### 다음 단계

- [소스에서 기여하거나 빌드하는 방법](./CONTRIBUTING.md)을 알아보세요.
- 사용 가능한 **[CLI 명령](./docs/cli/commands.md)**을 탐색하세요.
- 문제가 발생하면 **[문제 해결 가이드](./docs/troubleshooting.md)**를 검토하세요.
- 더 포괄적인 문서는 [전체 문서](./docs/index.md)를 참조하세요.
- 더 많은 영감을 위해 [인기 작업](#인기-작업)을 살펴보세요.

### 문제 해결

문제가 발생하면 [문제 해결](docs/troubleshooting.md) 가이드로 이동하세요.

## 인기 작업

### 새로운 코드베이스 탐색

기존 또는 새로 클론된 저장소로 `cd`하고 `gemini`를 실행하여 시작하세요.

```text
> 이 시스템의 아키텍처의 주요 구성 요소를 설명해주세요.
```

```text
> 어떤 보안 메커니즘이 구현되어 있나요?
```

### 기존 코드로 작업

```text
> GitHub 이슈 #123에 대한 첫 번째 초안을 구현해주세요.
```

```text
> 이 코드베이스를 Java 최신 버전으로 마이그레이션하는 데 도움을 주세요. 계획부터 시작해주세요.
```

### 워크플로우 자동화

MCP 서버를 사용하여 로컬 시스템 도구를 엔터프라이즈 협업 제품군과 통합하세요.

```text
> 지난 7일간의 git 히스토리를 기능과 팀원별로 그룹화하여 슬라이드 덱을 만들어주세요.
```

```text
> 가장 많이 상호작용한 GitHub 이슈를 보여주는 월 디스플레이용 전체 화면 웹 앱을 만들어주세요.
```

### 시스템과 상호작용

```text
> 이 디렉토리의 모든 이미지를 png로 변환하고 exif 데이터의 날짜를 사용하여 이름을 변경해주세요.
```

```text
> PDF 송장을 지출 월별로 정리해주세요.
```

### 제거

제거 지침은 [제거](docs/Uninstall.md) 가이드를 참조하세요.

## 서비스 약관 및 개인정보 보호 고지

Gemini CLI 사용에 적용되는 서비스 약관 및 개인정보 보호 고지에 대한 자세한 내용은 [서비스 약관 및 개인정보 보호 고지](./docs/tos-privacy.md)를 참조하세요.
