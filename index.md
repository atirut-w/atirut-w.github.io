# Home
Hi! Welcome to my blog site thingy! I assume you've read my GitHub profile? Most of the information is there, but to recap: I'm Atirut, you may otherwise know me as Wattana. I'm interested in lots of nerdy topics, yada yada yada. This is where I ramble on and on.

## Recent Posts

Stay updated with my latest blog posts below. For the full list of posts, visit [here](/blog).

For RSS feed, click <a href="{{ "/feed.xml" | absolute_url }}" download>here</a> for XML, or use this URL: `{{ "/feed.xml" | absolute_url }}`.<br>

{% if site.posts.size > 0 %}
  {% for post in site.posts limit: 5 %}
<!-- DO NOT indent the line below, or the first and last tag from the included file breaks! -->
{% include post-entry.html post=post %}
  {% endfor %}
{% else %}
  <p>No recent posts available at the moment. Please check back later.</p>
{% endif %}
