# Competitor-Event-movie-clip-analysis
Analysis Youtube to make the report 

## YouTube 경쟁사 이벤트 리포트 Skill 사용 가이드

이 저장소에는 YouTube 영상을 기반으로 경쟁사의 conference, event, 발표 내용, 제품 업데이트, 파트너십, roadmap 신호를 한국어 HTML 리포트로 정리하는 Skill 파일이 포함되어 있습니다.

이 Skill은 Codex용으로 작성되었지만, ChatGPT, Gemini, Claude에서도 지침과 참고 파일을 업로드해 비슷하게 사용할 수 있습니다.

### 포함 파일

```text
skills/youtube-competitive-event-report/SKILL.md
skills/youtube-competitive-event-report/assets/report-template.html
skills/youtube-competitive-event-report/references/report-schema.md
skills/youtube-competitive-event-report/references/example-output.md
docs/youtube-competitive-event-report-install-guide.md
docs/youtube-competitive-event-report-platform-guide.md

핵심 기능YouTube URL을 주요 소스로 사용
경쟁사의 conference, event, 발표, 제품 업데이트 요약
YouTube timestamp 근거 표시
웹 검색 또는 제공한 웹 링크 출처 표시
영어 소스는 한국어로 번역 요약
주요 고유명사는 영어로 유지예: OpenAI, Google, Microsoft, Google I/O, Microsoft Build, Gemini, Copilot

GitHub Pages에 올릴 수 있는 단일 HTML 생성
PC와 모바일에 맞춘 반응형 HTML 템플릿 제공
ChatGPT에서 사용하기방법 1. Custom GPTChatGPT에서 GPTs 또는 Explore GPTs로 이동합니다.
Create를 선택합니다.
Configure 탭으로 이동합니다.
이름을 입력합니다.
text



YouTube 경쟁사 이벤트 리포트 생성기

Instructions에 아래 파일 내용을 붙여넣습니다.
text



skills/youtube-competitive-event-report/SKILL.md

Knowledge 파일로 아래 파일들을 업로드합니다.
text



skills/youtube-competitive-event-report/references/report-schema.md
skills/youtube-competitive-event-report/references/example-output.md
skills/youtube-competitive-event-report/assets/report-template.html
docs/youtube-competitive-event-report-install-guide.md

가능하면 Web search, Canvas, 파일 생성 기능을 켭니다.
저장 후 새 대화에서 사용합니다.
방법 2. ProjectChatGPT에서 New project를 만듭니다.
프로젝트 이름을 입력합니다.
text



YouTube 경쟁사 이벤트 리포트

Project instructions에 SKILL.md 내용을 붙여넣습니다.
프로젝트 파일로 report-schema.md, example-output.md, report-template.html을 업로드합니다.
프로젝트 안에서 기본 프롬프트를 사용합니다.
Gemini에서 사용하기Gemini에서는 Gems로 사용하는 방식이 가장 비슷합니다.
Gemini에서 Gem manager 또는 Gems로 이동합니다.
새 Gem을 만듭니다.
이름을 입력합니다.
text



YouTube 경쟁사 이벤트 리포트 생성기

Instructions 영역에 SKILL.md 내용을 붙여넣습니다.
파일 추가가 가능하면 아래 파일을 추가합니다.
text



report-schema.md
example-output.md
report-template.html
youtube-competitive-event-report-install-guide.md

파일 업로드가 제한되면 report-schema.md와 example-output.md 내용을 Instructions 뒤에 이어 붙이고, report-template.html은 대화 시작 시 별도 첨부합니다.
Claude에서 사용하기Claude에서는 Project를 사용하는 방식이 가장 안정적입니다.
Claude에서 새 Project를 만듭니다.
Project 이름을 입력합니다.
text



YouTube 경쟁사 이벤트 리포트

Project instructions에 SKILL.md 내용을 붙여넣습니다.
Project knowledge 또는 파일 영역에 아래 파일을 업로드합니다.
text



report-schema.md
example-output.md
report-template.html
youtube-competitive-event-report-install-guide.md

새 Project chat에서 기본 프롬프트를 사용합니다.
기본 프롬프트아래 프롬프트를 ChatGPT, Gemini, Claude에서 공통으로 사용할 수 있습니다.
text



첨부한 SKILL.md를 최상위 작업 지침으로 사용해줘.
report-schema.md의 evidence schema를 따르고, example-output.md의 출력 형식을 참고해줘.
report-template.html의 디자인 흐름을 유지해서 GitHub Pages에 올릴 수 있는 단일 HTML을 만들어줘.

작업 목표:
- YouTube 영상을 주요 소스로 사용
- 경쟁사의 conference, event, 발표, 제품 업데이트, 파트너십, roadmap 신호를 요약
- 주요 내용마다 YouTube timestamp 근거 표시
- 웹 검색 또는 제공한 웹 링크로 보강한 사실은 페이지 제목, URL, domain, source type 표시
- 본문은 한국어로 작성
- OpenAI, Google, Microsoft, Google I/O, Microsoft Build, Gemini, Copilot 같은 주요 고유명사는 영어로 유지
- 영어 소스는 한국어로 번역 또는 의역
- 불확실한 내용은 `확인 필요`로 표시
- 마지막에 Source Map 섹션을 포함

입력:
YouTube URL:
[여기에 YouTube URL 입력]

Transcript 또는 주요 timestamp 메모:
[가능하면 00:00, 04:38 같은 시간 포함해서 붙여넣기]

관련 웹 링크:
[공식 발표, 행사 페이지, 문서, 뉴스 링크를 줄 단위로 입력]

출력:
1. 먼저 부족한 소스가 있으면 질문해줘.
2. 충분하면 최종 HTML 파일 내용을 생성해줘.
3. HTML 안에는 YouTube timestamp 버튼과 웹 출처 chip을 포함해줘.

transcript가 없을 때text



YouTube URL만 먼저 줄게.
가능한 범위에서 영상 제목, 설명, 공개 정보, 웹 검색으로 리포트 초안을 만들되,
timestamp 근거가 부족한 주장은 `확인 필요`로 표시해줘.
정확한 timestamp가 필요한 부분은 내가 transcript를 추가로 제공할 수 있도록 질문해줘.

YouTube URL:
https://youtu.be/...

웹 링크를 함께 줄 때text



아래 YouTube 영상과 웹 링크를 함께 사용해줘.
YouTube를 주요 소스로 삼고, 웹 링크는 날짜, 행사명, 제품명, 공식 발표 여부를 보강하는 용도로만 사용해줘.

YouTube URL:
https://youtu.be/...

Transcript:
00:00 ...
04:38 ...

웹 링크:
- https://example.com/event
- https://example.com/press-release
- https://example.com/docs

웹 출처는 `공식 발표`, `행사 페이지`, `문서`, `뉴스`, `확인 필요` 중 하나로 라벨링해줘.

최종 HTML 요청 프롬프트text



이제 최종 결과를 단일 HTML로 작성해줘.

조건:
- report-template.html의 CSS와 구조를 따른다.
- `<html lang="ko">`를 사용한다.
- YouTube timestamp는 `https://youtu.be/VIDEO_ID?t=SECONDS` 형식으로 연결한다.
- 웹 출처는 title, URL, domain, source type을 표시한다.
- 마지막에 Source Map 섹션을 넣는다.
- 설명 문장은 한국어로 쓴다.
- 주요 고유명사는 영어로 유지한다.

주의사항YouTube transcript 자동 확보는 플랫폼과 환경에 따라 실패할 수 있습니다.
가장 안정적인 입력은 YouTube URL + timestamp 포함 transcript + 관련 웹 링크입니다.
timestamp가 없는 입력이면 정확한 영상 구간 버튼을 만들기 어렵습니다.
웹 검색 결과는 플랫폼, 플랜, 설정에 따라 다를 수 있습니다.
공식 출처와 뉴스 출처가 충돌하면 공식 출처를 우선하고 Source Map에 충돌을 표시하는 것이 좋습니다.
자세한 문서설치 및 사용 가이드
ChatGPT / Gemini / Claude 플랫폼별 사용 가이드
