# Report Schema

Use this schema before composing final prose or HTML. Build structured claims first, then render them.

## Source Inventory

```json
{
  "youtube": {
    "url": "https://youtu.be/example",
    "videoId": "example",
    "title": "영상 제목",
    "channel": "채널명",
    "publishedDate": "2026-05-22",
    "descriptionAvailable": true,
    "transcriptCoverage": "full"
  },
  "userProvided": {
    "transcript": true,
    "notes": true,
    "links": ["https://example.com/event"]
  },
  "webSearch": {
    "performed": true,
    "reason": "행사 날짜와 공식 발표 확인"
  }
}
```

`transcriptCoverage` values:

- `full`: transcript or captions cover the whole video.
- `partial`: only some timestamp ranges are available.
- `metadata-only`: only title, description, or user notes are available.

## Claim

```json
{
  "claim": "OpenAI announced a new workflow feature at a developer event.",
  "koreanSummary": "OpenAI는 developer event에서 새로운 workflow 기능을 발표했다.",
  "category": "product-announcement",
  "companies": ["OpenAI"],
  "events": ["Developer Event"],
  "youtubeEvidence": [
    {
      "label": "04:38",
      "startSeconds": 278,
      "endSeconds": 342,
      "url": "https://youtu.be/example?t=278",
      "excerptKo": "발표자가 workflow 자동화 기능을 설명하는 구간이다."
    }
  ],
  "webEvidence": [
    {
      "title": "Official Event Announcement",
      "url": "https://example.com/event",
      "domain": "example.com",
      "sourceType": "공식 발표",
      "supportsKo": "행사명과 발표 제품을 확인한다."
    }
  ],
  "confidence": "high"
}
```

`category` values:

- `conference`
- `event`
- `product-announcement`
- `partnership`
- `roadmap`
- `market-signal`
- `competitive-insight`

`confidence` values:

- `high`: YouTube timestamp or official web source directly supports the claim.
- `medium`: reputable secondary source or strong context supports the claim.
- `needs-review`: source is ambiguous, incomplete, conflicting, or inferred.

## Web Source Types

- `공식 발표`: company announcement, press release, official blog.
- `행사 페이지`: event landing page, agenda page, registration page.
- `문서`: official documentation, developer docs, release notes.
- `뉴스`: reputable media or trade publication.
- `확인 필요`: weak, indirect, conflicting, or user-provided-only evidence.

## Required Report Sections

1. `Hero`
2. `핵심 개요`
3. `주요 Conference/Event 타임라인`
4. `YouTube 구간별 요약`
5. `Web 보강 사실`
6. `경쟁사 인사이트`
7. `Source Map`

## Source Map Rules

The final Source Map must include:

- Every YouTube timestamp used in the report.
- Every web source used in the report.
- Claim text or section name that each source supports.
- Confidence label.
- `확인 필요` badge for weak or incomplete evidence.

## Korean Language Rules

- Write explanations in Korean.
- Preserve company, product, event, technology, model, and framework names in English.
- Translate English source content into Korean.
- Keep official English source titles when useful, then explain relevance in Korean.
