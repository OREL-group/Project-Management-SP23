# HealthInsightX: An Open-Source Healthcare Analytics Tool

## Abstract
In this paper, I will describe a hypothetical open-source software I would like to create to help the healthcare industry gain meaningful insights into healthcare cost analysis. I will also explain the importance of the tool, how it can be used, and how the software tool will come together. This tool in the future can be added to EHR systems (electronic health records). Open-source tools can be more cost-effective for healthcare organizations, allow for greater customization and flexibility, and foster collaboration and knowledge sharing among healthcare professionals. So, being open-source is extremely important. With being open-source, it is important to make sure that the code is sustainable in the future and the right people have access to it to make the proper changes. By using what I have learned from the lectures in IS 340 and conducting external research for this hypothetical tool, I aim to establish the potential of this tool and the usefulness of it as an open-source project. 

I will go over the tool, its purpose, the target audience, current open-source healthcare analytic tools, the code behind the tool, events, privacy concerns with the tool, and the sustainability. 

## Introduction 
Healthcare analytics can be highly vital to healthcare professionals. The advancements in technology and data collection have resulted in a vast amount of information that can benefit humans. According to The Role of Data Analytics in Health Care, “The collection of data in health care settings has become more streamlined in recent years. Not only does the data help improve day-to-day operations and better patient care, it can now be better used in predictive modeling. Instead of just looking at historical information or current information, we can use both datasets to track trends and make predictions. We are now able to take preventive measures and track the outcomes.” Healthcare is constantly evolving and improving, and with the right tools, patient care can be improved. Tracking healthcare information can help professionals track the trends and make predictions that can lead to better decision-making and patient outcomes. 

Healthcare in the United States can be costly. “If hospitalization is necessary, data analytics can help practitioners predict risks of infection, deterioration, and readmission. This too can help lower costs and improve patient care outcomes” (The Role of Data Analytics in Health Care). Healthcare analytics can be highly complicated and challenging to sort and analyze. There is so much volume in the data that it’s essential to be extremely specific. We can’t take all the healthcare data, but if the software is particular on a clinical trial and ways to use analytics from that specific trial to save costs, it can be beneficial to the industry. 

## Purpose
The software tool itself will be used to analyze healthcare data and extract meaningful insights. The tool will be used for healthcare cost analysis and can be used with EHR systems for better data management that will be open-sourced so that it can be replicated for other instances. It will be called HealthInsightX. This project is open source meaning that “the source code of a piece of software is kept open and free to download, modify and incorporate into third party projects, which helps to improve the software itself over time” (Towers-Clark). My goal is that this project will continue improving over time, and more and more people will be able to contribute and make it so that healthcare costs eventually can be lowered in all specialties. With its ability to be more customized, healthcare organizations using it for their tailored needs could eventually make healthcare costs lowered for the patients. 

## Target Audience
The target audience for this project is anyone who works in healthcare. It doesn't necessarily mean that the group of individuals using this software needs to be doctors. Having a diverse user base can be helpful. It's important to emphasize that the tool can be used by a diverse range of healthcare professionals, including doctors, nurses, researchers, healthcare administrators, and possibly even patients, to track their symptoms/experiences. Patients tracking their symptoms can be handy. They can start to understand their own symptoms and possible triggers and take a more active role in their own health. Also, this open-source tool can be highly customizable. This means that anyone can tailor this tool so that it fits them, which is why it being open-source is essential. 

Review of Current Open-Source Healthcare Analytic Tools: 
With healthcare analytics being so useful, there are currently a few analytic tools on the market that people are possibly using at the moment, but that does not necessarily mean that they are the best tools. In this section of this paper, I will review current open-source healthcare analytics tools that are currently on the market and their advantages and disadvantages. 

One current open-source healthcare analytics tool that is on the market is OpenClinica, an open-source electronic data capture (EDC) and clinical data management system (CDMS). However, a limitation of this source is setting up the tool and using this tool requires technical expertise. This can be a huge learning curve for doctors, patients, and researchers that need to become more familiar with the technology. Also, integrating OpenClinica with other applications may require additional customization, which can add to the overall cost. 

Another possible tool is OpenMRS, which is an open-source electronic medical record (EMR) system. OpenMRS is a tool that can be customized and used in resource-limited settings. OpenMRS allows healthcare providers to collect and manage patient data electronically and analyze healthcare data for research and policy purposes. This would be the closest example of what I am looking to do with my open-source too. However, there are some things that could be improved to this tool. A disadvantage of OpenMRS is that its UX is less easy to use compared to other EMR systems, which can affect its usability and adoption. Another disadvantage of OpenMRS is that the tool is designed for small datasets or high-performance computing.

The final tool I wanted to mention was KNIME. KNIME is an open-source data analytics platform that can be used for healthcare data analysis, including data mining, machine learning, and visualization. It is extremely flexible and has a large community of users, developers, and contributors who support the platform. Some limitations of KINME is that integrating KNIME with other healthcare applications may require additional development and customization, which can add to the overall cost. My aim is to get a tool that is not extremely expensive, to lower healthcare costs in the future. KNIME can also have scalability limitations if it is not designed or optimized for large datasets or high-performance computing.


## Code
The code that would best work for this project is Python. Python is the best language for this project because of its ability to handle large datasets. Python also has so many great libraries such as NumPy, Pandas, Scikit-Learn. All of these can be extremely useful when analyzing data and use machine learning to predict information. For healthcare data, we want a python language that is used by many, and can keep up with the amount of data that is being processed. Also, the pre-built packages of Python are also useful because it can speed up the development process, which can be beneficial for healthcare data analysis. Also, Python is extremely user friendly and many people currently use it. Using Python will also ensure that the project will be sustainable in the future. 

This project’s code will sit on Github. The reason behind this is that a Github Repository can be created to host the code and can be organized into different sections. With people only having certain parts of access to the repository can also help ensure privacy. Version control is also a positive of using GitHub. With version control, git can be used to track changes and can allow for great collaboration. Automated testing can also ensure the lack of bugs in the code or break current code. 

Github is fairly easy to use, and there can be documentation and instructions within the repository to make sure that collaborators are making changes accordingly. Also, with pull requests, code changes can be reviewed. This way, if anyone was making changes to the code, there would be a review process to make sure nothing is being released that should not. Having code standards is vital to make sure that everyone is following the standards and all of the standards match up. Everyone can be different types of coders, so to have these standards can make it easier. 

If the repository is set up correctly, the issue management can be extremely useful using the Kanban boards. Keeping track of all the information in one place like Github can make it useful to see all the changes that need to be implemented and all the bugs that are the priority. 

Overall, having a well-organized and well-maintained GitHub repository can help make the project more accessible, inclusive, and sustainable for our open-source project. 

## Privacy Concerns
When creating this software, it is extremely important that a person’s healthcare information is private. Security and privacy will be extremely important due to not only the law but also ethical reasons. HIPAA is a federal law that requires the creation of national standards to protect sensitive patient health information from being disclosed without the patient's consent or knowledge.

Due to the collaborative nature of this tool, privacy is also extremely important. Secure storage of data is vital. Encryption of the data is needed, and it is also important that proper penetration testing is done twice a year to make sure that the data cannot be leaked and the security is checked. User authentication is also vital, and access control is important so that sensitive data is not open to everyone. 

Also, when training users, the importance of privacy must be maintained and made clear. Best practices should be maintained for all users and contributors of the open-source tool. This will ensure that everyone involved in the project understands the importance of privacy and is equipped with the knowledge and skills to maintain it.

All of this can help ensure that the data is secure and make sure that not anyone can be able to access the data. Two-factor authentication can secure the information. Regular audits are also a must to make sure that there are no breaches in the security. 

Furthermore, it’s important for the open-source tool to be designed with the user experience that has a clear privacy policy and guidelines for the tools. Trust between the patient and their HCP (healthcare provider) and this tool is vital. Without the trust, there can be fear of information being sold or used for something that is not conducive to the research. 

Open communication is also extremely important, and transparency with the patients also needs to be maintained to make sure that addressing privacy concerns and vulnerabilities. Overall, the importance of privacy in healthcare and the measures that will be implemented will empower the open-source tool will be fully taken into consideration. 


## Events 
There are events that regularly happen that can help the outcome of this healthcare analytics tool and make sure that it is adopted by more people. Adoption is extremely important for this tool so that it stays sustainable and more people use it for their tailored needs. 

Some events that would be helpful for this open-source tool are regular user feedback sessions. This would be helpful because it can be held with the contributors and users to gather their input on how to fix the platform. Having these regularly can make it extremely useful to start an issue management system where requests are taken care of based on the importance of the users themselves. This will also help with bugs more quickly and improve the usability of the application. 

Conference presentations can be beneficial for this platform. Throughout the year, there are so many different conferences for doctors, researchers, etc. It can be extremely beneficial to go and promote the platform and get the word out there on this platform. With more people adopting the platform, it can help improve the platform. Showcasing the tools and getting press on this platform can be helped and with more people learning about the platform, it could be better for the healthcare environment. 

Hackathons are also extremely helpful for open-source tools. When software developers, UX designers and other contributors come together for the tool, the platform can gain a lot of useful insights and the community can grow. With a bigger community of collaborators, the tool can grow faster and improve.


## Sustainability
For this project, sustainability can be extremely helpful. Being sustainable means that the data can be used and can grow. Prioritizing the accessibility of the tool, inclusivity of the tool, and being transparent about the data are extremely important. Encouraging feedback and collaboration is also vital so the project stays sustainable. A community of individuals who find the project meaningful and are willing to collaborate can also make sure that this project stays sustainable. A dedicated community is important to keep the project thriving over time; however, in order to do that, a long-term vision is vital. If this project is coded in Python, then commitment to maintaining code, documentation, and infrastructure can also be essential to maintain sustainability. Finally, in order to be sustainable, ethical practices are extremely important. We are working with highly private data, so using the data for ethical uses is vital. The confidential data of patients cannot be leaked. 

While I want to make sure that this tool is cost effective, it is also important to make sure that it is streaming enough revenue to keep the platform up and running. Developing partnerships with other companies or healthcare organizations can be vital to make sure that the platform is able to maintain itself. This would mean that with these partnerships, integrating the tool into the organization’s systems can also mean that there is more adoption of the tool. 

Also, since this tool is for the healthcare industry, I want to make sure that it is accessible. People of all ages and backgrounds should be able to use it. People from all communities should be able to use it including those with disabilities or underrepresented groups. With regular user testing and feedback, this platform should be easy to use for everyone without difficulties for long term growth and sustainability. 

## Conclusion 
Overall, my goal is that this project will eventually be implemented. I want a tool that is easy to use, cost effective, and eventually helps people. With the events and privacy of the tool, I hope that eventually, there is trust in the community for adoption of the tool. This would mean that eventually a lot of people start using it for the reasons that they need, since the tool is customizable. Eventually all types of people with diverse backgrounds and jobs in the healthcare field should be able to use the tool for their custom needs and gain the insights from the data collected. 


## References
Donato, C. (n.d.). SAP BrandVoice: Can Big Data Analytics Save Billions in Healthcare Costs? Forbes. Retrieved April 27, 2023, from     https://www.forbes.com/sites/sap/2016/02/22/can-big-data-analytics-save-billions-in-healthcare-costs/

HealthITAnalytics. (2019a, May 10). Is Healthcare Any Closer to Achieving the Promises of Big Data Analytics? HealthITAnalytics. https://healthitanalytics.com/news/is-healthcare-any-closer-to-achieving-the-promises-of-big-data-analytics

HealthITAnalytics. (2019b, November 25). Big Data Analytics, Precision Medicine Top Priorities in 2020. HealthITAnalytics. https://healthitanalytics.com/news/big-data-analytics-precision-medicine-top-priorities-in-2020

HITInfrastructure. (2018, November 5). EHR Integration Among Top Health IT Infrastructure Priorities. HITInfrastructure. https://hitinfrastructure.com/news/ehr-integration-among-top-health-it-infrastructure-priorities

Raghupathi, W., & Raghupathi, V. (2014). Big data analytics in healthcare: Promise and potential. Health Information Science and Systems, 2(1), 3. https://doi.org/10.1186/2047-2501-2-3

Ravishankar Rao, A., Clarke, D., & Vargas, M. (2018). Building an Open Health Data Analytics Platform: A Case Study Examining Relationships and Trends in Seniority and Performance in Healthcare Providers. Journal of Healthcare Informatics Research, 2(1–2), 44–70. https://doi.org/10.1007/s41666-018-0014-0

The Role of Data Analytics in Health Care. (2021, January 13). https://online.shrs.pitt.edu/blog/data-analytics-in-health-care/
Towers-Clark, C. (n.d.). Why Is Open-Source So Important? Part One: Principles And Parity. Forbes. Retrieved April 27, 2023, from https://www.forbes.com/sites/charlestowersclark/2019/09/24/why-is-open-source-so-important-part-one-principles-and-parity/
