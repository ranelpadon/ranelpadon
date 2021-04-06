name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit (optional)
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      # See action.yml for all options
      - uses: lowlighter/metrics@latest
        with:
            # Your GitHub token
            token: ${{ secrets.METRICS_TOKEN }}
            config_order: base.header, introduction, base.activity+community, base.repositories, followup, languages, projects, activity, stargazers, stackoverflow, achievements, gists, stars
            repositories_forks: yes
            plugin_languages: yes
            plugin_stargazers: yes
            plugin_followup: yes
            plugin_stackoverflow: yes
            plugin_stackoverflow_user: 2705847 
            plugin_stackoverflow_sections: ''
            plugin_achievements: yes
            plugin_achievements_ignored: influencer, follower, maintainer, contributor, explorer, octonaut
            plugin_gists: yes
            plugin_lines: yes
            plugin_stars: yes
            plugin_stars_limit: 3
            plugin_traffic: yes
