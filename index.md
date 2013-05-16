---
layout: default
title: Homepage
tagline:
---
{% include JB/setup %}

## Hello World!

Welcome.
    
    - (IBAction)changeGreeting:(id)sender {
        self.userName = self.textField.text;
        NSString *nameString = self.userName;
        if ([nameString length] == 0) {
            nameString = @"World";
        }
        NSString *greeting = [[NSString alloc] initWithFormat:@"Hello, %@!", nameString];
        self.label.text = greeting;
    }
    
## My Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

