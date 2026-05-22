---
name: youtube-competitive-event-report
description: Use when generating Korean competitor conference, event, or announcement reports from YouTube URLs, transcripts, video notes, or related web sources, especially when the output must be a GitHub Pages-ready HTML file with YouTube timestamp evidence and web source links.
---

# YouTube Competitive Event Report

## Purpose

Generate a Korean HTML report from a YouTube-centered source set. The report summarizes competitor conferences, events, announcements, and strategic implications while showing evidence for every major claim.

## Use This Skill When

- The user gives a YouTube URL and asks for an HTML report.
- The user asks to summarize competitor conference, event, launch, keynote, or announcement content.
- The report must show which YouTube timestamp supports each point.
- The report must show which web page supports any web-enriched fact.
- The output should be Korean, with major proper nouns preserved in English.

## Required Output Defaults

- Write the report body in Korean.
- Preserve major proper nouns in English, including company, product, event, technology, model, and framework names.
- Translate or paraphrase English source material into natural Korean.
- Generate a single static `.html` file that works locally and on GitHub Pages.
- Use the visual flow from `assets/report-template.html`.
- Include a final `Source Map` section.

## Workflow

1. Normalize the YouTube URL and extract the video ID when possible.
2. Gather available source material: title, channel, date, description, transcript, user notes, and user-provided links.
3. If transcript or timestamped notes are missing, ask the user for transcript, captions, notes, or key timestamp ranges before making detailed claims.
4. Use YouTube as the primary source.
5. Use web search only when needed to verify or enrich dates, event names, official announcements, product details, or company context.
6. Prefer official pages, company blogs, conference pages, press releases, documentation, and reputable news.
7. Build claims with explicit evidence fields before writing prose.
8. Compose the final HTML using the report sections and evidence UI rules below.

## Agent Stages

### Source Intake Agent

- Normalize YouTube URL.
- Extract video ID when possible.
- Record title, channel, date, description, transcript availability, user notes, and web links.
- Identify missing source material.

### Event Extraction Agent

- Extract competitor names, conference names, event names, dates, locations, product launches, partnerships, market claims, and roadmap signals.
- Separate confirmed facts from interpretation.
- Attach empty evidence fields first, then fill them before composing final prose.

### YouTube Summary Agent

- Summarize the video by timestamp.
- Attach a clickable timestamp link to each material claim.
- Use `https://youtu.be/VIDEO_ID?t=SECONDS` links.
- Translate English transcript content into Korean while preserving major proper nouns.

### Web Enrichment Agent

- Add web evidence only when it supports or clarifies a claim.
- Label each source as `공식 발표`, `행사 페이지`, `문서`, `뉴스`, or `확인 필요`.
- Summarize English pages in Korean.
- Mark uncertain, conflicting, or weakly sourced facts as `확인 필요`.

### Competitive Insight Agent

- Convert facts into strategic Korean analysis.
- Separate evidence-backed facts from interpretation.
- Identify threats, opportunities, trend signals, and recommended watch points.

### HTML Composer Agent

- Render the report as one HTML file.
- Use the template's class names and visual style.
- Include YouTube timestamp buttons and web source chips near the claims they support.
- Include a final `Source Map` listing all YouTube and web evidence.

## Report Sections

Use these sections unless the source material does not support them:

1. `Hero`: title, video/channel/date, thesis, four stat cards.
2. `핵심 개요`: what happened, competitors involved, why it matters, primary timestamp.
3. `주요 Conference/Event 타임라인`: event list with company, date, announcement, evidence.
4. `YouTube 구간별 요약`: timestamped video summary.
5. `Web 보강 사실`: web-enriched facts with source pages.
6. `경쟁사 인사이트`: implications, risks, opportunities, watch points.
7. `Source Map`: all timestamp and web evidence.

## Evidence Rules

Every major claim must include at least one of:

- `youtubeEvidence`: label, start seconds, optional end seconds, URL, Korean excerpt.
- `webEvidence`: title, URL, domain, source type, Korean support summary.

Confidence labels:

- `high`: directly supported by a YouTube timestamp or official web source.
- `medium`: supported by reputable secondary source or strong context.
- `needs-review`: ambiguous, incomplete, conflicting, or inferred.

## Fallbacks

- If transcript is unavailable, ask for transcript, captions, notes, or timestamp ranges.
- If web search is unavailable, use user-provided sources and state that web enrichment was not performed.
- If sources conflict, prefer official sources and explain the conflict in `Source Map`.
- If the video does not contain competitor event material, produce a concise finding and ask for more relevant input.

## References

- Read `references/report-schema.md` when composing the claim data model or Source Map.
- Read `references/example-output.md` when checking expected output shape.
- Use `assets/report-template.html` as the visual and structural template for generated reports.
