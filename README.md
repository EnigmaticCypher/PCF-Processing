# PCF Processing
## Introduction
This project was created out of the lack of good examples and instructions on how to begin
processing the PCF messages that IBM generates automatically as part of its normal queue manager operations.
While IBM does provide many samples for processing PCF messages in multiple languages, they do not provide any samples
that utilise the MQ Classes for JMS to process PCF messages, nor are there any good "getting started" guides related to
processing PCF messages that I could find. (With that being said, Colin Pace's blog has some posts in relation to
processing PCF which have been useful in solving some specific problems, thank you for posting those Colin!)

The project mainly focuses on pulling down these messages, then pulling them apart into their respective
individual parameters and extracting the data desired by the programmer. In this particular instance, I am looking
to build an open source and free monitoring / auditing system that tracks administrative actions and/or user actions
against a queue manager. This includes things such as running commands against the queue manager, altering the queue
manager's configuration in some way (eg creating a new queue, or setting a new channel authentication rule, etc), and
watching for blocked connection attempts to channels and tracking the sources of these attempts.

## Disclaimer
I'll just state it here for convenience, but I am by no means an expert in processing PCF messages, and the practices
undertaken as part of this project should not be considered to be the "best practices" unless otherwise specified by
IBM or more experienced members of the MQ community. Wherever possible I try to follow the advice given within the IBM
Knowledge Center regarding best practice, and will provide comments within the code that link to specific knowledge
center articles in relation to that particular area. A good example would be processing PCF messages in JMS has a known
pitfall in relation to little endian platforms. The solution to this is outlined within the knowledge center, and I'll
be providing references to that page in the relevant part of the codebase here.

The following is a list of well known individuals within the MQ community, whom I have referenced as part of my
research:

* Colin Pace
* Morag Hughson
* Paul Clarke

## Contributing to the Project
Should you have some spare time and wish to help me out with building this, please feel free! I'm fairly busy with my
day job, and so this will likely have its ups and downs according to whether or not I have time available to dedicate
to working on it. Create a fork of the repository, make all the modifications you like, and create a pull request back.
The only requirement I have is that you follow the terms set out in the licensing section below. (TBA)
