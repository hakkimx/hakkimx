- 👋 Hi, I’m @hakkimx
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
hakkimx/hakkimx is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
name: hakkim

on:
  workflow_dispatch:
  schedule:
    # Runs every minute
    - cron: "* * * * *"

jobs:
  update-readme:
    name: Update todoist stats
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses:hakkim/todoist-readme@master
        with:
          TODOIST_API_KEY: ${{ secrets.TODOIST_API_KEY }}
          PREMIUM: ""
