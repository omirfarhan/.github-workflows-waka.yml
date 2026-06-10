# .github-workflows-waka.yml

name: Waka Readme

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  update-readme:
    name: Update Readme
    runs-on: ubuntu-latest

    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
           user: omirfarhan
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Dhaka
          plugin_commits: yes
          plugin_commits_sections: all
          plugin_commits_history: 1y
          plugin_isocalendar: yes
          plugin_followup: yes
          plugin_stargazers: yes
          plugin_lines: yes
          plugin_people: yes
          plugin_reactions: yes
          plugin_achievements: yes
          plugin_traffic: yes
