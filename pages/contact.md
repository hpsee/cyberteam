---
layout: wide
title: Contact
permalink: /contact/
---

<form action="https://formspree.io/{{ site.email }}" method="POST">
  <div class="form-group">
    <label for="name">Your Name</label>
    <input type="text" class="form-control" name="name" placeholder="Enter name" aria-describedby="nameHelp">
    <small id="nameHelp" class="form-text text-muted">What should we call you?</small>
  </div>
  <div class="form-group">
    <label for="email">Email address</label>
    <input type="email" class="form-control" name="_replyto" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="message">Message</label>
    <input rows="4" type="textarea" class="form-control" aria-describedby="messageHelp" placeholder="Enter message">
    <small id="messageHelp" class="form-text text-muted">How can we help you today?</small>
  </div>
  <button type="submit" class="btn btn-primary">Send</button>
</form>
