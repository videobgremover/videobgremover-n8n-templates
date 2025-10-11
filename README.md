# VideoBGRemover × n8n Templates

Official n8n workflow templates for automating video background removal and composition.

## Templates

### 01-video-composition-gdrive.json
Remove video background, composite on custom background, save to Google Drive.

**Features:**
- Background removal
- Video composition with templates postion (ai_ugc_ad, centered, etc.)
- Audio mixing from both videos
- Google Drive upload
- Status polling with retry logic

**Setup:** ~7 min | **Processing:** 3-5 min per min of video

---

## 🚀 Quick Start

You can import the workflow directly into n8n:

1. In n8n, go to **Workflows → Import from URL**
2. Paste this link:

```
https://raw.githubusercontent.com/videobgremover/videobgremover-n8n-templates/main/templates/01-video-composition-gdrive.json
```

3. Click **Import**
4. Add your API key: **Settings → Variables → `VIDEOBGREMOVER_KEY`**
5. Connect Google Drive
6. Test with sample videos

Get your API key: https://videobgremover.com/api-management

---

## Sample Assets

Use these for testing:

**Foreground (AI actor):**  
`https://videos.videobgremover.com/public-videos/assets/ai-actor.mp4`

**Background (vertical scene):**  
`https://videos.videobgremover.com/public-videos/assets/vertical_background.mp4`

---

## Docs

**API Documentation:** https://docs.videobgremover.com/  
**Support:** paul@videobgremover.com
