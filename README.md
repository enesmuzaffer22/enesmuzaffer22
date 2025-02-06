# 💫 About Me:
I'm into frontend development and love working on projects in this area. Graphic design is more of a hobby for me, and I occasionally share my designs on Behance. 😊


# 🌐 Socials:
[![Behance](https://img.shields.io/badge/Behance-1769ff?logo=behance&logoColor=white)](https://behance.net/muzafferyldrm) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/enesmuzafferr) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/muzaffer-yildirim) [![Medium](https://img.shields.io/badge/Medium-12100E?logo=medium&logoColor=white)](https://medium.com/@enesmuzaffer22) 

# 💻 Tech Stack:
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![Angular.js](https://img.shields.io/badge/angular.js-%23E23237.svg?style=for-the-badge&logo=angularjs&logoColor=white) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) ![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white) ![Adobe Illustrator](https://img.shields.io/badge/adobe%20illustrator-%23FF9A00.svg?style=for-the-badge&logo=adobe%20illustrator&logoColor=white) ![Adobe Photoshop](https://img.shields.io/badge/adobe%20photoshop-%2331A8FF.svg?style=for-the-badge&logo=adobe%20photoshop&logoColor=white) ![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)

name: GitHub Snake Game

on:
  # Schedule the workflow to run daily at midnight UTC
  schedule:
    - cron: "0 0 * * *"
  # Allow manual triggering of the workflow
  workflow_dispatch:
  # Trigger the workflow on pushes to the main branch
  push:
    branches:
      - main
jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      # Step 1: Checkout the repository
      - name: Checkout Repository
        uses: actions/checkout@v3
      # Step 2: Generate the snake animations
      - name: Generate GitHub Contributions Snake Animations
        uses: Platane/snk@v3
        with:
          # GitHub username to generate the animation for
          github_user_name: ${{ github.repository_owner }}
          # Define the output files and their configurations
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
      # Step 3: Deploy the generated files to the 'output' branch
      - name: Deploy to Output Branch
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
          publish_branch: output
          # Optionally, you can set a custom commit message
          commit_message: "Update snake animation [skip ci]"

# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=enesmuzaffer22&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=enesmuzaffer22&theme=tokyonight&hide_border=true)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=enesmuzaffer22&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false&layout=compact)
![](https://visitcount.itsvg.in/api?id=enesmuzaffer22&icon=0&color=0)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
