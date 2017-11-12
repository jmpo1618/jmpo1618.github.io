---
layout: post
title: Week Eleven
category: SWE
---

### What did you do this past week?
Lectures this week switched gears from SQL to code refractoring. The latter is pretty interesting, even though it's in Java; but it would be nice to see examples with themes that are slightly more motivating. The real focus of this past week was IDB though. Although most of my team was busy until Tuesday, we were able to finish on schedule. My responsibilites were mainly managed by Flask, so my contributions were less relevant than the frontend work for this phase, and my teammates did a pretty good job with that.

### What's in your way?
Two things. The first one is GCP's App Engine. Having to use this to host our project was a huge mistake, generating more problems than solving them. Although IDB is a semester long project, its hosting requirements are really simple and don't need any sofisticated mechanisms. However, App Engine defaults to auto-scaling loading balancing, deploying multiple instances of our site, and ultimately meaning that our Python script runs a number of times that we cannot predict. Given our particular way to start our server, this creates trouble. To be specific, when we launch our servers, we rebuild our database in order to achieve idempotence between deployments, which is a logical move provided the small scale of a school project. However, given that multiple instances are trying to touch our data, a lot of undefined behavior takes place. I tried to fix this by specifying the maximum number of instances to be one, but App Engine does not allow this type of balancing. This made our deployment only possible through workarounds that should not be necessary, since they take time and effort that we would rather spend on the actual project.  
  
  
The second thing that was on my way is grading, specifically the "Quality of API" section. I understand that documenting the API is an important thing to do, but there shouldn't be incongruity between the rubric on the project specification and the one provided by a TA after grading. Namely, the project website stated two factors considered for the quality of our API, its refinement and the use of Apiary. The TA's rubric on the other hand, only considered Apiary. Threfore, an honest mistake cost our group all 5 points for that section. To be perfectly honest, the points aren't a big deal to any of us, since we are all doing well in the class, but it would be nice if rubrics were actually consistent and reflected the same criteria for both students and graders in the future. Additionally, the graders' refusal to recognize a logistical mistake even when the actual work was done is not ideal.

### What will you do next week?
Next week is one of the "break weeks" in SWE that doesn't have a project deadline. It would be nice to start working on the last phase to avoid any complications for the deadline after Thanksgiving.

### What's my experience of the class?
Besides the issues I mentioned above, I'm still enjoying the class. Lectures are not boring like those of other classes and seeing the our project running is really satisfying.

### Tip of the week:
My tip of the week was probably implied earlier: don't trust GCP. Even if your site hasn't been down yet, make sure your script doesn't contain operations that might interfere with each other if executed across multiple instances. 
