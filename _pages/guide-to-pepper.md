---
layout: post
title: Guide to Pepper
permalink: /guide-to-pepper/
---

<div class="guide-header">
    <img src="{{ site.baseurl }}/assets/pepper_logo.svg" alt="Pepper Robot" class="robot-logo">
    <h1>Guide to Pepper</h1>
</div>

So, you want to program your Pepper?

Well, how to do so strongly depends on which version of Pepper you have:

 * On the more recent **Pepper 2.9** (or "**Pepper QiSDK**" or "**Pepper Android**"), applications run on Pepper's tablet and are made with Android Studio
 * On the classic **Pepper 2.5** or (as well as Pepper 2.1), applications ("behaviors") run on Pepper's head, and are typically made with Chorégraphe or in standalone Python.

## Pepper 2.9 QiSDK (Android-based)

### Making Android Applications

On this version, applications are pure Android Applications, that run on Pepper's tablet, and control Pepper via a special library called "QiSDK". So a lot of development will be "typical" Android development, tho since Pepper's tablet is running Android 6 ("Marshmallow" - fairly old by now), you will need to be careful about which features you use.

The most useful ressources for doing this:

 * [Android Developers Platform](https://developer.android.com/develop) - where you can get Android Studio, API reference, etc.
 * The [QiSDK documentation](https://qisdk.softbankrobotics.com/sdk/doc/pepper-sdk/index.html#), which covers all the APIs, and links to examples, tho also, as of 2025 some of that might not work 100% (especially the Android Studio Plugin), which is why you should look at
 * The [MyPepperApplication example project](https://github.com/RoboHeartsDEV/MyPepperApplication), that in addition to providing a working starting point of an application that works in 2025, contains explanations on how to work in Android Studio without the Plugin.

If you want to create more advanced applications, you can look into the [SoftBank Robotics Labs](https://github.com/softbankrobotics-labs/) github repositories which has more example applications and helper libraries (such as navigation utilities, a telepresence toolkit, a collection of animations, etc.).

### Programming Pepper 2.9 directly in Python 3

As Android Development is quite complex, you may want to use Python as a simpler alternative. You have two possibilities:

 * [pepper.robothearts.dev](https://pepper.robohearts.dev) provides a browser-based development environment based on [Jupyter Notebook](https://jupyter.org/), allowing you to directly run commands on Pepper from your browser, which is very useful for quick iteration. This requires special packages not installed by default.
 * It's also possible to execute Python 3 code on Pepper's head, in which case it mostly works as for NAO (tho without Chorégraphe) - see the doc [on Python 3 for NAO]({{ site.baseurl }}/nao/2023-11-10-nao-python3) for details (will probably need some adjusting).

 Note that both of those use the "classic" NAOqi API, rather than the (more limited, but also safer) QiSDK API; the version used in Pepper 2.9 is not publicly documented but is mostly similar to [the NAOqi 2.5 API](http://doc.aldebaran.com/2-5/naoqi/index.html) (tho everything related to Choregraphe such as ALFrameManager does not exist any more; and navigation has been overhauled).

### Using a pre-made application.

If the above is too much work, you can also try [RoboHearts AI](https://www.robohearts.ai/), our application for creating your own interactions powered by LLMs and/or by QiChat.

## Pepper 2.5 (Python / Choregraphe )

Many Pepper robots still run NAOqi 2.5 (especially in academia). For these systems, the **[Official NAOqi 2.5 Documentation](http://doc.aldebaran.com/2-5/index.html) is still the best reference.

There are two main approaches for making applications:

| What do you want to do?    | How can you do that? |
|-|-|
| Visual programming; prototypes; animations | Use **Choregraphe**, downloadable [here](https://aldebaran.com/en/support/kb/softwares/downloads-softwares/pepper-2-5-downloads/) with [NAOqi 2.5 documentation](http://doc.aldebaran.com/2-5/index.html) |
|-|-|
| Python development | Most [NAO Python examples]({{ site.baseurl }}/guide-to-nao/) work on Pepper 2.5 since they share the same NAOqi foundation; A good starting point is [Robot Jumstarter](https://github.com/aldebaran/robot-jumpstarter) that has templtes for Pepper that include tablet examples. |
|-|-|

