---
layout: page
permalink: /repositories/
title: code
description: Research software from my group. Most of it was written with undergraduate collaborators at Rhodes College.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

- **[SAWS](https://github.com/brianlarkins/saws)**: OpenSHMEM-accelerated work stealing, which uses structured atomic operations to reduce the communication cost of distributed dynamic load balancing. ([ICPP '21](https://doi.org/10.1145/3472456.3472522))
- **[PAWS](https://github.com/brianlarkins/paws)**: Portals-accelerated work stealing, which uses Portals 4 network offload capabilities to accelerate distributed work stealing. ([ICPP '19](https://doi.org/10.1145/3337821.3337878))
- **[PDHT](https://github.com/brianlarkins/pdht)**: a parallel distributed key/value store built directly on Portals 4. It provides PGAS-style semantics for a partitioned global *logical* address space suitable for network hardware offload. ([COMHPC '16](https://doi.org/10.1109/COMHPC.2016.007), [ICPP '18](https://doi.org/10.1145/3225058.3225092))
