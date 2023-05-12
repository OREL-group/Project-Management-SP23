# NoteTalk: An Open-Source Meeting Transcription Software

Riya Shah, Spring 2023, https://www.linkedin.com/in/riyashah360/

## Executive Summary
This paper will discuss the creation of “NoteTalk”, an open-source and real-time meeting notes transcription software. NoteTalk aims to help the daily meeting-attenders keep track of their meetings, important discussions, and tasks that need to be done instead of worrying about taking notes and participating in the meetings simultaneously. Additionally, this paper will discuss the open-source implementation and management process, focusing on three main principles: open collaboration, open data, and sustainability.

## Background
There are a few problems that exist when it comes to taking meeting notes. One of the biggest is that it becomes very hard to multitask, actively participate and pay attention in the meeting, and take detailed notes. From my own experiences and observing others, I have noticed that when individuals take meeting notes, they are scrambling to remember and write the important notes as the discussion goes on, therefore leading to a knowledge gap every few seconds. Furthermore, the knowledge gap only increases over time as we have to attend hours upon hours of meetings everyday focusing on a variety of topics and if effective meeting notes are not taken in time, then it becomes very hard to keep track of all the different discussions and quickly remember the important points and tasks that need to be done before the next round of meetings. Lastly, there are several existing softwares and apps in the market that provide meeting notes transcription, however there are several concerns with them as they are not open-source. There is no guarantee that the data will be handled in a responsible and secure manner, preventing third parties from accessing that data and using it for their own benefits.

For example, a journalist interviewed an individual, Mustafa Aksu, who was under surveillance by the Chinese government and used Otter.ai to transcribe the meeting. The journalist got an email from Otter.ai’s inquiring about the meeting with the Aksu and its purpose. The journalist conducted a deep dive into Otter.ai’s policies and realized that the company shares information with third parties and legally, the government can request to get access to the data with a subpoena. While no information was shared with any third parties, it shed light on the fact that cloud-based transcription services while effective, have a lot of risks and sensitive data might be accessible to those that could take advantage and cause further harm (Clark 2022). Also, some of the products in the market only focus on utilizing recorded meeting files to transcribe instead of providing real-time transcription and are not that accurate due to issues with audio clarity because of talking fast or with an accent.

In summary, taking effective meeting notes can be challenging and draining for the daily meeting attendee especially when trying to provide their undivided attention to the discussion. This leads to knowledge gaps and a struggle to remember the important points and tasks for several meetings in a day or a week. While the existing products transcribe meeting notes, there are several concerns regarding privacy and accuracy and therefore, NoteTalk is a unique open-source approach to this problem. 

## NoteTalk Purpose and Project Vision
The purpose of NoteTalk is to provide an open-source AI tool that not only transcribes meeting notes in real-time and explicitly writes the tasks needed to be done, but also values the need for open data policies and secure storage for sensitive data. Through NoteTalk, companies and individuals can utilize the tool and customize based on their data storage and accessibility preferences. If some companies discuss a lot of sensitive and top-secret information in their meetings, then they can download NoteTalk and store the data on their own servers and set their own regulations, therefore reducing the possibility of the data getting into the wrong hands. Also, through NoteTalk, I aim to further develop the open-source community by encouraging the responsible use of data to develop AI tools that do not discriminate based on race, accents, and other factors.

## Target Audience
The ideal target audience for NoteTalk are individuals that have to attend a lot of meetings and discussions and need a tool that will write the meeting minutes accurately, be able to keep track of the discussions, and differentiate between important points and tasks that need to be accomplished. These individuals can be students, teachers, corporate professionals, and others. Their pain points are focused on the need for a tool that helps them be more productive and spend less time writing meeting notes and more time paying attention in the meeting and providing their valuable input. NoteTalk will help them be more productive because they can listen and participate in the meeting alongside see conversation being transcribed on the screen live.

The second target audience for NoteTalk are companies or organizations that have a lot of meetings and want an in-house tool that all their employees can use and control who has access to the notes and data collected from the meetings. There is no limit on what type of company and organization because meetings are inevitable and all of them discuss information that they might not want to share with the public or give a third-party access to for reasons related to security, privacy, and competitive edge.
Overall, NoteTalk is applicable to all types of users, but can be the most beneficial for those that attend a lot of meetings and need to quality notes to refer to as well as companies that want to regulate the information discussed in meetings and increase their employees’ productivity.

## Benefits of Open Source
There are several benefits of open-source software and NoteTalk is well suited for this approach. One of the main reasons for developing an open-source transcription software is because it allows users to potentially “control their own computing” and data. Also, it encourages collaboration, so contributors can “improve projects quickly” and individuals can even add their own features based on their needs and requirements (Open Source Guides, 2023).
NoteTalk takes inspiration from Mycroft.ai which is an open-source voice assistant. Similar to Mycroft.ai, NoteTalk has a huge focus on data protection and privacy and therefore, the software can be run and hosted on the user’s own network, on-premises (Mycroft AI, 2023). Also, NoteTalk will not store any data and will follow the FAIR and open data policies to make sure that the data is handled in a responsible manner and cannot be sold or taken advantage of. Finally, creating an open-source implementation of a meeting notes transcription software will further train and develop the AI model. Open collaboration can allow contributors from all over the world to train the model to understand a variety of accents, dialects, and cadence, making NoteTalk the top accurate and inclusive real-time transcription software in the market.
As discussed, open-source projects are very advantageous and beneficial to society and with NoteTalk, we can really help our target audience be more productive and worry less about the data that is being collected and stored.

## Project Mangagement
### Project Scope
For NoteTalk to become a reality, there will be three phases. The first phase will be to gather high-quality training data containing a variety of accents, dialects, and recordings which state clear differences between notes and action items. Also, in this phase, we will conduct research to evaluate the natural language processing model to use for the transcription AI. This phase is the most important because without an effective NLP model and data to train it, the implementation becomes extremely hard and can threaten the project from being a success. The second phase focuses on implementation, developing the NLP model, the front-end, and backend. The second phase is extremely important because it is the bulk of the project. This phase will require several contributors and a lot of time. This phase will also have serval sub-phase to break it down into more manageable work streams that people can contribute to. The final phase will be the product launch and user testing. In this phase, we will launch the product with beta testing first to catch and fix any major issues that prevent users from getting the best NoteTalk experience. After beta testing and making sure we have a product that work effectively, we will officially launch it with a few companies and individual users to be productive and spend less time worrying about their meeting notes. As we gain traction and our customer base increases, we will refine NoteTalk and continuously train the model to perform better.

### GANTT Chart
The following GANTT chart will be used to provide the initial workflow and scope of this project. The GANTT chart will help contributors get the “bird’s eye view of the project” and will also show how “changing one task has the potential to impact” the project roadmap and workflow (Meardon). The GANTT chart will especially be helpful for this open-source project because there are a lot of moving parts and a lot of contributors, so I can make sure we are following the timeline and there is no confusion on what phase of the project we are on. The GANTT chart shows there are several tasks per phase and will be regularly updated as we progress through the timeline and the project, depending on how long each tasks takes and the roadblocks we face.
|Phase|Tasks|Weeks Needed|
|:----|:----|:----|
|Phase 1: Research|Research NLP Model|4|
| |Research Existing Open-Source Projects|2|
| |Research Transcription Methods|3|
| | Collect high quality data from various audio recordings|6|
| |Develop a high quality and cleaned training dataset from collected data|3|
|Phase 2: Implementation|Develop NLP Model|8|
| |Develop Front-end|5|
| |Develop Back-end|5|
| |Implement secure data storage methods|5|
| |Integrate Model with Front-end and Backend|5|
| |Train and Test Model and MVP|3|
|Phase 3: Test and Launch|Conduct Beta Testing|3|
| |Refine NoteTalk Based on Testing Feedback|3|
| |Officially Launch NoteTalk and Continue Testing|2|

## Open-Source Methodology
In addition to the GANTT chart, NoteTalk’s management methods will focus on the following open-source principles: open collaboration, open data, sustainability, and licensing. By applying these principles, NoteTalk will become a successful open-source project that provides value to the open-source community and the target audience.

### Open Collaboration
Open collaboration is integral for managing and working on an open-source project. Through this, “people from different backgrounds” can “co-create better products and services” because it allows more creativity and innovation (Pallister, 2023). Open collaboration will further enhance NoteTalk because the more contributors and perspectives, the less bias and racist the AI model will be.

To manage the collaboration, the Agile methodology will be implemented because that will provide some calmness to the chaos. Instead of trying to fix all the errors and bugs before beta testing is conducted, we will iteratively check the accomplished work through monthly and weekly sprints. The monthly and weekly sprints will help contributors keep up with the timeline, constantly debug and enhance NoteTalk, and help manage any unexpected challenges. The monthly sprints will be focused on the overall project success and making sure all the different tasks and their teams are doing well. The weekly sprints will help manage the teams and their tasks on a granular level. For example, the team tasked with researching existing open-source projects and models to use will have weekly sprints to keep track of the progress and their findings, but they will also be a part of a larger research team that will have monthly sprints, so they are aware of what the other research teams are doing and how each team’s contribution affects the research phase and the overall NoteTalk timeline.

To further manage the different sprints and tasks, we will utilize GitHub effectively. We will have a main branch where the fundamental code for NoteTalk will live so all collaborators can pull it and work. Since there will be a lot of versions for each task, we will also have sub-branches for each task and once the pull request is accepted, it can be pushed to the main branch. This will help in maintaining a consistent code base and making sure everything is thoroughly reviewed for any bugs before being pushed to the main branch for production and beta testing. Also, we will utilize GitHub’s Project Dashboard to visually manage the workstreams and tasks for each phase, so the team leads, and the contributors can quickly see what tasks they need to work on and what is done. The dashboard will be similar to the pictures on the bottom and will have more detailed tasks and descriptions as each phase occurs and there is a need to divide the tasks into more subtasks.

<img width="800" alt="image" src="https://github.com/Freedom360/Project-Management/assets/53009666/d55ab99e-7f98-4649-a4cb-bf0967951634">
<img width="469" alt="image" src="https://github.com/Freedom360/Project-Management/assets/53009666/7dc574f8-f360-4627-90fc-a505e4d773ae">

In addition to task management, documentation will be important in maintaining an open and collaborative environment. Each contributor will write documentation about the code they have written, and the team leads will also review the documentation and make sure it comprehensive and concise. There will be a documentation template for contributors to use so we have consistency across all the tasks, phases, and the overall project. By having consistent and thorough documentation for the project, any individual that wants to contribute to NoteTalk or even use the software will be able to easily understand the code base and how it works without feeling extremely overwhelmed.

In summary, through open collaboration, NoteTalk will provide an effective and efficient environment that encourages contributors to take initiative, innovate, and manage their task and the overall project timeline. With the help of weekly and monthly sprints, comprehensive documentation, and GitHub, the NoteTalk community will have to spend less time on understanding what work has been done and technical debt, and more time on developing the best open-source real-time meeting notes transcription software.

### Open Data
Since NoteTalk is a data-driven software because it listens to the meetings audio in real-time and then generates more data based on the audio, it is crucial to handle the data responsibly. NoteTalk will utilize a similar structure to Mycroft.ai where the data is only accessible to those that download the software on their own networks and servers instead of contributors. This way, users can control who gets access to their data and their meeting notes and NoteTalk is not liable for any of the data that is generated or collected. We will be transparent in what data is collected and handled on-premises through NoteTalk’s AI because the audio and notes may contain sensitive and confidential information. Also, we will ask for informed consent from the user to listen to the audio in the meeting, store it the data, and write the notes in their preferred note-taking app. Asking for informed consent before NoteTalk does its job is extremely important because if the user does not give consent and how the data is handled, then that can lead to issues with liability, data management, and data security, especially since the information in the meetings may be sensitive. Also, because it is an open-source application and individuals may want to use the training and testing datasets we have created or public data that has been generated, we will make it available to use, but access must be requested and there must be a clear reason and plan for how the data is going to be used to make sure it is not being taken advantage of or used by third parties. In conclusion, while NoteTalk aims to be as open and accessible with the data collected and generated, the data cannot be shared, collected, and used without proper consent from the users and interested individuals and NoteTalk will also not handle any data directly related to the meetings on its own servers, networks, and platforms for security and liability reasons.

### Sustainability
To maintain NoteTalk as an active and contributing project in the open-source community, we will take several sustainability initiatives. First, to make sure the contributor community is active and engaged in this project, we will have quarterly events to celebrate NoteTalk’s progression and all the hard work our contributors have put into making NoteTalk a reality. This event will focus more on celebration, networking, and developing the community, so contributors feel like they made an impact and are recognized for being a part of a unique project. Second, to maintain our codebase, we will try to utilize as much open-source technology as possible. We will use WhisperAI and Python because WhisperAI is an open-source speech to text model and can easily be used to develop NoteTalk’s AI without licensing or copyright issues. We will use Python because it is one of the most common languages for software development and AI. Also, Python is easy to learn and code with because of its syntax and there is a lot of documentation available online and a huge community for contributors to look into if they face any challenges while coding. Finally, to maintain the structure of this project, there will be several projects leads and team leads. Project leads will oversee the entire project and the phases. They will be responsible for running the monthly sprints, doing code reviews, managing the team leads, and developing an active and engaging community. The team leads will be responsible for a specific task or workstream in each phase and will manage the weekly sprints and the contributors on their team. This encourages responsibility and accountability because each member in leadership is responsible for making sure NoteTalk is a success along with all the contributors that are putting a lot of their time to make NoteTalk. Overall, through a clear leadership structure, the use of popular technologies, and an engaging environment, NoteTalk will sustain over time as the project reaches new heights and technology advances.

## License
There are two licenses that will be used to develop and maintain NoteTalk which are Apache 2.0 and OpenRAIL. Apache 2.0 will be used because it provides legal protection and allows companies and other organizations to use NoteTalk. OpenRAIL will be used because it is a “AI specific license” especially created to “use and distribute AI artifacts while requiring a responsible use” of the data and anything related to the model (Ferrandis, 2022). With Apache 2.0 and OpenRAIL licensing, NoteTalk will be open and accessible for anyone to use, but also prevent us from facing any legal issues related to company usage or the misuse of the AI and the data.

## Future Actions
Once NoteTalk has been developed and tested efficiently, we will continue to train and refine the mode, so it can write more effective and efficient notes and action items. After launching with a few companies, we will work on expanding our reach to more companies that want an in-house meeting notes transcription software for their employees. NoteTalk aims to become the best meeting notes transcription software focused on increasing an individual’s productivity and providing a secure way to manage the data being generated and collected through NoteTalk.

## References
Clark, M. (2022, February 17). This journalist’s Otter.ai scare is a reminder that cloud transcription isn’t completely private. The Verge. https://www.theverge.com/2022/2/16/22937766/go-read-this-otter-ai-transcription-data-privacy-report 

Ferrandis, C. M. (2022, August 31). OpenRAIL: Towards open and responsible AI licensing frameworks. Hugging Face – The AI community building the future. https://huggingface.co/blog/open_rail 

Meardon, E. (n.d.). What are Gantt charts?. Atlassian. 
https://www.atlassian.com/agile/project-management/gantt-chart#:~:text=Gantt%20charts%20help%20teams%20to,%2C%20milestones%2C%20and%20dependent%20tasks.

Mycroft AI, Inc. (2023). About Mycroft: The open source artificial intelligence voice assistant. Mycroft.ai.
https://mycroft.ai/about-mycroft/ 

Pallister, B. (2023, February 27). What is Open Collaboration?. Innovolo.
https://innovolo-group.com/innovation-en/innovation-terminology-en/what-is-open-collaboration/ 

Starting an open source project. Open Source Guides. (2023, May 2). https://opensource.guide/starting-a-project/#:~:text=Open%20source%20is%20powerful%20because,computing%2C%20relative%20to%20closed%20source. 














