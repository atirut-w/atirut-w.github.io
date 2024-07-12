# Home
Hi! My name's Atirut, but you may know me by another alias, Wattana. This is my personal website where I write blogs sharing my thoughts, opinions, experiences, blah blah blah. I'm a hobbyist programmer (hence the website's name) and also a gamer, so most of the stuff here will be pretty nerdy. I'll try to keep it varied, though. Oh, yeah, I also occasionally write tutorials, too. I hope you enjoy reading my ramblings!

## Work and Education
I am currently studying computer science (and getting curb-stomped by Calculus) at Kasetsart University, and working as an assistant at a school in Bang Lamung, Chonburi.

## Notable Projects
- [Fantacom](https://github.com/atirut-w/fantacom/) (on hold due to infrastructural issues)
- [ZDK](https://github.com/atirut-w/zdk/) (a C compiler and runtime for the Z80 processor)

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
For RSS feed, click <a href="{{ "/feed.xml" | absolute_url }}" download>here</a> for XML, or use this URL: `{{ "/feed.xml" | absolute_url }}`.<br>
For all posts, visit [here](/blog).

{% for post in site.posts limit: 5 %}
### {{ post.date | date: "%d/%m/%Y" }} - [{{ post.title }}]({{ post.url }})
{{ post.excerpt }}
{% endfor %}
