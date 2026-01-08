# TechTips Aggregator - Claude Code Instructions

## Project Overview
Automated social media bot that scrapes tech tips from Twitter, Reddit, HackerNews, and tech blogs, then uses AI to summarize and post them with difficulty levels.

## Tech Stack
- **Language:** Python 3.11+
- **Scraping:** twscrape, PRAW, BeautifulSoup, feedparser
- **AI:** Claude API (Anthropic)
- **Database:** Supabase (PostgreSQL)
- **Scheduling:** APScheduler or cron
- **Posting:** Tweepy (Twitter API)

## Project Structure
```
techtips-aggregator/
├── src/
│   ├── scrapers/
│   │   ├── twitter_scraper.py
│   │   ├── reddit_scraper.py
│   │   ├── hackernews_scraper.py
│   │   └── blog_scraper.py
│   ├── processors/
│   │   ├── content_analyzer.py    # Claude API integration
│   │   └── difficulty_classifier.py
│   ├── publishers/
│   │   └── twitter_publisher.py
│   ├── database/
│   │   └── supabase_client.py
│   └── main.py
├── config/
│   ├── sources.yaml              # List of sources to scrape
│   └── prompts.yaml              # Claude API prompts
├── tests/
├── .env.example
├── requirements.txt
└── README.md
```

## Coding Standards
- Use type hints for all functions
- Write docstrings for public functions
- Handle rate limits gracefully with exponential backoff
- Log all scraping and posting activity
- Never commit API keys (use .env)

## Key Behaviors
- When scraping, always respect robots.txt and rate limits
- Store raw content before processing (for debugging)
- Tag all content with source and timestamp
- Use async where possible for better performance

## Difficulty Classification Prompt
When classifying difficulty, use these criteria:
- **Beginner:** No coding required, GUI-based, everyday user tips
- **Intermediate:** Basic coding/CLI, some technical knowledge needed
- **Advanced:** Deep technical knowledge, complex setup, developer-focused

## Error Handling
- Retry failed API calls 3 times with exponential backoff
- Log errors to file, not just console
- Send notification if scraper fails for >1 hour
- Gracefully handle deleted/private content

## Testing Requirements
- Unit tests for each scraper
- Integration test for full pipeline
- Mock external APIs in tests

## Do NOT
- Scrape private accounts or protected tweets
- Post more than 10 tweets per hour (rate limit safety)
- Store user personal data beyond public posts
- Ignore Twitter's Terms of Service
