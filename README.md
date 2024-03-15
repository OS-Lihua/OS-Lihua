- 👋 Hi, I’m Lihua
- 👀 I’m interested in Cpp,Game,Server,GIS,netWork,cloud computing,Database,Web3
- 🌱 I’m currently learning Cpp,GIS,linux,netWork,Car,Web3
- 💞️ I’m looking to collaborate on Some project with Cpp
- 📫 How to reach me : e-mail 2634610614@qq.com
<!---
OS-Lihua/OS-Lihua is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<!-- 信息统计 -->
<!-- <div align="center"> <img src="https://metrics.lecoq.io/OS-Lihua?template=classic&config.timezone=Asia%2FShanghai"> </div> -->
# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: OS-Lihua
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Shanghai

<!-- Github 统计卡片 -->
<div align="center"> <img height="137px" src="https://github-readme-stats.vercel.app/api?username=OS-Lihua&hide_title=true&hide_border=true&show_icons=trueline_height=21&text_color=000&icon_color=000&bg_color=0,ea6161,ffc64d,fffc4d,52fa5a&theme=graywhite" /> </div> 

<!-- GitHub 使用语言统计 -->
<div align="center"> <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=OS-Lihua&hide_title=true&hide_border=true&layout=compact&langs_count=6&text_color=000&icon_color=fff&bg_color=0,52fa5a,4dfcff,c64dff&theme=graywhite" /> </div>
<!-- GitHub 资料奖杯 -->
<div align="center"> <img src="https://github-profile-trophy.vercel.app/?username=OS-Lihua" /> </div>


<!-- GitHub 徽章 -->
<span > 
    <img src="https://img.shields.io/badge/-cpp-E34F26?style=flat-square&logo=html5&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-go-1572B6?style=flat-square&logo=css3" /> 
    <img src="https://img.shields.io/badge/-solidity-oringe?style=flat-square&logo=javascript" /> 
</span>

<!-- GitHub 访客徽章 -->
<!-- <div align="center"> <img src="https://visitor-badge.glitch.me/badge?page_id=OS-Lihua" /> </div> -->

<!-- GitHub 活动统计图 -->
<!-- <div align="center"> <img src="https://activity-graph.herokuapp.com/graph?username=OS-Lihua&theme=xcode" /> </div> -->

<!-- GitHub 连续打卡 -->
<div align="center"> <img src="https://github-readme-streak-stats.herokuapp.com/?user=OS-Lihua" /> </div>

