## Olá, me chamo Francisco Anacleto e estou no 2° período de Análise e Desenvolvimento de Sistemas.

Atualmente faço estágio na Secretaria Executiva de Tecnologia e Ciências de minha cidade.

<div style="display: inline_block"><br>
  <img align="center" alt="Faalb-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Faalb-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Faalb-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Faalb-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
</div>
  
  ##
 
<div> 
  <a href = "mailto:franciscoaalbuquerque30@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://linkedin.com/in/
franciscoaalbuquerque" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>

<hr>
<img alt="faalb" src="https://github-readme-stats.anuraghazra1.vercel.app/api?username=faalb&line_height=27&include_all_commits=true&show_icons=true&hide_border=true&theme=dark&count_private=true"/>
<a href="https://github.com/Daggy1234">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=faalb&theme=dark"/>
</a>
<hr>

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: faalb
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
