## WaveCraft: An Open-Source Virtual Studio Technology Instrument
Devang Ghela, Spring 2023


###  Abstract
Open-source work and software development has made impacts on many industries and areas, but one area that needs more attention is the area of music production. This paper proposes a process that uses open-source principles in the form of openness, collaboration, and innovation for developing and managing a free, open-source Virtual Studio Technology (VST) plugin to be used in Digital Audio Workstations by music producers. It also lays out ideas for building and maintaining a community of users and developers for the plugin.


### Introduction
Recording and modifying music used to require large, expensive pieces of hardware to produce the effects and sounds that musicians desired. The high costs and need for space to hold those pieces acted as a barrier to enter the realm of music production for aspiring musicians, producers, and those who were just curious about the hobby. Over time, technology progressed, and recording became more and more dependent on computers for the process. 

This eventually led to Steinberg Media Technologies creating something for computers that would simplify the pipeline for music production: the Virtual Studio Technology or VST. As put by Steinberg, “VST allows the integration of virtual effect processors and instruments into the digital audio environment” (Steinberg, 2023). As that might suggest, there are two major types of VSTs: instruments and effects. Regardless of the type, VSTs work to simulate the sounds produced by the expensive, physical hardware I mentioned before, all without having to actually use it. Digital Audio Workstations or DAWs are pieces of software that allow for composition of multiple tracks of audio files and instruments, and VSTs work as plugins to integrated into and used in them.

The creation of the VST framework has led to the creation of several plugins that imitate physical music creation hardware for a relatively low cost. Unfortunately, the low cost can still be a barrier to entry for those who want to get into music production. This paper aims to lay out a possible solution this problem: WaveCraft, an open-source VST that would be available for free to the public for use and for modification.


### Purpose
By following open-source principles and working with a thorough technology stack, the development and management of WaveCraft can benefit the music production community, offering both versatility and value. The three open-source principles that will be embraced include openness, collaboration, and innovation, each playing a vital role in enhancing the project's appeal and utility to those who may want to use it, and even those who want to work on a new version of it.

Openness, as a principle at the forefront, establishes a foundation of trust within the community. By ensuring developers are honest and transparent about their work and updates, WaveCraft can cultivate a sense of legitimacy, fostering a community that believes in the project's integrity and objectives.

Collaboration, another key principle, involves the engagement between project developers and musicians who utilize the software. This interaction guarantees that WaveCraft meets industry standards and incorporates the essential features expected from an everyday VST. By incorporating valuable input from musicians, the project can address their specific needs effectively. At the same time, developers will also collaborate with each other bringing together different perspectives and skills to the project.

Finally, innovation as an important principle, drives the gradual but continuous growth of WaveCraft. WaveCraft will distinguish itself from other widely used VSTs by introducing new and groundbreaking features after testing said features and gathering feedback on them. This focus on innovation ensures that the software does not fall into obsolescence, and instead remains responsive to current and new trends, while meeting the demands of music producers.

Overall, WaveCraft aims to be a high-quality, open-source VST that facilitates experimentation within the open-source community and also contributes to the growth and advancement of the music production industry. By adhering to open-source principles such as openness, collaboration, and innovation, WaveCraft will establish itself as a versatile tool that musicians and encourages creative exploration within the field.


### Target Audience
WaveCraft is meant to be designed with a diverse audience in mind, but it is expected that they all have an interest in music or production in some way. There are plenty of people who can benefit from this project; they can be divided into two groups. Users are the ones who actually use the plugin to produce music and design sounds while the developers are the ones who work behind the scenes to grow and improve the project.

The first few types of people that come to mind in the user group are independent musicians, producers, and sound designers who might be looking for affordable and customizable solutions for their creative needs. Without the backing of a bigger entity like a music label for funding, it can be difficult for those types to access industry-standard tools.  Users can also include those that are teaching music production as well as the ones who are learning from them. The people who want to learn production may not be able to sacrifice hundreds of dollars for a VST that can do the same thing as WaveCraft, and the teachers would not be able to gather students if they tools they use to teach aren’t easily accessible for beginners.

The developer group consists primarily of people like software developers interested in contributing to an open-source project related to music or sound processing. The group can also simply have people who are very enthusiastic about music technology and want to be a part of furthering their passion.


### Strategy
To ensure that the development and management starts off and remains smooth while allowing growth, some open-source principles WaveCraft would adopt are openness (or transparency), collaboration, and innovation.

#### Openness
Starting off with the principle of openness, The Open Source Way Guidebook 2.0 suggests that instilling a culture of transparency or openness in a project “builds trust, handles objections by including feedback as solutions along the way, and builds toward a community acting as a chorus” (Wade, 2020).

In the case of WaveCraft, a major part of the plan to foster that culture is to host the project’s source code publicly on the version control platform known as GitHub. This will allow easy access to the code for people who may be interested in checking the project out. It will also force transparency on the project when developers make changes to the software. At the same time, using GitHub allows developers to create thorough documentation for describing the code and technologies of the project. This documentation also includes manuals and guides that can easily be accessed by developers new to the project or those who want to build onto it on their own fork. As a final note that will be expanded upon later, the process of developing and managing WaveCraft will be very visible to the target audience through regular updates on progress and decisions.


#### Collaboration
Collaboration is another key pillar to ensuring WaveCraft is developed and managed well. Opensource.com states, “When we’re free to participate, we can enhance each other’s work in unanticipated ways” (Opensource.com, 2023).

WaveCraft would be built using a collaborative development model, and that means that there would be collaboration among developers of WaveCraft and those building onto their own forks. Ideally, the project would also encourage collaboration between those developers and the userbase of the plugin (musicians, producers, etc.) as their experiences can be analyzed for needs. 
Something else that will help the collaborative model is GitHub’s pull request system. This system allows for contributors of a project to have their desired changes reviewed before they are implemented into the actual GitHub repository. Besides adding a layer of security to the project, having someone check over the changes and code can be seen as having a paper proofread before submitting it.

As one may expect, communication is an important part of collaboration, so a part of the collaborative development model is to create open channels of communication for the community. One idea for this is to setup a Subreddit on the discussion website, Reddit. The subreddit would allow the members of the community to discuss WaveCraft and would encourage an exchange of new ideas. Reddit already provides tools to aid in moderation of content, and a system for finding moderators within the community can easily be set up. A similar idea is to have a Discord server for the WaveCraft community. In this server, there would be channels for various topics related to WaveCraft. Either idea would maintain a culture of collaboration.

Besides communication, it is also important to set standards for using the source code or adding on to it. To ensure this WaveCraft, would be released under the GNU General Public License (GPLv3 specifically). This license would offer users the freedom to: “use the software for any purpose,” “change the software to suit [their] needs,” “share the software with [their] friends and neighbors,” and “share the changes [they] make” (Smith, 2022). Overall, this license will make sure the project and other derivative works would stay open source.


#### Innovation
A minor problem in the world of VSTs is that are already plenty of them (premium and free) to be used by musicians and producers, and there will always be new ones emerging as new trends come around. For those reasons, it is important that innovation is one of the focusses of WaveCraft.

Once the base of the plugin is developed, the development of unique features and new sound design capabilities must be developed to ensure that it is easily distinguishable from existing VSTs. To figure out the needs of users, the team would first seek feedback through their communication channels. From the feedback, developers could implement the desired features. These features would then be sent out for testing by the users. From there developers can see what works well and what needs work. This cycle would inevitably be repeated as new trends emerge in the production space.

Another idea that can be used to ensure innovation in the development and management process is hosting events like hackathons which would allow developers to create new features and experiment with the source code under a compact amount of time.


### Technology Stack
The technology stack required for developing the open-source VST instrument project will include various tools and libraries. A major tool that will be required for creating WaveCraft is Steinberg’s VST Software Development Kit or SDK (currently version 3.7.7) (ygrabit & scheffle, 2023). The SDK contains libraries that a developer can use to make the VST process digital signals into audio. It is written primarily in C++, so it is logical for WaveCraft to be written in C++ as well. It is important to develop a Graphical  User-Interface for ease of use for the users. To help with this process, Steinberg has also developed a library for just that called VST GUI (Steinbergmedia, 2023). Developers could harness the power of using these tools together to create a powerful, easy-to-use VST for the users. As I have previously mentioned, GitHub would be the platform that hosts the code for the public. A major reason for this is because Git would be used by developers to actually check the code out for modification. As new trends emerge and disappear, the tech stack may be expanded or become smaller, but for now, the mentioned tools should be good for creating a base for the project.

### Community
After the initial establishment and development of WaveCraft, it will be very important to sustain the project by having a community to loves using it and working on it. To do this there is a plan of doing various things to ensure that the community is looked out for while shining a light on the project within the music production space.

The first idea is to create and maintain a website for WaveCraft that shows off what the project is about. It can serve as a hub for people who are new to the project, but also something that current users and developers can go to for news on the project. This can also be considered as another channel of communication.

After the base build of WaveCraft is released, it will be important to get the word out and promote it. There are already sites that plugins can be sold and promoted on, so that would be one part of this effort. Another part of this is to promote it on channels of communication that music producers frequent like Subreddits. Content creation around music production is a growing area that can also help promote WaveCraft. There are plenty of creators who have a knack for showcasing VSTs, and they can be approached for promotion. Another possible route of production is sending WaveCraft out to music producers for them to use in their workflow. Doing all of this should help initiate a following for the plugin.

Once there is a following, it is important to make sure the people within it get along and are welcoming to people who are new to the community. To help with this, WaveCraft’s community will have a code of conduct. This code of conduct will ideally create a positive atmosphere for everyone including newcomers. This, in turn, should foster collaboration and contribution from the developers and users.

As previously mentioned, hackathons and hackathon-like events can be held for community members as a chance to collaborate and contribute new ideas for features to add. Something somewhat similar to this is having an event called a “Jamathon” where WaveCraft producers have a limited amount of time to create a song or cool sample using WaveCraft within the pipeline. Something along the lines of both of those events is hosting conferences or meetups where prominent innovations and achievements made by community members and developers can be showcased.

Finally, users who want to dive deeper into the realm of development can be acknowledged as well. The technology stack may evolve as new technologies are added into it, so it would be very important to get new and current developers familiar with said technologies. For this process, events like seminars and workshops can be held to teach developers how to use any new tools.

By implementing these ideas at appropriate times, WaveCraft can establish a community to builds onto itself and continues to grow as the world of music production does.


### Conclusion
By following open-source principles in the form of openness, collaboration, and innovation for the development and management of WaveCraft while fostering and growing the community of users and developers, I believe that the plugin can make a significant change in the world of music production.

### References
Opensource.com. (n.d.). The open source way. Opensource.com. https://opensource.com/open-source-way. Accessed 01 May 2023.

“Our Technologies.” Steinberg, www.steinberg.net/technology/. Accessed 01 May 2023.

Smith, Brett. “A Quick Guide to Gplv3 - GNU Project - Free Software Foundation.” GNU Operating System, 4 Jan. 2022, www.gnu.org/licenses/quick-guide-gplv3.html. Accessed 01 May 2023.
 
Steinbergmedia. “Steinbergmedia/Vstgui: A User Interface Toolkit Mainly for Audio Plug-Ins.” GitHub, https://github.com/steinbergmedia/vstgui. Accessed 01 May 2023. 

Wade, Karsten. “Defining Healthy Communities.” The Open Source Way Guidebook 2.0, https://www.theopensourceway.org/the_open_source_way-guidebook-2.0.html. Accessed 01 May 2023. 

ygrabit, and scheffle. “Steinbergmedia/Vst3sdk: VST 3 Plug-in SDK.” GitHub, https://github.com/steinbergmedia/vst3sdk. Accessed 01 May 2023. 
