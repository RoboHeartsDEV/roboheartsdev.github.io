---
layout: post
title: Guide to NAO
permalink: /guide-to-nao/
---

<div class="guide-header">
    <img src="{{ site.baseurl }}/assets/nao_logo.svg" alt="NAO Robot" class="robot-logo">
    <h1>Guide to NAO</h1>
</div>

Welcome to the NAO Programming Guide!

So, you want to program your NAO robot? There are many ways to do that!

| What do you want to do?    | How can you do that? |
|-|-|
| Simple visual programming; prototypes; animations    | Use **Choregraphe**, which can be downloaded [here](https://www.aldebaran.com/en/support/nao-6/downloads-softwares) and is well-covered by [the NAOqi 2.8 reference documentation](http://doc.aldebaran.com/2-8/index.html) |
|-|-|
| Build applications in pure Python    | You can do that either [in Python 2]({{ site.baseurl }}/nao/2023-11-09-nao-python) (works out of the box), or [in Python 3]({{ site.baseurl }}/nao/2023-11-10-nao-python3) (requires installing an extra package)|
|-|-|
| Use ROS | See  [ROS for NAO]({{ site.baseurl }}/nao/2023-11-20-nao-ros)|
|-|-|
| Add AI conversations | Integrate [robohearts.ai](https://robohearts.ai) - an LLM-based conversation solution that works with NAO robots |

## Quick Start Resources

- **Visual programming**: [Choregraphe Downloads](https://www.aldebaran.com/en/support/nao-6/downloads-softwares)
- **Documentation**: [NAOqi 2.8 Reference](http://doc.aldebaran.com/2-8/index.html)
- **Python tutorials**: See our detailed [Python 2]({{ site.baseurl }}/nao/2023-11-09-nao-python) and [Python 3]({{ site.baseurl }}/nao/2023-11-10-nao-python3) guides
- **ROS integration**: [ROS for NAO]({{ site.baseurl }}/nao/2023-11-20-nao-ros) tutorial
- **AI conversations**: [robohearts.ai](https://robohearts.ai) for intelligent dialogue capabilities

## Compatible with Pepper 2.5

Note that NAO uses NAOqi 2.8, which shares the same foundation as Pepper 2.5 systems. Many of these NAO programming examples and techniques will also work on legacy Pepper robots running NAOqi 2.5.
