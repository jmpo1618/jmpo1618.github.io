---
layout: post
title: Week Thirteen
---

### What did I do this past week?
This past week, my partner and I submitted the Life project. A couple of hours before the project was due, I realized we had a memory leak, which is critical for this project since we were actually allocating memory ourselves. Luckily I was able to find the leak quickly and submit on time. (I was not deleting pointers I created through the `clone()` methods in my unit tests, my actual implementation was not flawed.) I missed class on Monday, but I understand that it was on virtual methods, continuing the topic of inheritance. On Wednesday we had guest speakers from Spiceworks who talked about their jobs, Ruby, and advice for us. And finally, this Friday, we went over abstract classes.

### What's in your way?
Currently nothing is in my way. I only have to convince myself that this Thanksgiving break means that I need to start studying soon instead of relaxing, since the last round of midterms is coming up right after it.

### What will you do next week?
Next week, as implied by the previous section, I will start studying for the last OOP midterm.

### Tip of the week:
Once again, for those interested in graphics (and more specifically, game engines), you should check out this [project](http://www.playfuljs.com/a-first-person-engine-in-265-lines/) and its [source code](https://github.com/hunterloftis/playfuljs-demos/blob/gh-pages/raycaster/index.html). It is a first-person engine written in less than 300 lines. Clearly, writing a full-fledged engine takes a lot more work, but projects like this will give you a lot of experience with the basics and encourage you to keep working since you are seeing actual results.
