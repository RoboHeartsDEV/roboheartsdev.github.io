---
layout: post
title: Guide to Pepper
permalink: /guide-to-pepper/
---

Welcome to the Pepper Programming Guide!

So, you want to program your Pepper robot? Here are the main approaches available!

| What do you want to do?    | How can you do that? |
|-|-|
| Simple visual programming; prototypes; animations    | Use **Choregraphe**, which can be downloaded [here](https://www.aldebaran.com/en/support/pepper/downloads-softwares) and is well-covered by [the NAOqi 2.5 reference documentation](http://doc.aldebaran.com/2-5/index.html) |
|-|-|
| Build applications in pure Python    | You can develop Python applications using the NAOqi Python SDK for Pepper's operating system |
|-|-|
| Android development | Pepper runs on Android, so you can develop native Android applications using the [Pepper SDK for Android](https://developer.softbankrobotics.com/pepper-naoqi-25-documentation/pepper-sdk-android) |
|-|-|
| Web-based applications | Create tablet applications using HTML/CSS/JavaScript that run on Pepper's built-in tablet |

## Getting Started

Pepper uses NAOqi 2.5 as its operating system, which provides APIs for:
- **Motion control** - Moving Pepper's arms, head, and base
- **Speech recognition and synthesis** - Making Pepper talk and understand voice commands
- **Vision** - Using Pepper's cameras for face detection, object recognition, etc.
- **Touch sensors** - Responding to touch on Pepper's head and hands
- **Tablet interaction** - Controlling the tablet display for user interfaces

## Development Environment

To get started with Pepper development:

1. **Download Choregraphe** from the SoftBank Robotics developer portal
2. **Set up the Python SDK** for programmatic control
3. **Configure your development environment** to connect to your Pepper robot
4. **Explore the documentation** and sample projects

## Resources

- [Official Pepper Documentation](https://developer.softbankrobotics.com/pepper-naoqi-25-documentation)
- [Choregraphe User Guide](http://doc.aldebaran.com/2-5/software/choregraphe/index.html)
- [Python SDK Documentation](http://doc.aldebaran.com/2-5/dev/python/index.html)
- [Android SDK for Pepper](https://developer.softbankrobotics.com/pepper-naoqi-25-documentation/pepper-sdk-android)