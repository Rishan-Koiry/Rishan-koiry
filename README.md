<p align="center">
  <h1 style="font-family: 'Fira Code', monospace; color: #00ADB5;">Hey! I'm Rishan Koiry.</h1>
  <p style="font-family: Arial, sans-serif; font-size: 1.5rem; color: #222831;">A Passionate Developer, Lifelong Learner, and Tech Enthusiast!</p>
</p>

---

## 🌌 <span style="font-size: 2rem; color: #00ADB5;">**About Me**</span>
- 🎓 **Passionate student** exploring the world of technology.
- 🌱 Currently diving deep into **Python, Web Development & AI**.
- 🚀 **Love building projects & collaborating** with developers.
- 💡 Proficient in **HTML, CSS, Python**.
- 🏆 Contributed to **Open Source Projects**.

---

## ⚡ <span style="font-size: 2rem; color: #00ADB5;">**Tech Stack**</span>
<p align="center">
  <img src="https://skillicons.dev/icons?i=html,css,python,github" />
</p>

---

## 📊 <span style="font-size: 2rem; color: #00ADB5;">**GitHub Stats**</span>
<p align="center">
  <br>
  <img src="https://github-readme-stats.vercel.app/api?username=Rishan-Koiry&show_icons=true&theme=tokyonight" width="500px">
  <br>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rishan-Koiry&layout=compact&theme=tokyonight" width="500px">
</p>

---

## 🏆 <span style="font-size: 2rem; color: #00ADB5;">**Achievements**</span>
- 🥇 Contributed to **Open Source** projects.
- 🌟 Successfully deployed **high-traffic applications**.
- 📚 Always **learning & improving** my skills.

---

## 🔥 <span style="font-size: 2rem; color: #00ADB5;">**Current Focus**</span>
- 🚀 Exploring **Microservices Architecture**.
- 📱 Advancing in **Mobile App Development**.
- 🧠 Diving into **AI & Machine Learning**.

---

## 🌟 <span style="font-size: 2rem; color: #00ADB5;">**Fun Facts**</span>
- 🏏 **Cricket Enthusiast**
- 🏸 **Badminton Player**
- 🎮 **Gaming Addict**
- 🎬 **Loves Movies & Series**

---
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

## 📬 <span style="font-size: 2rem; color: #00ADB5;">**Get in Touch**</span>
<p align="center">
  <a href="https://www.linkedin.com/in/rishan-koiry">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:koiryrishan1@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://github.com/Rishan-Koiry">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <i>⭐️ Designed & Maintained by <a href="https://github.com/Rishan-Koiry" style="color: #00ADB5;">Rishan Koiry</a></i>
</p>
