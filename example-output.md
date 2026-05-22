# Example Output Shape

This example shows structure and tone. Do not copy the facts unless they match the user's source.

## Input

- YouTube URL: `https://youtu.be/example`
- Topic: competitor AI conference summary
- Transcript excerpt:
  - `00:00`: Welcome to the developer event.
  - `04:38`: OpenAI introduces a new agentic workflow feature.
  - `08:21`: The speaker explains integration with enterprise tools.
- Web source:
  - `https://example.com/event`: official event page.

## Korean Claim Example

```json
{
  "claim": "OpenAI introduced an agentic workflow feature.",
  "koreanSummary": "OpenAI는 agentic workflow(에이전트형 작업 흐름) 기능을 공개하며 enterprise tool 연동을 강조했다.",
  "category": "product-announcement",
  "companies": ["OpenAI"],
  "events": ["Developer Event"],
  "youtubeEvidence": [
    {
      "label": "04:38",
      "startSeconds": 278,
      "url": "https://youtu.be/example?t=278",
      "excerptKo": "발표자가 새 workflow 기능의 목적을 설명한다."
    }
  ],
  "webEvidence": [
    {
      "title": "Official Event Page",
      "url": "https://example.com/event",
      "domain": "example.com",
      "sourceType": "행사 페이지",
      "supportsKo": "행사명과 발표 맥락을 확인한다."
    }
  ],
  "confidence": "high"
}
```

## HTML Section Example

```html
<div class="section">
  <div class="sec-head">
    <div class="sec-num">4</div>
    <div class="sec-title">YouTube 구간별 요약</div>
  </div>
  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-meta">OpenAI | product-announcement | high</div>
      <div class="timeline-title">agentic workflow 공개</div>
      <div class="card-body">OpenAI는 agentic workflow(에이전트형 작업 흐름)를 통해 enterprise tool 연동을 강화하는 방향을 제시했다.</div>
      <div class="evidence-row">
        <a class="time-link" href="https://youtu.be/example?t=278" target="_blank" rel="noopener">04:38</a>
        <a class="source-chip" href="https://example.com/event" target="_blank" rel="noopener">행사 페이지 · example.com</a>
      </div>
    </div>
  </div>
</div>
```

## Tone Rules

- Use concise Korean business prose.
- Keep proper nouns such as `OpenAI`, `Google I/O`, `Gemini`, and `Copilot` in English.
- Translate English claims into Korean instead of leaving raw English summaries.
- Make unsupported assumptions visible with `확인 필요`.
