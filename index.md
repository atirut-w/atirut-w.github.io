# Home
Hi! My name's Atirut, but you may know me by another alias, Wattana. This is my personal website where I write blogs sharing my thoughts, opinions, experiences, blah blah blah. I'm a hobbyist programmer (hence the website's name) and also a gamer, so most of the stuff here will be pretty nerdy. I'll try to keep it varied, though. Oh, yeah, I also occasionally write tutorials, too. I hope you enjoy reading my ramblings!

## Work and Education
I am currently studying computer science (and getting curb-stomped by math) at Kasetsart University.

## Notable Projects
- [MultiEmu](https://github.com/atirut-w/multiemu/) (on hold due to infrastructural issues)

## Skills
- C++ (intermediate)
- C# (ex-intermediate, now rusty)
- GDScript (intermediate, somewhat rusty)
- Lua (intermediate, somewhat rusty)
- Python (intermediate)
- Assembly
  - Z80 (beginner-intermediate)
  - 6502 (beginner-intermediate, but tends to avoid)

## Recent Posts

Stay updated with my latest blog posts below. For the full list of posts, visit [here](/blog).

For RSS feed, click <a href="{{ "/feed.xml" | absolute_url }}" download>here</a> for XML, or use this URL: `{{ "/feed.xml" | absolute_url }}`.<br>

{% if site.posts.size > 0 %}
  {% for post in site.posts limit: 5 %}
### {{ post.date | date: "%d %B %Y" }} - [{{ post.title }}]({{ post.url }})
{{ post.excerpt | strip_html | truncatewords: 30 }}
[Read more]({{ post.url }})
  {% endfor %}
{% else %}
  <p>No recent posts available at the moment. Please check back later.</p>
{% endif %}
