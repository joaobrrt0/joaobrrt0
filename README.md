## Hi my name is João Pedro!

- 🔭 currently working on data science
- 🌱 I’m currently learning power bi
  
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=joaobrrt0&show_icons=true&theme=radical)]

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=joaobrrt0&hide_progress=truee&theme=radical)

![Snake Animation]

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
