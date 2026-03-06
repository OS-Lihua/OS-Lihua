# GitHub Profile Setup Guide

## 🚀 Implementation Checklist

### 1. Repository Secrets Configuration

Set these in GitHub Repository Settings → Secrets and variables → Actions:

| Secret | Service | How to Get | Required |
|--------|---------|-----------|----------|
| `ANTHROPIC_API_KEY` | Claude (Anthropic) | [api.anthropic.com](https://console.anthropic.com/keys) | ✅ |
| `GEMINI_API_KEY` | Gemini (Google) | [aistudio.google.com](https://aistudio.google.com/apikey) | ✅ (free tier) |
| `OPENAI_API_KEY` | GPT (OpenAI) | [platform.openai.com](https://platform.openai.com/api-keys) | ⭐ Optional |

**Steps to add secrets:**
1. Go to your repo → Settings → Secrets and variables → Actions
2. Click "New repository secret"
3. Add each key from the table above
4. Save

### 2. File Structure Verification

```
OS-Lihua/
├── README.md                           ✅
├── README.zh.md                        ✅
├── SETUP.md                            ✅
├── assets/
│   ├── dark-header.svg                ✅
│   ├── light-header.svg               ✅
│   └── github-contribution-grid-snake-dark.svg   (auto-generated)
└── .github/workflows/
    ├── update-stats.yml               ✅
    ├── ai-daily.yml                   ✅
    └── snake.yml                      ✅
```

### 3. Test Workflows

#### Manual Trigger Tests:
1. **Test Stats Update**
   - Go to Actions → "Update Skill Stats"
   - Click "Run workflow" → Run workflow
   - Wait for completion, verify README changes

2. **Test AI Daily**
   - Go to Actions → "AI Daily Oracle"
   - Click "Run workflow" → Run workflow
   - Wait for completion, verify AI content updates

3. **Test Snake Animation**
   - Go to Actions → "Generate Snake Animation"
   - Click "Run workflow" → Run workflow
   - Check `assets/github-contribution-grid-snake-dark.svg` is created

#### Automatic Triggers:
- **update-stats.yml**: Runs every Monday at 00:00 UTC
- **ai-daily.yml**: Runs every day at 08:00 UTC
- **snake.yml**: Runs every day at 00:00 UTC

### 4. Verification Checklist

- [ ] Dark header banner displays correctly in dark mode
- [ ] Light header banner displays correctly in light mode
- [ ] Language switcher links work (EN ↔ 中文)
- [ ] GitHub stats cards load
- [ ] Featured projects section displays all 4 projects
- [ ] Skill matrix populated with real commit data
- [ ] AI oracle section has content
- [ ] Snake animation generates and displays
- [ ] Social links are clickable and correct

### 5. Customization Options

#### Theme Customization
- **Dark theme colors**: Edit `assets/dark-header.svg`
  - Cyan: `#00fff2`
  - Magenta: `#ff00ff`
  - Purple: `#7000ff`

- **Light theme colors**: Edit `assets/light-header.svg`
  - Navy: `#1a1a6e`
  - Gold: `#c9a227`

#### AI Provider Configuration
Edit `.github/workflows/ai-daily.yml` to adjust:
- **Rotation schedule**: Modify `ai_rotation` dictionary (line ~75)
- **Prompts**: Customize the system prompts for each AI
- **Models**: Change model names (Claude 3.5 Sonnet, Gemini 2.0 Flash, GPT-4o-mini)

#### Schedule Times
- Edit cron expressions in workflow files to change trigger times
- Format: `HH MM DD MM DW` (see [crontab guru](https://crontab.guru) for help)

### 6. Troubleshooting

#### Skills not updating?
- Check `GITHUB_TOKEN` has proper permissions
- Verify Python script output in workflow logs
- Ensure commit history is not sparse

#### AI content not generating?
- Verify API key is correctly set in Secrets
- Check API quota limits in each service
- Review workflow logs for specific error messages

#### Snake animation missing?
- Ensure `platane/snk` action has permission to read contributions
- Check if GitHub profile is public (required for the action)

#### Theme not switching?
- Ensure SVG files are in `assets/` directory
- Verify `<picture>` tag syntax in README
- Check GitHub renders media queries for color-scheme

### 7. Optional Enhancements

1. **Add WakaTime Stats** (if you use WakaTime plugin)
   ```markdown
   [![WakaTime Stats](https://github-readme-stats.vercel.app/api/wakatime?username=0xYaCo&theme=tokyonight&hide_border=true)](https://wakatime.com/@0xYaCo)
   ```

2. **Custom Badge Color Themes**
   - Edit shield.io badges to match cyberpunk colors
   - Replace `flat-square` with `for-the-badge` for larger badges

3. **Add Visitor Counter**
   ```markdown
   ![Visitors](https://komarev.com/ghpvc/?username=OS-Lihua&style=flat-square&color=00fff2&label=VISITORS)
   ```

4. **Pin More Projects**
   - Go to your GitHub profile
   - Click "Customize your pins"
   - Select top 6 repositories to feature

### 8. Emergency Commands

**Reset workflows** (if something breaks):
```bash
git pull origin main
rm -rf .github/workflows/*.yml
# Copy workflows from this repo again
git add .
git commit -m "fix: reset workflows"
git push
```

**Manually update README**:
```bash
# Run stats update locally (requires Python)
python3 scripts/update-stats.py

# Run AI oracle locally
python3 scripts/ai-oracle.py
```

---

## 🎯 Expected Results

After successful setup, your GitHub profile will show:
- **Cyberpunk aesthetic** with animated glitch effects
- **Multi-language support** (English/Chinese toggle)
- **Dynamic skill matrix** updating weekly
- **Daily AI wisdom** rotating between Claude, Gemini, and GPT
- **Live statistics** from github-readme-stats
- **Contribution visualization** with snake animation
- **Professional project showcase** with descriptions

---

## 📚 Resources

- [GitHub Profile README](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Anthropic API Docs](https://docs.anthropic.com)
- [Google Generative AI API](https://developers.google.com/generative-ai)
- [OpenAI API Reference](https://platform.openai.com/docs/api-reference)

---

## 🤝 Support

If you encounter issues:
1. Check workflow logs in Actions tab
2. Verify all secrets are set correctly
3. Ensure Python dependencies are installed
4. Review error messages in job output

**Questions?** Check the relevant API documentation or GitHub Actions documentation.

---

Made with 💻 + ✨ | Last updated: 2025-03-06
