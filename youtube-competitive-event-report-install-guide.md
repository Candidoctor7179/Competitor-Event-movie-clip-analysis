# YouTube 경쟁사 이벤트 리포트 Skill 설치 및 사용 가이드

이 문서는 `youtube-competitive-event-report` Skill을 처음 설치하고 사용하는 사람을 위한 안내서입니다.

## 이 Skill이 하는 일

YouTube 주소, transcript, 관련 웹 링크를 바탕으로 경쟁사의 conference, event, 발표 내용, 전략적 시사점을 한국어 HTML 리포트로 만들어 줍니다.

리포트에는 다음이 포함됩니다.

- YouTube 영상의 어느 구간이 근거인지 보여주는 timestamp 버튼.
- 웹 검색 또는 사용자가 제공한 웹 페이지 출처.
- 영어 소스를 한국어로 번역 요약한 내용.
- `OpenAI`, `Google I/O`, `Microsoft Build`, `Gemini` 같은 주요 고유명사의 영어 표기.
- GitHub Pages에 바로 올릴 수 있는 단일 HTML 파일.

## 설치 위치

이 저장소 안의 Skill 폴더는 다음 위치에 있습니다.

```text
skills/youtube-competitive-event-report/
```

Codex가 자동으로 찾게 하려면 이 폴더를 개인 Skill 폴더로 복사합니다.

```bash
mkdir -p ~/.codex/skills
cp -R skills/youtube-competitive-event-report ~/.codex/skills/
```

복사 후 위치는 다음과 같아야 합니다.

```text
~/.codex/skills/youtube-competitive-event-report/SKILL.md
```

## 설치 확인

Codex를 다시 시작한 뒤 다음처럼 요청합니다.

```text
youtube-competitive-event-report Skill을 사용해서 이 YouTube 영상으로 경쟁사 이벤트 리포트 HTML을 만들어줘: https://youtu.be/example
```

Codex가 Skill을 사용한다고 말하고, transcript나 추가 소스가 필요한지 확인하면 정상입니다.

## 사용 예시

### 1. YouTube URL만 있는 경우

```text
이 YouTube 주소를 기반으로 경쟁사 conference/event 리포트 HTML을 만들어줘.
https://youtu.be/example
```

영상 transcript를 가져올 수 없으면 Codex가 transcript 또는 주요 timestamp 메모를 요청할 수 있습니다.

### 2. YouTube URL과 transcript가 있는 경우

```text
youtube-competitive-event-report Skill을 사용해줘.
YouTube URL: https://youtu.be/example

Transcript:
00:00 ...
04:38 OpenAI introduces ...
08:21 ...
```

이 방식이 가장 안정적입니다. timestamp가 포함되어 있으면 리포트의 근거 버튼도 더 정확해집니다.

### 3. YouTube URL과 관련 웹 링크가 있는 경우

```text
이 영상과 아래 웹 링크들을 함께 사용해서 경쟁사 이벤트 리포트 HTML을 만들어줘.

YouTube: https://youtu.be/example
Web:
- https://example.com/event
- https://example.com/press-release
```

Codex는 웹 링크를 보강 근거로 사용하고, 리포트에 출처 chip으로 표시합니다.

## 생성된 HTML 확인

Codex가 만든 `.html` 파일을 브라우저에서 열면 됩니다. 파일을 더블클릭하거나, 터미널에서 파일 경로를 확인한 뒤 브라우저로 엽니다.

## GitHub Pages에 올리는 방법

1. GitHub 저장소에 `news/` 또는 원하는 폴더를 만듭니다.
2. 생성된 HTML 파일을 그 폴더에 넣습니다.
3. 저장소 Settings에서 Pages를 활성화합니다.
4. 배포된 주소를 열어 HTML 페이지가 보이는지 확인합니다.

예시 경로:

```text
news/2026-05-22-competitor-event-report.html
```

## 자주 막히는 상황

### transcript를 사용할 수 없음

YouTube transcript 접근은 환경에 따라 실패할 수 있습니다. 이 경우 YouTube 자막, 직접 작성한 요약, 또는 주요 timestamp 메모를 붙여넣으면 됩니다.

### 웹 검색을 사용할 수 없음

웹 검색이 막혀 있으면 공식 페이지나 관련 기사 URL을 직접 제공하세요. Codex는 사용자가 제공한 웹 페이지를 근거로 사용할 수 있습니다.

### 출력에 timestamp가 부족함

입력 transcript에 시간이 없으면 정확한 timestamp 버튼을 만들기 어렵습니다. `04:38`, `08:21`처럼 시간 정보를 포함해 주세요.

### Skill이 감지되지 않음

다음을 확인하세요.

- `~/.codex/skills/youtube-competitive-event-report/SKILL.md` 파일이 있는지 확인.
- Codex를 재시작했는지 확인.
- 요청 문장에 `YouTube`, `경쟁사 event`, `HTML 리포트`, `timestamp` 같은 단어를 포함.
