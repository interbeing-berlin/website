---
layout: page
title: Email list
permalink: /email-list/
---

Sign up to receive updates about church of interbeing events and gatherings! We will handle your email with care ❤️

<form
  action="https://{{ site.mailchimp_region }}.list-manage.com/subscribe/post?u={{ site.mailchimp_u }}&amp;id={{ site.mailchimp_id }}"
  method="post"
  class="email-signup"
  target="_blank"
  novalidate>

  <input type="text" name="FNAME" placeholder="First name (optional)">
  <input type="text" name="LNAME" placeholder="Last name (optional)">
  <input type="email" name="EMAIL" placeholder="Your email" required>

  <!-- honeypot field -->
  <div style="position: absolute; left: -5000px;" aria-hidden="true">
    <input type="text" name="b_{{ site.mailchimp_u }}_{{ site.mailchimp_id }}" tabindex="-1" value="">
  </div>

  <button type="submit">Subscribe</button>
</form>
