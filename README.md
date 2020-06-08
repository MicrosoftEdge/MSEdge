# Microsoft Edge and Chromium Open Source: Our Intent
Authors: Microsoft Edge Team  
Last Updated: 2018-12-06

## Why this document 
For the past few years, Microsoft has meaningfully increased participation in the open source software (OSS) community, becoming one of the world’s largest supporters of OSS projects. We are starting down a path to adopt Chromium open source in the development of Microsoft Edge on the desktop, becoming a larger contributor and user of its open source so that we can create better web compatibility for our customers and less fragmentation of the web for all web developers. 

**This document exists to clarify our thinking on how that work will proceed**: we want to explain our plans and intentions related to Microsoft Edge and the Chromium open-source project. The audiences we think will find this document most relevant and useful are (a) the people working on Chromium as approvers/maintainers and leading that project (b) the companies and engineers who build other browsers and will be interested in the contributions we plan to make, and (c) the broader community of web developers, corporate-IT managers and partners we work with on Windows and Microsoft Edge. And of course, we and all those audiences care primarily about the end-user, who is ultimately the audience this work is intended to benefit.

### TL;DR
Working with open source is not new for Microsoft Edge.  Our new mobile browser has been based on open source from its beginnings over a year ago. We’ve also used open source for various features of Microsoft Edge on the desktop (e.g. ANGLE, Web Audio, Brotli) and we’ve begun making contributions to the Chromium project to help move browsing forward on new ARM-based Windows devices. In that context, we have been thinking through plans to adopt the Chromium open source project in the development of Microsoft Edge on the desktop to create better web-compatibility for our customers and less fragmentation of the web for all its developers, and we’re now ready to move forward.  

As part of this, we hope and intend to become a significant contributor to Chromium, in a way that can make not just Microsoft Edge—but other browsers as well—better on both PCs and other devices.  We’ve written down our “OSS Principles for Microsoft Edge” below and “What Happens Next” to clearly outline our approach to contributions.

Our plan is to engage in a way that embraces the well-established open source model that’s been working effectively for years:  meaningful and positive contributions which align with long-standing thoughtfully-designed architecture, collaborative engineering, and keeping in mind that we, together as a community, seek the best outcome for all people who use the web across many devices.

## Microsoft and The Web Today 
Our *intent* is profoundly informed by our context. Historically, Microsoft has focused on three primary constituencies: end-users, developers, and enterprises/organizations. These audiences have informed the investments we have made in Internet Explorer in the past, and now inform the investments we make in Microsoft Edge. As we have listened to these customers over the last few years, a consistent theme they echo is the increased complexity of their environments, and a desire for consistency, simplicity, reliability, compatibility. 

We have effectively partnered with Google and other browser vendors over the years, first in the W3C and now even more closely through the WHATWG, to create common standards for the web platform to reduce this complexity and to improve the overall web experience. While browser vendors across the industry have made significant progress in aligning to these common standards, the underlying implementations and differing release schedules have created difficulties for our developers to fully benefit from the promises of the open web.

We see an opportunity now to move forward in a deeper way on a common compatible web platform that will serve Microsoft’s customers well and will provide mutual benefit for the larger web community while maintaining the marketplace benefits of competitive diversity in the browser ecosystem. Consider the following opportunities as we view them across our customer segments:

* *End-users* - Although Microsoft Edge has very high web compatibility for both standards-based HTML and for capabilities added by highly-used browsers like Chrome, our unique web-platform codebase still faces occasional compatibility problems as web developers focus less on HTML standards and rationally focus on widely used platforms like Chrome to develop and validate experiences for their customers. While we work hard to make updates and fix these issues continuously, our implementation of Microsoft Edge as a component that ships solely on the same schedule as the full Windows operating system has slowed our ability to update, causing platform fragmentation and exposing compatibility gaps. We think greater use of open source software (OSS) can improve this experience for our end-users. 

* Outside the Microsoft Edge browser, users of *other browsers* on Windows PCs sometimes face inconsistent feature-sets and performance/battery-life across device types. Some browsers have had slower-progress to embrace new Windows capabilities like touch and ARM processors. As you know, we’ve recently started making contributions that provide these types of hardware support to Chromium-based browsers, and we believe that this approach can be generalized: we think we can help to accelerate the web and users’ experience of it by contributing new capabilities to Chromium open source for the benefit of all these browsers and users.

* *Developers* – as the web has grown in usage across an ever-widening array of device-types, the complexity and overhead involved in testing web-sites have exploded. Since web developers—particularly those at small companies—need to test so many different systems, it’s nearly impossible to ensure that interesting sites will work well across all device types and all browsers. We hope to simplify this matrix for web developers by aligning Microsoft Edge web-platform with other Chromium-browsers and to provide meaningful, aligned capabilities on Windows that can be used by any browser.

* *Corporate IT* - IT managers face the downstream-complexity of users with many different device types, using both new and old sites, on devices owned both personally and by the corporation. We see meaningful value in creating better web compatibility and an aligned web-platform across browsers for Corp IT, regardless of device platform.

*What’s common across all these audiences is the two-sided benefit we believe we can bring them when we (a) engineer valuable new capabilities into a shared open-source project, for the benefit of multiple browsers, and (b) increasingly use that shared open-source ourselves in the browser we distribute at scale. We intend to do both of these.*

### Recent Investments in Web-focused Open Source
Over the last year, we’ve started to engage in the Chromium and WebRTC open source projects (among other OSS areas more broadly at Microsoft), and our efforts have been ramping up as we consider a wider range of device types. Some examples include…

* **Porting Chromium to ARM64**: We’ve done significant work in collaboration with Google engineers to enable Chromium-based browsers to compile and run natively on Windows on ARM devices. Because of our engineering investment, Chromium-based browsers will soon be able to ship native implementations for ARM-based Windows PCs, which significantly improves their performance and battery life. This is a great example of us making investments in Chromium to move-forward the web experience across a range of browsers on these new types of PCs.

* **Enabling WebRTC to work for Windows UWP apps**: For more than a year, we have been working on WebRTC for Universal Windows Platform (UWP). This offers developers a WebRTC solution for all our Windows 10 platforms, including desktop, Xbox, HoloLens/VR and IoT. Last week, we announced our agreement with Google to push the UWP fork of WebRTC Lib back to the WebRTC.org repo. 

* **Improving ANGLE**: In the past, we have made improvements to ANGLE’s D3D11 backend and improve its performance. More recently, we collaborated with Intel and the ANGLE team on additional improvements to make ANGLE the official backend for WebGL in Microsoft Edge. 

We recognize that these are modest-but-still-meaningful examples of web-oriented open source contributions. Both have provided us with a valuable perspective on how we can collaboratively use and contribute to Chromium in a healthy way. Across Microsoft, our OSS expertise and focus has grown – and our web teams are excited to take these lessons and move the web experience for millions of people forward.

## Microsoft Edge + open source: a new direction for Microsoft
Getting down to brass tacks ... we have put this document together to be transparent to relevant OSS contributors and partners about our intent.

### Use of OSS in the Microsoft Edge Browser
While we’ve been consumers of Chromium open source for shipping our Microsoft Edge mobile browser and for some components of Microsoft Edge desktop, we’ve made the decision to move much more of Microsoft Edge desktop to use Chromium open source and to increase our contributions back to this community. 

The key aspects of this evolution in direction for Microsoft Edge are: 

1. *We will adopt Chromium as the web platform for Microsoft Edge desktop*. Our desire here is to align Microsoft Edge’s web platform both (a) with web standards and (b) with other Chromium-based browsers, for improved compatibility and a simpler test-matrix for developers.

2. *We will evolve the Microsoft Edge app architecture, enabling distribution to all supported versions of Windows including Windows 7 and Windows 8, as well as Windows 10. We will also bring Microsoft Edge to other desktop platforms, such as macOS*. Improving the web experience for end users (better compatibility) and developers (less fragmentation) requires a consistent web-platform as widely available as possible. To accomplish this, we will use Chromium’s cross-platform app-technology along with a change in our distribution model, so that the Microsoft Edge experience and web-platform become available across all supported operating systems.

3. *We will offer our Windows platform expertise to improve the experience of all Chromium-based browsers on Windows*. Our philosophy of greater participation in Chromium open source will embrace the contribution of beneficial new tech, consistent with some of the work we described above. We recognize that making the web better on Windows is good for our customers, partners and our business – and we intend to actively contribute to that end. We welcome the opportunity to partner with the Chromium community in the areas of battery life, touch, accessibility, security, and other areas of mutual interest.

### Our contributions: Principles and expectations 
A key goal in providing this document to the teams and people who are already immersed in Chromium OSS is to indicate how we plan to contribute and to kick-start the engineering planning needed to bring valuable new tech into Chromium browsers.

We're excited to engage more deeply with the broader Chromium project. This has been a heavily-weighed decision and one that we believe is the right next step. That said, we're taking that step in the spirit of learning. We know we have a lot to learn as we increase our use and contributions to Chromium, and we look forward to engaging and contributing back to the broader community in a collaborative way. We are looking forward to evolving the nature and scope of our involvement over time. 

### Our OSS principles for Microsoft Edge
1. *We are making this decision for the long term*. We expect our engineers to learn and over time become experts in the Chromium project and grow into active and responsible members of the community. We are eager to increase our contributions to the Chromium project and will continue to maintain any contributions we make.

2. *When seeking improvements in the web platform, our default position will be to contribute*. We are focused on delivering a world-class browser with Microsoft Edge through its differentiated user experience features and connected services, but where new platform capabilities are concerned, we will seek a ‘rising tide that floats all boats’. We will get started with bug fixes and meaningful contributions in such areas as ARM64 support, accessibility, security, touch input and power enhancements on Windows.

3. *We recognize and will respect the architecture requirements and engineering approach that are intrinsic in web open-source projects and have made Chromium successful*. There are many aspects that have governed Chromium OSS and other projects: multi-device support, multi-OS support, rigorous real-time engineering, etc. Although our company has historically had a focus on Windows PCs and we believe we can make contributions that improve browsers on Windows, we also understand that web OSS projects embrace a wide range of device-types, including Android, and that contributions must accommodate this device diversity. We will contribute in a way that is consistent with the architectural design that meets Chromium’s cross-platform and cross-device needs. 

4. *We believe the evolution of the open web is best served though the standards communities and the open web benefits from the open debate from a wide variety of perspectives*. We will remain deeply and vigorously engaged in the standards discussions in the context of the W3C, ECMA and the WHATWG where the perspectives of vendors developing competing browsers and the larger web community can be heard and considered. 

### Contribution: Initial Areas of Focus
As we’ve progressed our OSS work and considered the places where our engineering expertise can make the biggest difference for users and developers, we’ve put together an initial list of contribution “areas of focus”. 

We’d like to underscore that we view this list simply as the starting point—some areas where we can learn/practice together and create meaningful value in the Chromium codebase for all its consumers. 

* *ARM64* - Our plans here are to continue/finish the porting work that brings the Chromium codebase to support for ARM-64 and thus browsers can be shipped which support these devices natively. 

* *Accessibility* - To serve the needs of all our customers, we intend to build upon the accessibility of the Chromium codebase by adding Microsoft UI Automation (UIA) interfaces to support Narrator and other assistive technologies on Windows, integrating with Windows Ease of Access settings such as high contrast and caption styling, improving controls accessibility, and supporting caret browsing.

* *PC-hardware evolution* for modern input types (e.g. touch) - We can help improve desktop touch, gesture recognition and scroll/panning smoothness, particularly on newer, more modern Windows devices.

* *Security* - It is, of course, of paramount importance to all browser vendors that web users are kept as safe and secure as possible. In support of this shared goal, we are looking forward to partnering closely with the Chromium Security team and contributing our experience with building secure software in general, and our expertise with the Windows platform, in particular. 

## What Happens Next
This is a big step for Microsoft, for the Microsoft Edge team, and we recognize it will be a big step for the Chromium project as well. We are enthusiastic about the benefit we believe this will bring to the larger web community. We are eager to begin engaging with our counterparts at Google and the other contributors to the Chromium project, and in the Chromium project generally, on how we can move forward together on a common web platform. At the same time, we recognize the value of competition and intend to bring-to-life our best vision for a Microsoft Edge browser that builds on Chromium open source via differentiated user experience features and connected services.

We already have positive working relationships with many Chromium contributors based on our work in the standards bodies and in prior shared engineering efforts. We look forward to building on those relationships and learning-as-we-go how we can best contribute to this implementation of the open web.

To provide a more specific sense of what actions we’ll take with and following this memo, here’s the short-list:
1. We will start by contacting the engineering owners of various parts of the Chromium project to engage on how we can begin contributing in the areas listed above. This includes Google as well as other companies.
2. We will inform other key partners about this evolution in our Microsoft Edge strategy: e.g., WHATWG, the W3C… as well as our OEM partners, high-interaction development partners and others.
3. We’ll make a public announcement via blog post so that the external community of people interested will have a transparent view of our strategy change. 
4. We’ll post this document to GitHub so any interested developer or web-community member can read about our plans directly.

We invite your comments, advice, and feedback as we begin to engage with you on the Chromium project!
