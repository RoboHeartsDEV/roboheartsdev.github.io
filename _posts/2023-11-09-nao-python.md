---
title: Python 2 on NAO
author: Emile Kroeger
date: 2023-11-09
category: NAO
layout: post
---

There are two main ways of using Python 2 on NAO:

* Inside Choregraphe boxes. This is well-covered in [the official documentation](http://doc.aldebaran.com/2-8/index_dev_guide.html)
* As standalone Python scripts. This is covered here.

# Python 2 Scripts

These Python scripts can be run either on NAO or on your computer to connect remotely to NAO (useful for quick iteration, or if you need more compute). The scripts can also be integrated in packages with extra content (webpages, dialogues) that can be installed and launched via Choregraphe, distributed via [the Aldebaran app store](https://cloud.aldebaran.com), etc.

There are two SDKs used to control:

* The historical NAOqi SDK

This was the first one, and the only one on NAOqi 1.14 and before, and deprecated since.

```Python
    import naoqi
    tts = ALProxy("ALTextToSpeech", "nao.local")
    tts.say("Hello, humans!")
```

I recommend against using it, but include it hee so you can recognize it - it's still very present in online documentation and in Choregraphe boxes.

* The newer libqi

Introduced in NAOqi 2.1, this one opens new features (cleaner handling of async, ability to subscribe to signals)

```Python
    import qi
    session = Qi.Session()
    session.connect("nao.local")
    session.service("ALTextToSpeech").say("Hello, humans!")
```

This one is recommended throughout this documentation. You can install it with `pip install qi`


# Recommended workflow

The [Robot Jumpstarter](https://github.com/aldebaran/robot-jumpstarter/) project provides some templates of projects, that include wrappers around a script so that it can be run either locally (convenient when developing) or installed on the robot as a package.

You can clone the project, then generate projects form templates, as explained in the README.

# More info

Most documentation is [the NAOqi 2.8 reference documentation](http://doc.aldebaran.com/2-8/index.html), specifically the [Developer Guide](http://doc.aldebaran.com/2-8/index_dev_guide.html) which contains tutorials and a complete API reference.

The [Aldebaran Developer Center](https://www.aldebaran.com/developer-center/index.html) has content related to application development, such as:

- The [lesson on Prosody](https://www.aldebaran.com/developer-center/lesson/Mastering-Prosody/index.html) (most other lessons are primarily for Pepper)
- The "articles" section

You can also search [the nao-robot tag on StackOverflow](https://stackoverflow.com/questions/tagged/nao-robot), and ask questions to the community over there.

The software tools (Choregraphe and Python SDK) and the SDKs can be found [on the NAO6 support website](https://www.aldebaran.com/en/support/nao-6/downloads-softwares).
