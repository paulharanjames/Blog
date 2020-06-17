<h2>{{ site.data.samplelist.docs_list_title }}</h2>
<ul>
   {% for item in site.data.samplelist.docs %}
      <li><a href="{{ item.url }}">{{ item.title }}</a></li>
   {% endfor %}
</ul>


Cloud Computing – What is it?
August 28, 2014Comments: 2
Nowadays, everyone talks about Cloud and Software as a Service (SAAS) but is often paired with inflated expectations and misunderstandings.  Many people still misunderstand ‘hosted’ solution as ‘cloud’ solution and in fact, many vendors attracted by lucrative additional revenue are claiming to be ‘Cloud’ provider whereas they actually host traditional solution in a virtual platform 🙁

In this post, I will try to explain about Cloud & its characteristics and difference between hosted and cloud environment.
