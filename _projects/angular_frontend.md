---
layout: project
title: Angular cluster admin interface
---

### Angular frontend for a cluster admin

<a href="imgs/_posts/angular.png">
  <img src="/imgs/_posts/angular-preview.png" alt="" height=150 width=200>
  </a>

This project was undertaken for work so I can't provide any code, but it was pretty eye-opening.
The async aspect was the main hurdle. Basically, the frontend gets async updates and must update the
state accordingly. The state determines what is shown on each page, and on select pages, what page it should route to.

For example, if an event about user registration comes in, the state will be
updated and all browsers connected to the interface will be informed. Well,
that's just async 101, whatever. Anyway, this task required some interesting
things to be done with javascript structures and angular services. I
learned a lot by working on both sides of the API. Since I had mostly been
writing RESTful APIs up until this point, it gave me a nice reminder that
someone actually has to USE the API I'm providing.
