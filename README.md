- name: Pull in YouTube videos
  uses: gautamkrishnar/blog-post-workflow@v1
  with:
    comment_tag_name: "YOUTUBE"
    feed_list: "https://www.youtube.com/feeds/videos.xml?channel_id=SEU_CHANNEL_ID"
    max_post_count: 6
    template: '<a href="$url"><img width="140px" src="$thumbnail"></a>'
    committer_username: "youtube-bot"
    committer_email: "youtube-bot@example.com"
