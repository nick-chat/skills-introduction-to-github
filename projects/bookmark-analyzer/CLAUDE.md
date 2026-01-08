# Bookmark Analyzer - Claude Code Instructions

## Project Overview
Tool that analyzes Twitter bookmarks (videos and articles), transcribes/summarizes them, and generates ready-to-post Twitter threads showing how to do what the bookmark teaches.

## Tech Stack
- **Language:** Python 3.11+
- **Video Transcription:** OpenAI Whisper API
- **Article Extraction:** newspaper3k, trafilatura
- **AI Analysis:** Claude API (Anthropic)
- **Database:** Supabase or SQLite (local)
- **Video Download:** yt-dlp

## Project Structure
```
bookmark-analyzer/
├── src/
│   ├── fetchers/
│   │   ├── bookmark_fetcher.py    # Twitter API or browser extension
│   │   ├── video_downloader.py    # yt-dlp wrapper
│   │   └── article_fetcher.py     # Web content extraction
│   ├── processors/
│   │   ├── transcriber.py         # Whisper API integration
│   │   ├── article_parser.py      # Extract article content
│   │   └── content_analyzer.py    # Claude API analysis
│   ├── generators/
│   │   ├── thread_generator.py    # Create Twitter threads
│   │   └── hook_generator.py      # Create engaging first tweet
│   ├── database/
│   │   └── db_client.py
│   └── main.py
├── config/
│   └── prompts.yaml              # Claude API prompts
├── output/                       # Generated threads saved here
├── tests/
├── .env.example
├── requirements.txt
└── README.md
```

## Coding Standards
- Use type hints for all functions
- Async operations for API calls
- Cache transcriptions to avoid re-processing
- Store both raw and processed content

## Thread Generation Format
Generated threads should follow this structure:
1. **Hook tweet:** Attention-grabbing opener
2. **Context tweet:** What this teaches and why it matters
3. **Step tweets:** 3-7 tweets with actual how-to steps
4. **Summary tweet:** Key takeaway
5. **CTA tweet:** Call to action (follow, bookmark, etc.)

## Content Analysis Prompt Template
When analyzing content, extract:
- Main topic/skill being taught
- Prerequisites needed
- Step-by-step instructions
- Common mistakes to avoid
- Time required to implement
- Difficulty level

## Video Processing
- Download video locally (temp storage)
- Extract audio for transcription
- Delete video after processing (save space)
- Handle videos up to 30 minutes
- Skip videos longer than 30 min (flag for manual review)

## Error Handling
- Retry Whisper API 3 times on failure
- Handle deleted bookmarks gracefully
- Log processing failures with bookmark URL
- Queue failed items for retry

## Privacy & Storage
- Process locally when possible
- Don't store other users' content permanently
- Auto-delete processed videos after 24 hours
- Only store your generated threads

## Do NOT
- Process private/protected account content
- Store downloaded videos permanently
- Exceed API rate limits
- Generate threads without human review option
