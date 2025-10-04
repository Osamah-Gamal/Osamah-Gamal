<h2 align="center">Hi 👋<br>👨‍💻 I'm Osamah Gamal Mohammed Esmail<br>💻 Software Developer | Backend Engineer</h2>

###

<br clear="both">

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Osamah-Gamal&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=radical&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://streak-stats.demolab.com?user=Osamah-Gamal&locale=en&mode=daily&theme=radical&hide_border=false&border_radius=5" height="150" alt="streak graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=Osamah-Gamal&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=radical&hide_border=false" height="150" alt="languages graph"  />
</div>

###

<br clear="both">

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="30" alt="csharp logo"  />
  <img width="14" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="html5 logo"  />
  <img width="14" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="30" alt="css3 logo"  />
  <img width="14" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="python logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/javascript/F7DF1E" height="30" alt="javascript logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/flutter/02569B" height="30" alt="flutter logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/dart/0175C2" height="30" alt="dart logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/github/181717" height="30" alt="github logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/git/F05032" height="30" alt="git logo"  />
  <img width="14" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/microsoftsqlserver/microsoftsqlserver-plain.svg" height="30" alt="microsoftsqlserver logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/mysql/4479A1" height="30" alt="mysql logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/c++/00599C" height="30" alt="cplusplus logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/bootstrap/7952B3" height="30" alt="bootstrap logo"  />
  <img width="14" />
  <img src="https://cdn.simpleicons.org/php/777BB4" height="30" alt="php logo"  />
</div>

###

<img align="right" height="150" src="https://osamah-gamal.netlify.app/images/Profile/osamah2.jpeg"  />

###

<div align="center">
  <a href="https://www.linkedin.com/in/%D8%A3%D8%B3%D8%A7%D9%85%D8%A9-%D8%AC%D9%85%D8%A7%D9%84-%D9%85%D8%AD%D9%85%D8%AF-%D8%A7%D8%B3%D9%85%D8%A7%D8%B9%D9%8A%D9%84-07906326b?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg" width="42" height="30" alt="linkedin logo"  />
  </a>
  <a href="mailto:osamajamal2021@gmail.com" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/gmail/default.svg" width="42" height="30" alt="gmail logo"  />
  </a>
  <a href="https://www.facebook.com/osamh.gamal.2001" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/facebook/default.svg" width="42" height="30" alt="facebook logo"  />
  </a>
  <a href="https://www.instagram.com/osamah__gamal?igsh=YzZpcjB3ZGZpNjZ5" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/instagram/default.svg" width="42" height="30" alt="instagram logo"  />
  </a>
  <a href="https://t.me/Osamah_Gamal_2001" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/telegram/default.svg" width="42" height="30" alt="telegram logo"  />
  </a>
</div>

###

<br clear="both">

name: Generate Snake

on:
  schedule: # تشغيل أسبوعي لتحديث الأنيميشن
    - cron: "0 0 * * 1"
  workflow_dispatch: # يسمح بالتشغيل اليدوي من Actions

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Generate Snake animation
        uses: Platane/snk@v3
        with:
          github_user_name: Osamah-Gamal
          outputs: |
            dist/snake.svg

      - name: Push Snake animation to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}


###
