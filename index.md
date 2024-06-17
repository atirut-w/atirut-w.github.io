# Home
Hi! My name's Atirut, but you may know me by another alias, Wattana. This is my personal website where I write blogs sharing my thoughts, opinions, experiences, blah blah blah. I'm a hobbyist programmer (hence the website's name), so most of the stuff here will be pretty nerdy. I'll try to keep it varied, though. Oh, yeah, I also occasionally write tutorials, too. I hope you enjoy reading my ramblings!

## Recent Posts
For RSS feed, click <a href="{{ "/feed.xml" | absolute_url }}" download>here</a> for XML, or use this URL: `{{ "/feed.xml" | absolute_url }}`.<br>
For all posts, visit [here](/blog).

{% for post in site.posts limit: 5 %}
### {{ post.date | date: "%d/%m/%Y" }} - [{{ post.title }}]({{ post.url }})
{{ post.excerpt }}
{% endfor %}
