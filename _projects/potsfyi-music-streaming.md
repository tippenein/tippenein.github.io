---
layout: project
title: Potsfyi - HTML5 music streaming
---

<a href="/imgs/_posts/potsfyi.png">
  <img src="/imgs/_posts/potsfyi-preview.png"  alt=""  height=150 width=200>
  </a>

[@graue](http://twitter.com/graue) started a music streaming app intended to
run on a personal server. Since we both had the same idea, we started tackling
bits and pieces of functionality at a time.

As far as the backend, we pipe audio through `avconv` to transcode if needed and return track/album/artist information via json endpoints to the frontend. It's currently using a simple sqlite db for storing local track information.

It's in a very earlier stage and currently uses the
[flask](http://flask.pocoo.org/) python framework along with
[backbone](http://backbonejs.org), underscore,
[handlebars](http://handlebarsjs.com) and html5 audio

[Fork the original here](http://github.com/graue/potsfyi)

