# Dzeny Agents Content Repository

Public repository for final video outputs from Dzeny content generation pipeline.

## Structure

```
dzeny-agents-content/
├── output/
│   ├── 2026-03-27/  (final videos from this batch)
│   ├── 2026-03-29/  (final videos from this batch)
│   └── ...
├── manifests/       (JSON metadata of what was generated)
├── references/      (source videos used for cloning)
└── README.md
```

## Usage

### Accessing Videos via CDN
```
https://raw.githubusercontent.com/dzenyai/dzeny-agents-content/main/output/2026-03-29/final.mp4
```

### WaveSpeed Integration
Videos in this repo can be used directly as input for WaveSpeed processing:
```js
const videoUrl = 'https://raw.githubusercontent.com/dzenyai/dzeny-agents-content/main/output/2026-03-29/final.mp4';
```

## Publishing Workflow

1. **Generate:** `dzeny-agents/agents/content/` creates videos
2. **Filter:** Copy only FINAL videos to this repo
3. **Commit:** Push manifests + finalized videos
4. **Distribute:** Use GitHub raw URL for CDN delivery

## API Keys & Secrets

⚠️ **This repo is PUBLIC** — never commit API keys, credentials, or config files.
All secrets are stored in the private `dzeny-agents` repository.

---

Last updated: 2026-03-29
