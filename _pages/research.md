---
layout: page
permalink: /research/
title: research
description: Parallel programming models, runtime systems, and research computing.
nav: true
nav_order: 1
---

My research focuses on programming models, languages, and runtime systems for
high-performance parallel computing. I am especially interested in irregular
applications, which use dynamic, unbalanced workloads or globally shared, pointer-based
data structures such as trees and graphs, on distributed-memory systems that have
no physically shared memory. Most of my current work is done with Rhodes
undergraduates.

## Network-accelerated dynamic load balancing

Work stealing is a simple and effective way to balance irregular, dynamically
generated work across a parallel machine. On distributed-memory systems, however,
every steal costs several round trips over the network. My recent work uses the
offload capabilities of modern high-performance networks to take the CPU out of
that loop. It re-purposes message matching, triggered operations, and network
atomic operations so that steals require less communication.

- **Structured atomic operations in OpenSHMEM.** [ICPP '21](https://doi.org/10.1145/3472456.3472522), with Cameron Cartier† and James Dinan. Code: [SAWS](https://github.com/brianlarkins/saws).
- **Accelerated work stealing with Portals 4.** [ICPP '19](https://doi.org/10.1145/3337821.3337878), with John Snyder† and James Dinan. Code: [PAWS](https://github.com/brianlarkins/paws).
- **Locality-aware work stealing.** Kamil Yousuf, Rhodes Undergraduate Research Symposium, 2024.

## Partitioned global logical address spaces

Partitioned global address space (PGAS) models give programmers a shared view of
distributed data, but they tie each piece of data to a physical location. A
*logical* address space lets the runtime and network hardware locate data by key,
much like a distributed hash table, which makes irregular data structures easier to
build and lets the network do more of the work.

- [COMHPC '16](https://doi.org/10.1109/COMHPC.2016.007) and [ICPP '18](https://doi.org/10.1145/3225058.3225092), with John Snyder† and James Dinan. Code: [PDHT](https://github.com/brianlarkins/pdht).

## Global-view programming of irregular data structures

My graduate work at Ohio State, advised by P. Sadayappan and in collaboration with
colleagues at Pacific Northwest National Laboratory, focused on runtime support for
global-view programming. My current work builds on it.

- **Global Trees** (my dissertation work): a framework for linked data structures on
  distributed-memory parallel systems. [SC '08](https://doi.org/10.1109/SC.2008.5218880).
  See also [ACMSE '12](https://doi.org/10.1145/2184512.2184577) on data locality for irregular PGAS programs.
- **Scioto** (with James Dinan): global-view task parallelism with scalable work stealing.
  [ICPP '08](https://doi.org/10.1109/ICPP.2008.44) and [SC '09](https://doi.org/10.1145/1654059.1654113).

At Ohio State, I also worked on *Brew*, a language and compiler with multiple
dispatch, strong code mobility, and retroactive data abstraction, and on the
*Tensor Contraction Engine*, a domain-specific compiler that generates highly tuned
Fortran for tensor contraction expressions.

## Computer science education

- **Co-designed hardware/software systems curriculum** for the liberal-arts CS major. [SIGCSE '27]({{ '/publications/' | relative_url }}).
- **FPGAs across the systems curriculum**: a common FPGA platform for teaching digital logic, computer organization, and compilers.
  [SIGCSE '13](https://doi.org/10.1145/2445196.2445316),
  [ACMSE '11](https://doi.org/10.1145/2016039.2016053),
  [ACMSE '11](https://doi.org/10.1145/2016039.2016056).
- **K–12 STEM outreach**: applying the cognitive apprenticeship framework to robotics camps, and evaluating summer camp topics for building girls' confidence in computing.
  [SIGCSE '13](https://doi.org/10.1145/2445196.2445226), CCSC-MS '18.
- **Computational science for non-majors** using MATLAB and image processing. [WTCS '10](https://doi.org/10.1016/j.procs.2010.04.100).

## Research computing at Rhodes

{% comment %}
Keep these div tags at column 0: an indented </div> after the bullet list gets
swallowed into the last list item, and the figure HTML then renders as text.
{% endcomment %}
<div class="row">
<div class="col-sm-8" markdown="1">

As principal investigator on the NSF award *CC\* Compute: A High Performance
Computing Cluster to Accelerate Research, Education and Training at Rhodes
College* (Award #2018758, $389,662), I brought high-performance computing to Rhodes.
The resulting cluster, **lotus**, is housed in Briggs Hall and supports both
high-performance and high-throughput workloads as a shared, campus-wide research
computing resource. It is also used in my parallel computing course.

- **Compute:** 44 compute nodes with 2,112 cores
- **Memory:** 11.6 TB
- **Storage:** 350 TB
- **Interconnect:** 100 Gb/s InfiniBand

</div>
<div class="col-sm-4 mt-3 mt-md-0">
  {% include figure.html path="assets/img/IMG_7578.jpeg" class="img-fluid rounded z-depth-1" alt="The lotus HPC cluster rack" zoomable=true %}
  <div class="caption">lotus</div>
</div>
</div>

Rhodes faculty and students can find access information on the department's
[computing resources](https://www.cs.rhodes.edu/resources/computing-resources.html)
page and in the [lotus HPC user guide](https://rhodescollege.atlassian.net/wiki/spaces/HPCL/overview).

I have also been the Rhodes [ACCESS](https://access-ci.org) (formerly XSEDE)
Campus Champion since 2015, and I help faculty and students obtain time on national
supercomputing resources. Between 2013 and 2020, I secured thirteen XSEDE
allocations totaling more than 2.6 million compute hours for research and
teaching at Coastal Carolina and Rhodes, plus a 2018 allocation at the DOE's
National Energy Research Scientific Computing Center (NERSC).

## Working with me

I regularly mentor undergraduate research in parallel computing, often through
summer fellowships. My student collaborators have presented at the Rhodes
Undergraduate Research Symposium and co-authored papers at international
conferences. If you are a Rhodes student interested in HPC, systems, or parallel
programming, [email me](mailto:{{ site.email }}).

### Undergraduate research collaborators

Listed oldest to newest. † marks co-authors on my publications.

- Ben Whetstone† (Coastal Carolina)
- Laura Covington† (Coastal Carolina)
- Neva Waynesboro
- Hannah Chipman†
- John Snyder†
- Cameron Cartier†
- Grace Hill
- Catherine Magee
- Emily Clifton
- Danh Le
- London Bielcke
- Kamil Yousuf
- Remy Bozung
