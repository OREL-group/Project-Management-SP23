# **_The CodeBLEU Expansion_**

Khushi Jain, Spring 2023

## **Executive Summary**

This paper gives an overview of "_The CodeBLEU Expansion_": an open-source project for expanding evaluation capabilities of code-generation. _The CodeBLEU Expansion_ aims to increase evaluation support for more if not all programming languages. With the rise of code-generating tools and applications, there is also a greater need for ensuring **reliability** and **readability** of machine-generated code. CodeBLEU is a metric that can supposedly strike a decent balance between the two; however, current codebases only support evaluation of Java, JavaScript, C#, php, go, python, and ruby.

With _The CodeBLEU Expansion_, I hope to create a standardized package that leverages the CodeBLEU metric to evaluate code-generation models of any language. To achieve this goal, I aim to collaborate with a team of developers, NLP experts and researchers, applied scientists, and Code Bleu and/or Hugging Face contributors in a Scrum Agile environment. This document details a draft of my project planning process including background, goals, scope, strategies, and potential road- blocks/challenges.

_Note: I am no expert in NLP, NLG, or code evaluation, and completely acknowledge that this project and its scoping may be impractical. This document serves to overview a potential plan for a hopefully, implementable project._

## **Problem Identification & Purpose**

According to Gartner Inc., "the worldwide market for low-code development technologies is projected to total $26.9 billion in 2023, an increase of 19.6% from 2022" (Gartner). "By 2025, organizations will build 70% of their new applications using low-code or no-code platforms" (Shuler, 2023). "Low code can speed up application development by a factor of 10… reduc[ing] the time needed to build custom applications between 50% -90%" (Shuler, 2023). "Low code allows the average company to avoid hiring two IT developers, providing an additional $4.4 million in business value over three years plus labor reduction" (Shuler, 2023). Given these stats and the recent advancements of LLMs (Large Language Models), there is evidently an increasing demand and capability for code-generation, and it has the potential to streamline development across many organizations. However, these predictions are only valid given the assumption that platforms will produce good-quality code. Despite all the advantages, there are limitations to low-code/no-code platforms: "poor application performance and resource use" (Noelle, 22). Low code platforms "can…lead to errors…that then go undetected long enough to waste time and resources" (Noelle, 22). Not to mention, in terms of readability, the "obscure techniques and mangled variable names" can also be a pain to deal with (McMahon, 2019). With these major drawbacks, it becomes difficult for organizations to scale, if not adopt, such methodologies for development. If companies choose to resort to such technologies, they will need to hire engineers to evaluate and potentially reengineer/refactor generated code. This makes the development process inconvenient, introduces a lot of manual labor, and takes away productive time from innovation.

To address these drawbacks, I desire to start _The CodeBLEU expansion_. I am writing this proposal with the strong belief that people should be able to rely on code-generation without undergoing tedious human evaluation or crafting extensive test-cases for every code-evaluation task. _The CodeBLEU expansion_ would hopefully result in a consistent and reliable methodology for measuring the quality of any code-generating model. That being said, the goal is not to standardize how code is evaluated, but rather create a consistent tool/platform for all code-evaluation tasks. Ultimately, different types of code have different kinds of structure and requirements, and not all code should be evaluated the same way. However, it would be nice to have a standardized industry-approved tool/package with consistent steps for customizing all code-generation evaluation tasks. The differentiation should happen in the back end, which users should not have to worry about. Full disclaimer: this technology is not meant to eliminate the need for evaluation, but rather, make it easier and faster to diagnose weaknesses in code-generation models, and get a reliable score representing its effectiveness.

To summarize, with _The CodeBLEU expansion_, I hope to standardize a python package for evaluating code-generation and expand language support for code-generation evaluation. This will make code generation more reliable and scalable, thereby streamlining development pipelines across various industries. _The CodeBLEU expansion_ should reduce the burden for evaluators and test-case developers, while increasing time to plan software and model design rather than coding or reengineering them. Ultimately, the overarching goal is to help developers and organizations deploy code easier and faster.

## **Target Audience**

The target audience who would use this technology includes developers and the tech and IT departments of any organization. Ultimately, a simplified process of evaluation is probably beneficial for anyone/ any team that wishes to deploy models generating large amounts of code. If not, they would have to code or manually read a bunch of generated code themselves.

This would also be useful for start-ups and companies who create models/tools for autocompleting code. A great example is start-ups creating auto-completion and assistive coding tools for smart contracts. People contributing on the blockchain often need help writing smart contracts, and these assistive tools-based platforms make it easier to develop smart contracts. Companies using or developing such tools can use _The CodeBLEU Expansion_ as a metric to ensure that the tools are generating decent quality Solidity/Vyper contracts.

Even if organizations already have procedures for evaluating and reengineering generated code, including our technology would only improve their chances of deploying good quality code and streamline their processes for improving generative models. We hope that _The CodeBLEU expansion_ could evolve into an industry standard for measuring how well a model generates or autocompletes code. For example, we hope top code-generation start-ups will market themselves with statements like: "a tool with average 0.9+ CodeBLEU performance".

## **Implementation & More About CodeBLEU**

### **CodeBLEU:**

Before detailing my plans for implementation, I would first like to explain the CodeBLEU metric and existing capabilities around it. CodeBLEU is a metric for evaluating source code generated by machine translation systems (GitHub). It calculates the precision and recall of the generated code vs translations (Ren et al., 2020). In other words, it compares ground truth or ideal code to model-generated code. CodeBLEU is designed from the original BLEU score: a metric "calculated by comparing the n-grams of your predicted text with the n-grams of the reference text" (Dash, 2023). N-grams refers to a sequence of n-words, and the greater the number of matches between the generated and reference text, the higher the BLEU score (Dash, 2023).

BLEU, however, was created to specifically evaluate **natural language**** generation **, which was not effective for** code generation **. Code generation has an additional need to be logically correct and functional besides just being readable. To fulfill this gap, the CodeBLEU metric was created to balance both** semantic **and** syntactical** correctness from a coding context and return a summarized score between 0 and 1 (GitHub). Semantic correctness refers to the readability and intuitiveness of the code structure. Syntactic correctness refers to logical/syntax accuracy, making code compilable. CodeBLEU incorporates these aspects into score calculation by integrating abstract syntax trees for code syntactics and data-flow for code semantics (Ren et al., 2020). These integrations result in 5 scores: "ngram\_match\_score", "weighted\_ngram\_match\_score", "syntax\_match\_score", "dataflow\_match\_score", and an overall "CodeBLEU" score (Hugging Face). Including the sub-scores makes it easier to analyze the specific weaknesses of a code-generation model and tweak it accordingly.

There are 2 common use-cases for CodeBLEU: evaluating complete code-generation and autocompletion. In the complete code generation format, the user will take pieces of good quality code and write corresponding prompts for which he/she would expect their tool to generate similar pieces of code. Those prompts would then be passed into the code generation tool to generate, hopefully, similar code segments to what the user originally had. The original code segments and their corresponding generated counterparts would then be passed into the CodeBLEU model, which would output the scores described in the paragraph above. The autocompletion use-case would follow a similar approach, except, the user would break apart the pieces of good-quality code into smaller even-sized chunks and pass those into the auto-completion tool in-place of the prompts. For example, let's say I split a piece of code into 3 chunks: A, B, and C, my ideal predicted chunks would be A+B, and B+C respectively. Chunks A and B would be passed into the generative tool and CodeBLEU would measure how much A + B and B + C match generated output.

![](RackMultipart20230512-1-vo8dc9_html_6d1408b52439086a.png)

### **Implementation:**

The problem with current codebases for CodeBLEU is that they only include support for evaluation of Java, JavaScript, C#, PhP, Go, Python, and Ruby. This significantly limits the applicability of CodeBLEU metric. Looking at similarity in code content is not enough, models using CodeBLEU need to have prior understanding of the language and its structure to make out what lines of code are considered syntactically equivalent. This is the reason why existing code for CodeBLEU is difficult to scale for every language application. _The CodeBLEU Expansion_ will hopefully address this problem by investing in additional language-specific or generalized models.

![](RackMultipart20230512-1-vo8dc9_html_cafbc1e9409ede82.png)

As displayed in the image, there are 2 main and 3 sub-rotes I have brainstormed for implementation. The two main routes are a **generalized model** and a **language specific model.** A language specific model would involve copying current code-base functionality for additional languages. A generalized approach would involve training the model by passing in segments of a new language not already supported by CodeBLEU GitHub and using the resulting model to compute the CodeBLEU metric. There are 2 sub-approaches to this route: **translation** and **w/out translation**. The method with translation would involve converting the new language to a language that is already supported by existing CodeBLEU codebases and continuing with the already defined functionality defined in current codebases. There will be 2 ways to configure this conversion: user-customized and model-predicted. In other words, either the user can directly specify which language they would like to convert to or have the model predict which language is most similar based on structure. The non-translation method would involve using a tool like tree-sitter to generate a specific language parser, followed by using the language parser to generate a syntax tree for the respective language (Ren et al., 2020). We would also embed a data-flow graph generating capability in our software (Ren et al., 2020).

As mentioned before, I am no NLP expert, so I don't know if any of these approaches besides the language-specific one is even practical. For example, the only current popular tools for code translation are the ones that have predefined language pairings. I am unaware of any AI models that can convert between any 2 generic languages. That being said, the translation approach is supposed to pick the translation language that is most similar in structure and capabilities to the user's language. So, translation would hopefully not be an impossible task. We may need to use the **language specific** approach to expand template languages for conversion, so that regardless of user's choice of language, there would be always be a translation language that is similar enough. The **w/out translation** approach may also potentially be impractical, as it may be difficult to automate the generation of a language parser, syntax-tree, and data-flow graph. But hopefully, we can engineer an option for the user to directly pipeline (pass-in) these elements. This is not ideal, as the user would have to undergo significant efforts to generate these elements on their own. However, it is still better than reimplementing the entirety of existing codebases on their own for their respective language and use-case. So, to reiterate, this document is not meant to be an exact planned out approach for carrying out _The CodeBLEU Expansion_, but rather a proposal for an approach to improving and expanding current code-generation evaluation capabilities.

## **Target Contributors**

The target contributors for this model are NLP experts and researchers; applied scientists; CodeBLEU contributors; Hugging Face contributors; people working on code translation; MLEs; data scientists; Java, Python, PhP, Go, C#, and Ruby developers; and niche language developers: such as Solidity or Rust.

The NLP experts and researchers will update project members with new technologies and research, help develop and modify overall project scopes. Key leaders of the project will consistently have meetings with them to ensure that the project is up-to-standard and that our procedures and methodologies are most optimized and relevant.

The applied scientists, data scientists, developers, and MLEs will develop functionalities (write code) for the project. The applied and data scientists will be involved with model development and data gathering/preprocessing procedures. Applied Scientists will be more involved with the research aspect and helping data scientists incorporate those findings into models and procedures. The MLEs will work on model deployment. The developers will fulfill all software/UI/test-case needs. We specifically need Java, Python, PhP, Go, and C# developers for testing and understanding existing CodeBLEU code-base capabilities. We equally need developers of other languages to create/test implementations for new languages, which CodeBLEU codebases don't already support.

The CodeBLEU contributors are imperative for understanding current CodeBLEU capabilities and defining scopes for how to expand them. They will play similar roles to the NLP experts and researchers but will be more involved with technical scoping and planning specific aspects of work streams. NLP researchers and experts are more for general guidance and examining things from a bird's-eye-view.

Hugging Face contributors can contribute to any of the roles above. They are a target population because they can help initiate collaborations or potentially help us integrate our repositories into Hugging Face. Additionally, as open-source contributors, they are likely willing to make contributions to our project.

_Note: There may be a lot of overlap for all of the roles described above._

## **Why open source?**

As an NLP-based project, this technology would have wide applicability. NLP is a fundamental area of study in artificial intelligence and has a wide range of applications, including speech recognition, sentiment analysis, machine translation, and chatbots. Improving evaluation of code-generation can be beneficial for all these applications b/c good quality code inherently drives all applications. With the rise of code-generative and assistive tools, this project could potentially benefit a broad range of users and developers: making it more relevant and impactful on an open-source platform. By making this project open-source, developers can work together to create tools and applications that benefit the wider community.

NLP-based projects also have a large and active community of developers and researchers, which means that open-source NLP projects can benefit from a wealth of expertise, feedback, and contributions. This can lead to faster development, higher-quality code, and more innovative solutions.

NLP projects often rely on large amounts of data, which can be difficult for individual researchers or companies to obtain and process on their own. By making NLP projects open-source, data can be shared and used more efficiently, allowing for faster and more effective development.

Finally, NLP is a rapidly evolving field, with new techniques and models emerging on a regular basis. Our projects can stay at the forefront of these developments by leveraging the collective knowledge and expertise of the community, and by allowing researchers and developers to experiment and collaborate more easily. Ultimately, opening this project to an open-source platform will help us remain up-to-date with our technologies and methodologies, as contributors would constantly update the code base.

## **Project Scope & Methodology**

### **Methodology:**

I recommend using Scrum Agile methodology for this project because it is flexible and responds well to changes in scope (Koenig, 2023). In a project where there is no fixed scope most contributors have equal power, Scrum Agile methodology is a good approach (Koenig, 2023). Additionally, Scrum uses an iterative and incremental development approach which is beneficial for projects that involve constant updates and improvements to the codebase, like this project (Koenig, 2023). Finally, Scrum encourages constant collaboration and communication, which is necessary for projects like these, which involve many inter-connected workstreams and a wide range of expertise (Koenig, 2023).

**Code Access and Project Scope:**

![](RackMultipart20230512-1-vo8dc9_html_cafbc1e9409ede82.png)

We plan on keeping code publicly available on GitHub, and will hopefully, eventually integrate with Hugging Face as an accessible repository. We plan on having a main branch for final updates, as well as 3 feeding sub-branches. The 3 sub-branches correspond to the 3 main work streams as shown above and discussed in the implementation section: **generalized: translation** , **generalized: without translation** ,and **language specific models**. The leadership for each work-stream will control lower branches within their respective sub-branch. For example, the **language specific models** branchwill likely have a sub-branch for each new language-specific model, and appropriate leadership will be responsible for incorporating these updates. Also, the lowest level sub-branches will correspond to individual or group entities trying to contribute to a specific task in one of the 3 work streams.

For the project scope, I plan on having 4 main phases - Phase 1: **Deciding Approach** , Phase 2: **Implementation** , Phase 3; **Evaluation** , and Phase 4: **Deployment**. In Phase 1, the NLP and CodeBLEU experts will help investigate the practicality of the 3 main workstreams I mentioned above, how they plan on logistically executing them, and the their timelines. Additionally, in this phase, the key GitHub workstreams as well as leadership will be decided. There will be one tech-lead and PM for each of the 3 main workstreams (which are subject to change in this phase), and an executive tech-lead and an executive-PM for the main branch. The 3 pairs of PMs and tech-leads are responsible for assigning any additional managers for their respective workstream, as well as controlling pull-requests for their respective sub-branch. The executive tech lead and PMs are responsible for controlling pull-requests for the main branch; as well as managing, communicating, and supplying resources and connections to the workstream tech leads and PMs. The executive tech lead and PM are also responsible for planning the future of the open-source project, initiating collaborations with Hugging Face, and modifying scopes as necessary.

Phase 2 and Phase 3 will be a constant cycle, in which developers and leadership will focus on implementation and evaluating their implementations. It is a cycle because depending on the evaluation results, models and/or software may require various edits and changes. Or the stream may get extended, and more things will have to be implemented.

In Phase 4, we will try to do a hard pause of implementation and evaluation and focus solely on deploying the code. Poor results in deployment and other feedback may cause us to revert to previous phases. But the general, the goal is to stop editing all workstreams, so we can deploy without worrying about changes in code.

## **License:**

I believe the MIT License can be an ideal choice for _The CodeBLEU Expansion_ because it is permissive, simple, compatible, and offers decent protection (Snyk, 2020). Permissiveness enables flexibility in modifying, distributing, and using the software, while leaving the doors open for commercial use as well (Snyk, 2020). This encourages wider adoptions of the project's scripts and the models, which can lead to more contributions and improvements to the project.

The simplistic nature of MIT License reduces confusion and makes it easier to contribute to the project (Snyk, 2020). This can be particularly beneficial for an open-source project like _The CodeBLEU Expansion_, where there may be a diverse range of contributors with varying levels of experience.

The compatibility with other open-source licenses makes it easier to incorporate code from other projects into the scripts and models (Snyk, 2020). This can help extend the functionality of the project and enhance its capabilities, especially if we try to collaborate with Hugging Face projects.

Finally, the MIT License includes a disclaimer of liability, which can help protect members from legal issues related to the use or distribution of the scripts or the model (Snyk, 2020). This can be important _The CodeBLEU Expansion_, as it involves code generation evaluation, which may have legal implications.

## **Communications and Community Events:**

### **Communications:**

To maintain effective communication for our open-source project, we would use Discord as our primary communication platform. We would create a channel for each of our main workstreams (generalized model w/translation, generalized model w/out translation, and language specific models) to facilitate communication and collaboration among team members and PMs and tech leads for the specific project. Additionally, we would create a dedicated channel for NLP experts to discuss their approaches and share insights, as well as channels for additional managers and their sub-teams within a specific workstream. There will also be a leadership channel that is only accessible to key leadership: executive PM, executive tech lead, as well as the PMs and tech leads for the 3 workstreams. We would also set up a voice/video channel where team members can seek assistance from others in real-time, which can be especially helpful for resolving complex issues quickly. Finally, we will use Discord's expert labeling feature to ensure that team members can easily reach out to the right person for guidance and advice. By using these communication channels and tools, we can ensure that our team members can effectively collaborate, share knowledge, and keep the project on track to achieve its goals.

### **Community Events** :

The community events are strongly aligned with the project structure and scope. So, each phase has different kinds of weekly meetings held on zoom or Discord call. Phase 1 will have weekly meetings with NLP developers and experts to decide project scope and structure. Phase 2 will have weekly meetings for each workstream managed by the respective workstream's leadership, as well as a weekly leadership call among executive and regular tech leads and PMs. Phase 3 will retain everything from phase 2, but also include a weekly call with leadership and developers involved in code evaluation. Phase 4 will involve a weekly call will leadership and MLEs responsible for deploying code.

## **Sustainability**

Maintaining sustainability is an important aspect of any open-source project, and there are several strategies that can be employed to achieve this goal. One such strategy is to ensure that the project is implemented using appropriate technologies and languages that are well-suited to the task at hand. For _The CodeBLEU_ Expansion, Python is a suitable language choice for most of the code, as it is a popular language for ML and NLP applications. Our wide network of researchers and experts will help us stay up to date with our technologies.

Another important aspect of maintaining sustainability is to establish clear roles and responsibilities for project contributors, and a clear way to maintain repository code. By assigning executive leadership, workstream leadership, as well as sub-managers within each workstream, we are ensuring that work is effectively delegated and there is always somebody accountable at higher and lower levels. This leadership team is responsible for overseeing the work of contributors and validating that they can achieve their respective goals within a timeline. They also control the pull requests for their respective branch/sub-branches.

Finally, documenting the project and its processes can also help to maintain sustainability by providing a clear and accessible reference for contributors and future developers. This can include documentation on project goals, technical specifications, development processes, and community guidelines.

## **References**

_Codebleu - a hugging face space by dvitel_. codebleu - a Hugging Face Space by dvitel. (n.d.). https://huggingface.co/spaces/dvitel/codebleu

Dash, S. (2023, March 2). _Bleu score in NLP_. Scaler Topics. https://www.scaler.com/topics/nlp/bleu-score-in-nlp/

_Gartner forecasts worldwide low-code development technologies market to grow 20% in 2023_. Gartner. (n.d.). https://www.gartner.com/en/newsroom/press-releases/2022-12-13-gartner-forecasts-worldwide-low-code-development-technologies-market-to-grow-20-percent-in-2023

Kevin Shuler. (n.d.). _56+ Critical Low-Code Statistics to Review for 2023_. quandrycg.com. https://quandarycg.com/low-code-statistics/

McMahon, J. (2019, March 9). _Code that codes: The Pros and cons of code generation_. Medium. https://medium.com/bigdecimal/code-that-codes-pros-and-cons-of-code-generators-15b2e571281a

Microsoft. (n.d.). _CodeXGLUE/CodeBLEU.MD at main · Microsoft/Codexglue_. GitHub. https://github.com/microsoft/CodeXGLUE/blob/main/Code-Code/code-to-code-trans/CodeBLEU.MD

Nolle, T. (2022, October 11). _What it pros need to know about low-code limitations: TechTarget_. IT Operations. https://www.techtarget.com/searchitoperations/tip/What-IT-pros-need-to-know-about-low-code-limitations

Ren, S., Guo, D., Lu, S., Zhou, L., Liu, S., Tang, D., Sundaresan, N., Zhou, M., Blanco, A., & Ma, S. (2020, September 27). _CodeBLEU: A method for automatic evaluation of Code synthesis_. arXiv.org. https://arxiv.org/abs/2009.10297

_What is the difference between prince2 vs Scrum?_. koenig. (2023, May 1). https://www.koenig-solutions.com/blog/prince2-vs-scrum-a-comparison-of-the-two-methods#:~:text=PRINCE2%20is%20a%20plan%20based,customer%20requirement%20and%20project%20environment.

_What is the MIT License? top 10 questions answered_. Snyk. (2020, July 26). https://snyk.io/learn/what-is-mit-license/
