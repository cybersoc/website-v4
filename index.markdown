---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
title: Homepage
layout: home

heading: CyberSoc
subheading: Keep up to date with the society
header_img: /static/images/banners/DSCF3385.jpg
---

{% include section_header.html text="Upcoming Events" %}
<section class="container pt-5 p-5 text-center">
	<p class="fs-5 su-link">
		Please check <a class="inline-su-link" href="https://www.cardiffstudents.com/activities/society/22389/">our SU page</a> for a current event list whilst we work on getting things sorted here :)
	</p>
	<!--<a class="btn-link color-blue fs-5" href="{{ url_for('bpcs_main.page_event_list') }}">View All Events</a>-->
</section>

{% include section_header.html text="Cybersoc Aims To:" %}
<section class="container pt-5 p-2 p-sm-3 p-md-5 text-center">
    <div class="row g-2 g-sm-3">
        {% for card in site.data.joinus_cards %}
            {% include card.html icon=card.icon color=card.color
            title=card.title 
            description=card.description %}
        {% endfor %}
    </div>
</section>

{% include section_header.html text="Amazing companies we have worked with" %}
<section class="container-md pt-0 p-1 p-sm-3">
	<div class="row px-1 px-sm-3 px-md-5">
		{% for company in site.data.companies %}
		<div class="d-flex align-items-center justify-content-center col-6 col-sm-4 col-md-3 px-1 px-sm-2 px-md-5 py-5 companies-item
			{%  if company.name == "bipsync" %}
				bipsync-logo
			{%endif %} ">
			<img src="/static/images/logos/{{ company.image }}"
				 alt="{{ company.name }}"
				 class="img-fluid" />
		</div>
		{% endfor %}
	</div>
	<!--<a class="btn-link color-blue fs-5" href="{{ url_for('bpcs_main.page_sponsor_list') }}">View Our Sponsors</a>-->
</section>