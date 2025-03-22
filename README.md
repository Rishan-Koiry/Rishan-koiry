<p align="center">
  <h1 style="font-family: 'Fira Code', monospace; color: #00ADB5;">Hey! I'm Rishan Koiry</h1>
  <p style="font-family: Arial, sans-serif; font-size: 1.5rem; color: #222831;">A Passionate Developer, Lifelong Learner, and Tech Enthusiast!</p>
</p>

---

## 🌌 **About Me**
- 🎓 **Passionate student** exploring the world of technology.
- 🌱 Currently diving deep into **Python, Web Development & AI**.
- 🚀 **Love building projects & collaborating** with developers.
- 💡 Proficient in **HTML, CSS, Python**.
- 🏆 Contributed to **Open Source Projects**.

---

## ⚡ **Tech Stack**
<p align="center">
  <img src="https://skillicons.dev/icons?i=html,css,python,github" />
</p>

---

## 📊 **GitHub Stats**
<p align="center">
  <br>
  <img src="https://github-readme-stats.vercel.app/api?username=Rishan-Koiry&show_icons=true&theme=tokyonight" width="500px">
  <br>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rishan-Koiry&layout=compact&theme=tokyonight" width="500px">
</p>

---

## 🏆 **Achievements**
- 🥇 Contributed to **Open Source** projects.
- 🌟 Successfully deployed **high-traffic applications**.
- 📚 Always **learning & improving** my skills.

---

## 🔥 **Current Focus**
- 🚀 Exploring **Microservices Architecture**.
- 📱 Advancing in **Mobile App Development**.
- 🧠 Diving into **AI & Machine Learning**.

---

## 🌟 **Fun Facts**
- 🏏 **Cricket Enthusiast**
- 🏸 **Badminton Player**
- 🎮 **Gaming Addict**
- 🎬 **Loves Movies & Series**

---

## 🐍 **GitHub Snake Animation**
<p align="center">
  <img src="https://github.com/Rishan-Koiry/Rishan-Koiry/blob/output/github-snake.svg" alt="Snake Game Animation" />
</p>

```yaml
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
