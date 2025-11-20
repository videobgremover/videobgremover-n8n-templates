# VideoBGRemover × n8n Templates

Official n8n workflow templates for automating video background removal and composition.

## Templates

### 01-video-composition-gdrive.json
Remove video background, composite on custom background, save to Google Drive.

**Features:**
- Background removal
- Video composition with templates (ai_ugc_ad, centered, etc.)
- Audio mixing from both videos
- Google Drive upload
- Status polling with retry logic

**Setup:** ~7 min | **Processing:** 3-5 min per min of video

---

### 02-ugc-screenrecord-video.json
AI-powered UGC ad generator: App screen recording → Gemini analysis → Sora 2 AI actor → VBR composition.

**Features:**
- Gemini AI analyzes screen recording & generates ad structure
- Sora 2 creates AI actor delivering UGC-style ad
- Background removal on AI actor
- Composites actor over screen recording (ai_ugc_ad template)
- Audio mixing (30% background + 100% actor)
- Google Drive upload

**Perfect for:**
- App developers creating UGC-style ads
- SaaS product marketing
- Mobile app feature announcements
- Digital product launches

**Setup:** ~10 min (3 API keys) | **Processing:** 5-8 min total

---

### 03-image-composition-gdrive.json
Remove video background, composite on static image background, save to Google Drive.

**Features:**
- Background removal from any video
- Image composition with centered template
- Static image backgrounds (JPG, PNG, WebP)
- Google Drive upload
- Status polling with retry logic

**Perfect for:**
- Profile/presentation videos with professional backgrounds
- AI avatars (HeyGen, D-ID) on static scenes
- Social media content with custom branded backgrounds
- Product demos with consistent brand imagery

**Setup:** ~7 min | **Processing:** 3-5 min per min of video

---

### 04-ai-background-generation.json
Generate custom backgrounds with AI from text prompts, remove video background, composite, and save to Google Drive.

**Features:**
- AI background generation from text (Gemini Nano Banana)
- Automatic background removal from video
- Image composition with centered template
- Multiple aspect ratio support (1:1, 16:9, 9:16, 4:3, 21:9)
- Google Drive upload (image + video)
- Status polling with retry logic

**Perfect for:**
- Custom scenes from imagination (no stock images needed)
- Marketing videos with tailored AI-generated environments
- Product demos with unique, brand-specific backgrounds
- Social media content with creative AI-generated visuals

**Setup:** ~5 min (2 API keys) | **Processing:** 2-4 min per video

---

### 05-change-video-background-ai.json
AI-powered background change using Wan 2.2 VACE: Remove background → AI generates new background from text prompt. (Does not work very well)

**Features:**
- Background removal with VideoBGRemover (extracts mask)
- AI background generation with FAL Wan 2.2 VACE inpainting
- Text-prompt based background creation
- Temporal consistency across frames
- Seamless video inpainting
- Google Drive upload

**Perfect for:**
- Creative video transformations without stock footage
- Product demos with imaginative AI-generated backgrounds
- Social media content with unique, custom scenes

**Example prompts:**
- "A futuristic cyberpunk city at night"
- "A peaceful beach at sunset"
- "Inside a modern minimalist studio"
- "A magical forest with glowing trees"

**Setup:** ~10 min (2 API keys) | **Processing:** 7-10 min total

---

### 06-veo3-mobile-lottie-animation.json
Generate mobile animations with Veo 3, remove background, export as Lottie JSON for iOS/Android apps.

**Features:**
- Google Veo 3 AI animation generation (4-8 seconds)
- 1:1 square aspect ratio (mobile-optimized)
- Background removal with VideoBGRemover
- Lottie JSON export with full transparency
- Audio disabled (saves 50% credits)
- Tiny file size (30-150KB)
- Google Drive upload
- Status polling with retry logic

**Perfect for:**
- Mobile app animations (like Duolingo)
- Loading screens and onboarding flows
- UI micro-interactions and transitions
- Character animations for iOS/Android
- Tutorial and walkthrough animations
- App Store preview assets

**Output format:**
- `.json` file (Lottie format)
- Compatible with lottie-ios, lottie-android, lottie-react-native
- Full alpha channel transparency via WebP
- Vector-scalable, hardware-accelerated

**Setup:** ~7 min (2 API keys) | **Processing:** 5-8 min per animation

---

## 🚀 Quick Start

### Template 01: Video Composition

1. In n8n, go to **Workflows → Import from URL**
2. Paste: `https://raw.githubusercontent.com/videobgremover/videobgremover-n8n-templates/main/templates/01-video-composition-gdrive.json`
3. Click **Import**
4. Add API key: **Settings → Variables → `VIDEOBGREMOVER_KEY`**
5. Connect Google Drive
6. Test with sample videos

### Template 02: AI UGC Ad Generator

1. In n8n, go to **Workflows → Import from URL**
2. Paste: `https://raw.githubusercontent.com/videobgremover/videobgremover-n8n-templates/main/templates/02-ugc-screenrecord-video.json`
3. Click **Import**
4. Add API keys: **Settings → Variables**
   - `GEMINI_KEY` → Get from https://aistudio.google.com/apikey
   - `FAL_KEY` → Get from https://fal.ai/dashboard/keys
   - `VIDEOBGREMOVER_KEY` → Get from https://videobgremover.com/api-management
5. Connect Google Drive
6. Test with sample screen recording

### Template 03: Image Composition

1. In n8n, go to **Workflows → Import from URL**
2. Paste: `https://raw.githubusercontent.com/videobgremover/videobgremover-n8n-templates/main/templates/03-image-composition-gdrive.json`
3. Click **Import**
4. Add API key: **Settings → Variables → `VIDEOBGREMOVER_KEY`**
5. Connect Google Drive
6. Test with sample video + image

### Template 04: AI Background Generation

1. In n8n, go to **Workflows → Import from URL**
2. Paste: `https://raw.githubusercontent.com/videobgremover/videobgremover-n8n-templates/main/templates/04-ai-background-generation.json`
3. Click **Import**
4. Add API keys: **Settings → Variables**
   - `GEMINI_KEY` → Get from https://aistudio.google.com/apikey
   - `VIDEOBGREMOVER_KEY` → Get from https://videobgremover.com/api-management
5. Connect Google Drive
6. Test with sample video + text prompt

### Template 05: AI Background Change (VACE Inpainting)

1. In n8n, go to **Workflows → Import from URL**
2. Paste: `https://raw.githubusercontent.com/videobgremover/videobgremover-n8n-templates/main/templates/05-change-video-background-ai.json`
3. Click **Import**
4. Add API keys: **Settings → Variables**
   - `VIDEOBGREMOVER_KEY` → Get from https://videobgremover.com/api-management
   - `FAL_KEY` → Get from https://fal.ai/dashboard/keys
5. Connect Google Drive
6. Test with sample video + background prompt

### Template 06: Mobile Animation (Veo 3 + Lottie)

1. In n8n, go to **Workflows → Import from URL**
2. Paste: `https://raw.githubusercontent.com/videobgremover/videobgremover-n8n-templates/main/templates/06-veo3-mobile-lottie-animation.json`
3. Click **Import**
4. Add API keys: **Settings → Variables**
   - `FAL_KEY` → Get from https://fal.ai/dashboard/keys
   - `VIDEOBGREMOVER_KEY` → Get from https://videobgremover.com/api-management
5. Connect Google Drive
6. Test with sample prompt (e.g., "Cute owl celebrating with confetti")
7. Download `.json` file and use in your mobile app with Lottie library

Get your VideoBGRemover API key: https://videobgremover.com/api-management

---

## Sample Assets

Use these for testing:

**Foreground (AI actor):**
`https://videos.videobgremover.com/public-videos/assets/ai-actor.mp4`

**Background (vertical scene - video):**
`https://videos.videobgremover.com/public-videos/assets/vertical_background.mp4`

**Background (image):**
`https://drive.google.com/uc?id=1DYJxUcuN5n4BT4YZnRKYmXuLNSCs5bPy`

---

## Docs

**API Documentation:** https://docs.videobgremover.com/  
**Support:** paul@videobgremover.com
