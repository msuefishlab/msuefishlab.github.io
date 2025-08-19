---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# <i class="fas fa-envelope"></i>Contact

Our lab is part of the [Department of Integrative Biology](https://integrativebiology.natsci.msu.edu), at [Michigan State University](http://www.msu.edu).
We are located on the 1st floor of [Giltner Hall](https://maps.msu.edu/interactive/index.php?location=6NHQ).

{%
  include link.html
  type="email"
  icon=""
  text="jgallant@msu.edu"
  tooltip=""
  link="jgallant@msu.edu"
  style="button"
%}
{%
  include link.html
  type="phone"
  icon=""
  text="(517) 884-7756"
  tooltip=""
  link="+1-517-884-7756"
  style="button"
%}
{%
  include link.html
  type="address"
  icon=""
  text="Google Maps"
  tooltip="Our location on Google Maps for easy navigation"
  link="https://www.google.com/maps/place/Giltner+Hall,+293+Farm+Ln,+East+Lansing,+MI+48825/@42.7301698,-84.4786089,17z/data=!3m1!4b1!4m5!3m4!1s0x8822c281c37243e1:0x8e9ecd41ac7320c5!8m2!3d42.7301659!4d-84.4764202"
  style="button"
%}
{:.center}

{% include section.html %}

{% capture col1 %}
{%
  include figure.html
  image="images/giltner.jpg"
  caption="Giltner Hall, Farm Lane East Lansing"
%}
{% endcapture %}
{% capture col2 %}

### <i class="fas fa-mail-bulk"></i>Mailing Address

Dr. Jason Gallant  
Department of Integrative Biology  
Room 203 Natural Sciences  
288 Farm Lane  
East Lansing, MI 48824  
USA
{:.center}
{% endcapture %}
{% include two-col.html col1=col1 col2=col2 %}
