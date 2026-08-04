<p align="center">
  <img src="https://komarev.com/ghpvc/?username=alireza2040afshari-web&label=Profile%20Views&color=0e75b6&style=flat" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=3000&pause=1000&color=3B82F6&center=true&vCenter=true&width=700&lines=Hi+there!+I'm+Alireza+Afshari;Python+Developer;Learning+Django+and+AI" />
</p>

# 👋 Hi, I'm Alireza Afshari

🎓 Chemistry Education Student at Shahid Rajaee Teacher Training University

💻 Python Developer

🌱 Currently learning **Django and Artificial Intelligence**

---

## 💻 Tech Stack

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,git,github,vscode,anaconda" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" width="48" />
</p>

---

## 📚 Libraries & Tools

- Tkinter
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

---

## 🚀 Currently Learning

- Django Framework
- Backend Development Basics
- Artificial Intelligence
- Machine Learning

---
## 🌐 Connect with Me

<table>
  <tr>
    <td align="center" width="100">
      <a href="https://github.com/alireza2040afshari-web">
        <img src="https://skillicons.dev/icons?i=github" width="48" />
      </a>
      <br>GitHub
    </td>
    <td align="center" width="100">
      <a href="mailto:alireza2040afshari@gmail.com">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/google/google-original.svg" width="48" />
      </a>
      <br>Email
    </td>
  </tr>
</table>
name: Generate Snake Game

on:
  schedule:
    - cron: "0 */6 * * *"  # هر ۶ ساعت یکبار آپدیت می‌شود
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      - name: Generate GitHub Snake
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: alireza2040afshari-web
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
      
      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
