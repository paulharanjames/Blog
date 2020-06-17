{% assign doclist = site.data.samplelist.docs | sort: 'title'  %}
<ol>
{% for item in doclist %}
    <li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ol>


Cloud Computing – What is it?
August 28, 2014Comments: 2
Nowadays, everyone talks about Cloud and Software as a Service (SAAS) but is often paired with inflated expectations and misunderstandings.  Many people still misunderstand ‘hosted’ solution as ‘cloud’ solution and in fact, many vendors attracted by lucrative additional revenue are claiming to be ‘Cloud’ provider whereas they actually host traditional solution in a virtual platform 🙁

In this post, I will try to explain about Cloud & its characteristics and difference between hosted and cloud environment.
