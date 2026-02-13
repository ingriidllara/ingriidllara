name: Latest YouTube Videos
on:
  schedule:
    # Roda a cada 2 horas
    - cron: '0 */2 * * *'
  workflow_dispatch:

jobs:
  update-readme-with-youtube:
    name: Update this repo's README with latest videos from YouTube
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      
      - name: Pull in YouTube videos
        uses: gautamkrishnar/blog-post-workflow@v1
        with:
          comment_tag_name: "YOUTUBE"
          feed_list: "https://www.youtube.com/feeds/videos.xml?channel_id=SEU_CHANNEL_ID"
          max_post_count: 5
          template: '- 📺 [$title]($url)'
```
