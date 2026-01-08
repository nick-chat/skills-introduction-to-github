# Bookmark Analyzer

Turn your Twitter bookmarks into ready-to-post educational threads.

## Quick Start

### 1. Setup Environment
```bash
# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Install ffmpeg (required for audio extraction)
brew install ffmpeg

# Copy environment variables
cp .env.example .env
# Edit .env with your API keys
```

### 2. Get API Keys
- **Anthropic (Claude):** https://console.anthropic.com/
- **OpenAI (Whisper):** https://platform.openai.com/
- **Twitter API:** https://developer.twitter.com/ (for bookmarks access)

### 3. Start Claude Code Session
```bash
claude
```

Then tell Claude:
> "Read the CLAUDE.md and help me build the article fetcher first - I want to analyze bookmarked articles before we tackle videos"

## Features
- [ ] Fetch Twitter bookmarks
- [ ] Download and transcribe videos (Whisper)
- [ ] Extract article content
- [ ] AI-powered content analysis
- [ ] Thread generation
- [ ] Draft review interface
- [ ] One-click posting

## How It Works
```
Bookmark → Fetch Content → Transcribe/Parse → Analyze → Generate Thread → Review → Post
```

## Example Output

**Input:** Bookmark of a video explaining "How to use Claude Code effectively"

**Output Thread:**
```
1/ Most people waste hours with AI coding assistants.

Here's the 5-step framework that 10x'd my productivity with Claude Code:

🧵

2/ Step 1: Always start in Plan Mode

Press Shift+Tab twice. Tell Claude what you want.
Review the plan BEFORE any code is written.

This prevents wasted time on wrong approaches.

3/ Step 2: Give Claude verification tools
...
```

## Cost Estimate
- Claude API: ~$5-10/month
- Whisper API: ~$0.006/minute of audio
- Twitter API: Free (Basic)
