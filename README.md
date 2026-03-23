<!-- Profile README for Lasar105ch -->

<div align="center">
<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=00D9FF&center=true&vCenter=true&width=435&lines=Hey%2C+I'm+Lasar105ch!;Developer+%26+Content+Creator;Building+Cool+Stuff+%F0%9F%9A%80" />
<br><br>
<img src="https://komarev.com/ghpvc/?username=Lasar105ch&color=00d9ff&style=flat-square" />
</div>

---

## 🎯 About Me

~~~yaml
name: Lasar105ch (LazarTeh)
role: Software Engineer & YouTuber/TikToker
location: The Internet
interests:
  - Coding random stuff
  - Creating content
  - Breaking things (then fixing them)
currently: Building ports and stupid projects
<p align="center"> <img src="https://skillicons.dev/icons?i=python,javascript,typescript,react,nodejs,docker,git,linux,vscode&theme=dark" /> </p>
<div align="center"> <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Lasar105ch&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" /> <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Lasar105ch&layout=compact&theme=tokyonight&hide_border=true" /> </div>
<p align="center"> <a href="https://www.tiktok.com/@lazartech_" target="_blank"> <img src="https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white" /> </a> <a href="https://steamcommunity.com/id/lazartech/" target="_blank"> <img src="https://img.shields.io/badge/Steam-1b2838?style=for-the-badge&logo=steam&logoColor=white" /> </a> <a href="https://xdaforums.com/m/itsnotlazar.13027601/" target="_blank"> <img src="https://img.shields.io/badge/XDA-2DAAE9?style=for-the-badge&logo=xdadevelopers&logoColor=white" /> </a> </p>
<div align="center"> <picture> <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Lasar105ch/Lasar105ch/output/github-contribution-grid-snake-dark.svg" /> <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Lasar105ch/Lasar105ch/output/github-contribution-grid-snake.svg" /> <img src="https://raw.githubusercontent.com/Lasar105ch/Lasar105ch/output/github-contribution-grid-snake.svg" /> </picture> <br><br> <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00D9FF,100:7000FF&height=100&section=footer&text=Thanks%20for%20visiting!&fontSize=20&fontColor=ffffff&animation=twinkling" /> </div> ~~~
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Generate Snake Animation
        uses: Platane/snk@v3
        with:
          github_user_name: Lasar105ch
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push to Output Branch
        uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
