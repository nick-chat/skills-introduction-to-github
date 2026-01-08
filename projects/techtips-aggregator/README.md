# TechTips Aggregator

Automated tech tips curation and posting bot.

## Quick Start

### 1. Setup Environment
```bash
# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Copy environment variables
cp .env.example .env
# Edit .env with your API keys
```

### 2. Get API Keys
- **Anthropic (Claude):** https://console.anthropic.com/
- **Twitter API:** https://developer.twitter.com/
- **Supabase:** https://supabase.com/

### 3. Start Claude Code Session
```bash
claude
```

Then tell Claude:
> "Read the CLAUDE.md and help me build the Twitter scraper first"

## Features
- [ ] Twitter scraping
- [ ] Reddit scraping
- [ ] HackerNews scraping
- [ ] Blog RSS scraping
- [ ] AI difficulty classification
- [ ] Automated posting
- [ ] Analytics dashboard

## Architecture
```
Sources → Scrapers → AI Processor → Queue → Publisher → Twitter
```

## Cost Estimate
- Claude API: ~$5-10/month
- Supabase: Free tier
- Twitter API: Free (Basic) or $100/month (Pro)
