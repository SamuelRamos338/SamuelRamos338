##Oii! Eu sou Samuel Ramos

- 🔭 Hoje trabalho com: front-end
- 🌱 Estudando: NodeJs
- 😄 Pronomes: ele/dele
[![SamuelRamos338 GitHub stats](https://github-readme-stats.vercel.app/api?username=SamuelRamos338)](https://github.com/anuraghazra/github-readme-stats)


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
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
