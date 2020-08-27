---
layout: post
title: FreeCodeCamp Part 2
date: 2020-08-27 16:46:00
last_modified_at: 2020-08-27 17:05:00
---

Pointing an a element to "#" creates a dead link.

Other elements can be nested inside a elements to make them "clickable".

    <!-- text field  with placeholder text -->
    <input type="text" placeholder="some string">

You can nest input fields inside a `<form action="#"></form>` element to make it do stuff.

It's probably also a good idea to nest a `<button type="submit">submit button</button>` inside the form.

You can make form fields required by designating them like so: `<input type="text" required>`

Inputs like radio buttons should have `for` and `id` specifications to help with assistive technologies, and each input should have the same name so they get properly grouped together:

    <label for="button1">
    <input type="radio" id="button1" name="buttongroup">
    </label>
