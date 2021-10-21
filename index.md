---
layout: home-layout
text-color : white
background:
    class: inverted
    image:
        url: "/assets/css/images/pillars-of-creation.webp"
        position: right
        size: 100% 100%

header:
    title: "Light feathers"
    subtitle: "Home"

banner:
    title: "Light feathers"
    subtitle: "Technical blog"
    description: A Technical blog for mobile 
                 development technologies <br />managed by <a href="https://github.com/eng-mohamedalmahdy">Mohamed Almahdy</a>
    button:
        url: "/about"
        label: "About"

---



<section>
    <header class="major">
        <h1 style="color:white">Courses</h1>
    </header>
    <div class="posts">
  {% for post in site.posts %}
     {% if post.category == "course" %}
        {% include
           post.html 
           target-url= post.url
           image-src= post.image
           image-placeholder-src=post.placeholder 
           image-alt-text=post.title
           title=post.title
           content=post.description
         %}
     {% endif %}
  {% endfor %}
  </div>
</section>



<section>
    <header class="major">
        <h1 style="color:white">Projects</h1>
    </header>
    <div class="posts">
  {% for post in site.posts %}
     {% if post.category == "project" %}
        {% include
           post.html 
           target-url= post.url
           image-src= post.image
           image-placeholder-src=post.placeholder 
           image-alt-text=post.title
           title=post.title
           content=post.description
         %}
     {% endif %}
  {% endfor %}
  </div>
</section>
