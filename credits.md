<!-- Template repository: https://github.com/soulraven/jinja-templates
     Template path: credits.md
-->

# Credits

These projects were used to build `{{ project_name }}`. **Thank you!**

[`python`](https://www.python.org/)

### Direct dependencies

{% for dep in direct_dependencies -%}
[`{{ dep }}`](https://pypi.org/project/{{ dep }}/){% if not loop.last %} |{% endif %}
{%- endfor %}

### Indirect dependencies

{%- if indirect_dependencies is defined %}
{% for dep in indirect_dependencies -%}
[`{{ dep }}`](https://pypi.org/project/{{ dep }}/){% if not loop.last %} |{% endif %}
{%- endfor %}
{%- endif %}
{%- if more_credits %}

**[More credits from the author]({{ more_credits }})**
{%- endif %}
