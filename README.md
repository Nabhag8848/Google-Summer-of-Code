# 🚢 Summary of Work Under GSoC 2023

![Heading](https://github.com/Nabhag8848/GoogleSummerOfCode/assets/65061890/836f66fd-8a83-4c2b-bf62-38b276ecdaa9)
```
       Experience the Power of Notion inside RocketChat Workspace and Elevate Collaboration
```

## ✨ Project Abstract 

`Integrate Notion Via RC App` prioritizes teamwork by enhancing collaboration for workspace users. Imagine having the power of two essential platforms, RocketChat and Notion, united as one, eliminating the need to switch between two platforms. Teams can Seamlessly Connect, Effortlessly Manage various Notion Workspaces, Share documents, and Even View Documents all within RocketChat. The real magic lies in Preserving your Important message inside the Notion Page, Structured within the Notion Database, ensuring vital discussions, decisions, and insights are never lost again, fostering alignment and inclusivity as everyone stays on the same page, even if they're not actively chatting. Whether it's brainstorming sessions, meeting notes, or shared links, find them all in one organized place. Plus, Create Comments on the Notion Page, view the Notion Database, and interact with relevant information.Welcome to a new era of streamlined collaboration, Where RocketChat and Notion work together seamlessly to fuel your team's success.

## 🌅 Glimpse of Project
-  These Video is recording of Rocket.Chat's Google Summer of Code Project Demo Day 2023, Where Contributors like me Showcase Amazing Projects they have been working on under Coding Period. 
  <p align = "center" > <strong>Tap to View </strong></p>
<p align="center">
       
<a href="https://www.youtube.com/watch?v=G1fZBqy5jp8">
<img src="http://img.youtube.com/vi/G1fZBqy5jp8/0.jpg">
 </a>
</p>

## 📦 Deliverables

1.  **OnInstallation Message from Marketplace:** When users install the Notion App from the RocketChat Marketplace, they receive a welcome message that introduces the features and further using guide of the integration.

2.  **Helper Message:** Users can access a helper message with usage instructions by typing `/notion help`. This message provides guidance on how to use various commands and features.

3.  **Smooth Authorization with Notion:** Users can seamlessly connect their Notion account to the RocketChat workspace using the `/notion connect` command. Similarly, they can disconnect using the `/notion disconnect` command, ensuring privacy and security.
    
4.  **Manage Multiple Notion Workspaces and Switch Between Them:** Users can manage and switch between Notion workspaces using `/notion workspace` or `/notion ws` within RocketChat. This allows teams with different projects to collaborate effectively by connecting the appropriate Notion workspace.
    
5.  **Create a Page or Record:** Users can create new Notion pages or records directly from RocketChat using the `/notion create` command. This streamlines the process of initiating new collaborative documents.
    
6.  **Create Notion Database:** Teams can create new Notion databases using the `/notion create db` command. This enables structured data storage and management within Notion for efficient collaboration.
    
7.  **Sharing Notion Page:** Users can easily share Notion pages with their teammates using the `/notion share` command. This ensures that relevant information is quickly accessible to the right people.

### 📝 **Extra Features or Features Which was Reevaluated:**
    
8.  **Comment On Page:** Teams can add comments to Notion pages directly from RocketChat using the `/notion comment` command. This feature encourages discussions and annotations within the context of the shared documents.
    
9.  **Viewing Shared Notion Page:** Users can view shared Notion pages within RocketChat, even if they don't actively participate. This ensures that important information is readily available to everyone.
    
10.  **Preserve Message in Notion Page (Optional New Page Structured within a Database:** Users can choose to preserve RocketChat messages within a Notion page, structuring it within a database or while creating new task. This feature ensures that valuable discussions, decisions, and insights are captured in the appropriate context for future reference.

11. **View Notion Table and Update Database Entries:** Teams can view Notion database tables and update entries using the `/notion view` command. This facilitates collaborative data management without leaving RocketChat.

## 📺 Demo 
### 1. OnInstallation Message from Marketplace:

Once the app is installed from the marketplace and enabled for use, users will automatically receive a helper notification in the direct room that provides simple and user-friendly instructions on how to use the integration.


https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/f8ce0b29-095b-4f84-884a-e26c0df36136


### 2. Helper Message:

The `/notion help` command serves as a valuable command for users who might require a Quick Refresher. This command ensures that users can easily retrieve essential information, providing a convenient way to use App. 

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/ae120c49-cbcc-48d7-ab33-17d764fe5902

### 3. Smooth Authorization with Notion: 
The smooth authorization process for accessing and manipulating Notion pages and databases within a specific workspace directly from Rocket.Chat involves OAuth2 Notion Authorization.  user can connect to workspace using `/notion connect` and When a user wishes to disconnect from a workspace, they can simply run the `/notion disconnect` command.
- The implementation of this feature have been done using backward compatible approach and not using the Apps Engine framework's due to some limitations in Notion OAuth2 handling. Notably:
    1. **Basic HTTP Authentication**: Notion recommends using Basic HTTP Authentication during the access_token request.
    However, the Apps Engine OAuth2Client may not support this functionality at present.
    2. **Credential Format**: Notion advises providing credentials in the form of `Basic CLIENTID:CLIENTSECRET` in base64 format,
    which might not be fully supported by the Apps Engine OAuth2Client.
    3. **Extra Fields**: Notion integration requires additional fields in persistence storage,
    demanding customization of the Apps Engine to accommodate these fields.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/580f1165-fc1f-4ca2-be1f-3d507ff4f314
    
### 4. Manage and Switch Between Workspace: 
The `Manage and Switch Between Workspace` feature enables users to switch between previously connected workspaces without the need to fully disconnect from their current workspace. This smooth transition between different workspaces enhances productivity by eliminating interruptions in workflow and mitigates the risk of confusion and errors that may result from working in the wrong workspace.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/a23e9be0-0187-4292-a498-c400235bb84d

### 5. Create a Page Or Record:

The ability to create Notion pages or records directly from RocketChat via integration offers users remarkable convenience. For example, imagine a project discussion taking place in a RocketChat channel. With this feature, a team member can instantly initiate a new Notion page to capture meeting notes, action items, and decisions within the same conversation flow. This streamlined process eliminates the need to switch between platforms, empowering users to seamlessly document and collaborate in real-time, thus enhancing efficiency and knowledge retention.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/bd90bf55-5ee6-45e4-b7f0-febc02f2a6db

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/21a453e3-87b3-4d6f-8bd5-01ad9ba3cf92

### 6. Create Notion Database:

Enabling users to create Notion tables directly from RocketChat through integration provides a valuable tool for organized data management. For instance, consider a project manager coordinating tasks in a RocketChat workspace. With this feature, the manager can effortlessly generate a structured Notion table to track project milestones, deadlines, and responsible team members, all within the familiar chat environment. This seamless process enhances task tracking and collaboration, ensuring that vital project details are systematically recorded and easily accessible, thereby promoting efficiency and informed decision-making.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/b1b7a020-ce59-441c-a529-bb0f92d965a4

### 7. Share Notion Page: 
Sharing Notion pages directly from RocketChat via App offers users a streamlined approach to disseminate information and collaborate effectively. For instance, envision a team discussing a marketing campaign in a RocketChat channel. Using this feature, a team member can instantly share a relevant Notion page containing campaign details, strategies, and visuals without leaving the conversation. This seamless sharing enhances communication by providing context-rich information, minimizing the need for context-switching between platforms. As a result, teams can make informed decisions swiftly, boosting alignment and driving projects forward efficiently.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/322e7775-e500-400c-9c56-4f7002116bab

### 8. Comment On Page: 
The ability to comment on Notion pages directly from RocketChat offers users a powerful tool for collaborative discussions. For example, picture a design review discussion happening in a RocketChat channel. Utilizing this feature, team members can provide feedback, suggestions, and insights directly on a shared Notion page dedicated to the design. This seamless process keeps conversations and feedback contextualized within the project's documentation, fostering efficient communication and informed decision-making. As a result, teams can iterate and refine their work effectively, ensuring alignment and accelerating project progress.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/08728dde-4e35-45a3-8d88-58680ce7f8d2

### 9. View Shared Notion Page: 
Viewing shared Notion pages from RocketChat via integration empowers users with immediate access to critical information, bolstering collaboration and decision-making. For example, imagine a team member reviewing a Notion page shared in a RocketChat channel, outlining intricate project details. By effortlessly viewing this page within the same chat environment, the user gains a comprehensive understanding of the campaign's scope, goals, and strategies. This eliminates the need to navigate to a separate platform, ensuring focused discussions and enabling quicker consensus-building. Ultimately, this feature enriches engagement and accelerates project momentum by consolidating information within the conversation space.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/befbff18-3dd7-4575-a4e3-7cdbd3d4f532

### 10. Preserve Message in Notion Page:
#### Preserve in Existing Page:
Preserving RocketChat messages within an Existing Notion page through integration offers users a powerful means of capturing discussions and decisions seamlessly. For instance, envision a team collaborating on a product roadmap in a RocketChat channel. By utilizing this feature, team members can ensure that their valuable insights, brainstorming, and decisions are directly integrated into the associated Notion page. This functionality fosters a continuous record of thought processes and aligns discussions with documented outcomes, promoting transparency and informed actions. As a result, users can easily trace the evolution of ideas, keeping everyone on the same page and promoting a culture of inclusivity and efficiency.
#### Preserve in New Page:
Preserving RocketChat messages within a new Notion page or while creating entries in a database through integration offers users a powerful way to capture and contextualize discussions. For instance, imagine a project team discussing feature enhancements in a RocketChat channel. With this feature, users can effortlessly generate a dedicated Notion page or database entry linked to the ongoing conversation. This ensures that vital insights, decisions, and references are recorded alongside the relevant discussion, enhancing accountability and knowledge retention. This functionality establishes a dynamic repository that aligns communication with documentation, enabling teams to refer back to discussions and fostering collaboration with clarity and efficiency.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/d01a927c-f296-49a2-97ca-11be8c9cd498

### 11. View Notion Table: 
Viewing Notion tables directly within RocketChat through integration offers users a valuable tool for data analysis and collaboration. For example, consider a sales team tracking leads and conversions in a Notion database. By accessing and viewing this table within a RocketChat channel, team members can quickly assess sales trends, monitor progress, and discuss strategies without leaving the chat environment. This streamlined approach enhances real-time decision-making and encourages collaborative insights, minimizing the need for platform-switching. Ultimately, this feature empowers teams to stay informed and aligned, fostering efficient teamwork and informed actions.

https://github.com/Nabhag8848/Google-Summer-of-Code/assets/65061890/36a5e89f-4ed6-42e0-b503-2729e334a045

### Upcoming Feature:
- Certainly, the ability to Update Notion tables directly from RocketChat remains an upcoming feature within the integration. This enhancement will allow users to make changes and modifications to Notion tables seamlessly after the initial creation. While this functionality falls under the category of extra features rather than deliverables, it promises to provide users with an extended capability to manage and edit data within the integrated workspace. This feature aligns with the integration's focus on streamlining collaboration and boosting productivity by maintaining consistent access to, and manipulation of, crucial information.

## 🚀 Contributions
### Pull Requests

<div align="center">

| PR Link   | Description  | Status | 
| :-----------: | :------------------------------------:| :------:|
| [PR #2](https://github.com/RocketChat/Apps.Notion/pull/2) | <b> [CHORE] Initialise Notion App</b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #3](https://github.com/RocketChat/Apps.Notion/pull/3) | <b> [CHORE] Add Bug & Feature Forms Including PR Template </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #5](https://github.com/RocketChat/Apps.Notion/pull/5) | <b> [Feat] Notion Authorization with Rocket.Chat </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #14](https://github.com/RocketChat/Apps.Notion/pull/14) | <b> [Feat] Create Notion Database From RocketChat For Properties Without Configuration  </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #15](https://github.com/RocketChat/Apps.Notion/pull/15) | <b> [Feat] Create Notion Database From RocketChat For Properties Includes Configuration   </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #17](https://github.com/RocketChat/Apps.Notion/pull/17) | <b> [Feat] Provide Helper Message on /notion help having Commands as Attachment </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #18](https://github.com/RocketChat/Apps.Notion/pull/18) | <b> [Feat] Provide Helper Message OnInstallation of App </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #19](https://github.com/RocketChat/Apps.Notion/pull/19) | <b> [Feat] Comment on Notion Page </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #20](https://github.com/RocketChat/Apps.Notion/pull/20) | <b> [Feat] Create Notion Page From RocketChat  </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #21](https://github.com/RocketChat/Apps.Notion/pull/21) | <b>  [Feat] Change Between Workspace </b>  | <img src="https://i.imgur.com/tskv8MM.png" width=55 height=40> |
| [PR #22](https://github.com/RocketChat/Apps.Notion/pull/22) | <b>  [Feat] Create Notion Record From RC </b>  | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40> |
| [PR #24](https://github.com/RocketChat/Apps.Notion/pull/24) | <b>  [Feat] Share Docs and Intiaitives From RC </b>  | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40> |
| [PR #26](https://github.com/RocketChat/Apps.Notion/pull/26) | <b>  [Feat] Preserve RocketChat Message in New and Existing Notion Page </b>  | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40> |
| [PR #28](https://github.com/RocketChat/Apps.Notion/pull/28) | <b>  [Feat] View Notion Table inside RC </b>  | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40> |
| [PR #30](https://github.com/RocketChat/Apps.Notion/pull/30) | <b>  [DOCS] updated readme to include setup and general info about app </b>  | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40> |
| [PR #31](https://github.com/RocketChat/Apps.Notion/pull/31) | <b>  [Feat] View Notion Page Inside RocketChat Channel  </b>  | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40> |

</div>

### Issues
    
<div align="center">
    
| Issue Link   | Description  | Status | 
| :-----------: | :------------------------------------:| :------:|
| [ISSUE #1](https://github.com/RocketChat/Apps.Notion/issues/1) | <b>[CHORE] Add Template of Opening Feature Request and Bug Issues</b> | <img src="https://i.imgur.com/ihaDyZS.png" width=55 height=40>
| [ISSUE #4](https://github.com/RocketChat/Apps.Notion/issues/4) | <b>[Feat] Notion Authorization with Rocket.Chat</b> | <img src="https://i.imgur.com/ihaDyZS.png" width=55 height=40>
| [ISSUE #6](https://github.com/RocketChat/Apps.Notion/issues/6) | <b>[Feat] Create Notion Database From RocketChat</b> | <img src="https://i.imgur.com/ihaDyZS.png" width=55 height=40>
| [ISSUE #7](https://github.com/RocketChat/Apps.Notion/issues/7) | <b>[Feat] Provide Helper Message on /notion help </b> | <img src="https://i.imgur.com/ihaDyZS.png" width=55 height=40>
| [ISSUE #8](https://github.com/RocketChat/Apps.Notion/issues/8) | <b>[Feat] Provide Helper Message OnInstallation of App</b> | <img src="https://i.imgur.com/ihaDyZS.png" width=55 height=40>
| [ISSUE #9](https://github.com/RocketChat/Apps.Notion/issues/9) | <b>[Feat] Comment on Notion Page</b> | <img src="https://i.imgur.com/ihaDyZS.png" width=55 height=40>
| [ISSUE #11](https://github.com/RocketChat/Apps.Notion/issues/11) | <b>[Feat] Change Between Workspace</b> | <img src="https://i.imgur.com/ihaDyZS.png" width=55 height=40>
| [ISSUE #10](https://github.com/RocketChat/Apps.Notion/issues/10) | <b>[Feat] Create Notion Page and Record</b> | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40>
| [ISSUE #16](https://github.com/RocketChat/Apps.Notion/issues/16) | <b>[Feat] Gitpodify App with Updates in ReadME </b> | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40>
| [ISSUE #23](https://github.com/RocketChat/Apps.Notion/issues/23) | <b>[Feat] Share Docs and Intiaitives From RC </b> | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40>
| [ISSUE #25](https://github.com/RocketChat/Apps.Notion/issues/25) | <b>[Feat] Preserve RocketChat Message in New and Existing Notion Page </b> | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40>
| [ISSUE #27](https://github.com/RocketChat/Apps.Notion/issues/27) | <b>[Feat] View Notion Table inside RC </b> | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40>
| [ISSUE #29](https://github.com/RocketChat/Apps.Notion/issues/29) | <b>[Feat] View Notion Page Inside RocketChat Channel </b> | <img src="https://user-images.githubusercontent.com/70485812/189489748-ed27630f-36e7-4eb9-a9a4-e082d6894490.png" width=55 height=40>

</div>

## 🔜 Whats Next ?
I plan to continue enhancing the integration by focusing on two key features. Firstly, I'll be working on implementing the `Update Table Entries` feature, which will empower users to modify and manage data within Notion tables directly from RocketChat. This aims to provide a comprehensive data manipulation capability, enhancing the integration's practicality. Additionally, I'll be involved in shifting the Notion Page Markdown conversion to a NPM module. This transition will streamline the process of converting content from Notion pages to markdown, ensuring efficiency and compatibility and I'm excited to contribute to its continued evolution beyond the GSoC period.

## 🙌🏼 Mentors

I would like to express my heartfelt gratitude to [Bárbara Zanella](https://www.linkedin.com/in/barbara-zanella/) and [Samad Yar Khan](https://www.linkedin.com/in/samad-yar-khan/), my exceptional mentors throughout this project journey. Their unwavering support and guidance have been instrumental in shaping my growth. With their insightful guidance, we held two productive meetings each week, a testament to their commitment. Their encouragement to step beyond conventional boundaries has truly been transformative, pushing me to explore innovative solutions. From enhancing user-centric aspects to intricate technical implementations, their mentorship covered every aspect. In the face of diverse challenges at every juncture, their expertise helped us conquer each obstacle with determination.

![Team(1)](https://github.com/Nabhag8848/GoogleSummerOfCode/assets/65061890/e33b8b4c-598d-40e8-978a-b0ad4414a23f)

I Extend my sincere thanks to Sing Li and the community for their invaluable contributions. Their insights and alerts on project direction have been invaluable, enhancing the project's usability. The continuous feedback loop created by this collaborative effort has been pivotal in our project's evolution. Without this constant stream of input, our progress would not have been as remarkable. I am truly grateful for the guidance and support provided by both my mentors and the community, as they have been pivotal in making this journey an enriching and successful one.

## 👤 About Me

I'm Nabhag, a final-year Computer Engineering student from India, driven by a deep passion for Engineering. Beyond my academics, I'm devoted to crafting Plugins and Integrations that seamlessly connect various products, resulting in substantial impacts. I’m an active Contributor in the Rocket.Chat Apps Community, and I firmly believe in transparently sharing my learning journey and progress. This involvement has opened doors to exciting opportunities, allowing me to shape platform integrations and extensions. Every Hackathon fuels my passion for designing innovative plugins, while my broader focus extends to creating developer tools and products that enhance the overall developer experience. Embracing the world of open source empowers me to work on projects close to my heart. While my primary identity revolves around being an OpenSource Contributor, I've also had the honor of taking part in Google Summer of Code, which has added another layer of enrichment to my journey.

## 🛤️ My Journey

My journey in the world of technology has been quite a ride. It all began with me diving into C++ programming and exploring the intricacies of Data Structures and Algorithms during my degree course. Initially, programming felt like a foreign concept, but I gradually picked up the ropes. However, I soon felt a sense of monotony and decided to switch to Java when I couldn't find exciting projects within the realm of C++. As I delved into Java, I started creating small console applications, only to realize that I wasn't making much progress.

Then, a game-changer entered the scene: [WeMakeDevs](https://wemakedevs.org/) Community introduced me to the concept of **Learning in Public** and the intriguing challenge of **100DaysOfCode**. This was my gateway to the world of Full Stack Development. Embracing this approach, I began sharing my daily learning experiences on Twitter. Thankfully, through the 100DaysOfCode Challenge, I connected with like-minded individuals who shared my passion.

As I continued, I found myself gravitating towards Backend Engineering. However, I realized that I was stuck in a cycle of endlessly learning without any concrete application and missing real users. Seeking a breakthrough, I embarked on an internship with a fintech startup. Here, I was responsible for crafting an Investing Monitoring Tool that offered real-time analytics for trading Crypto using a blend of WebSockets, Angular, and NestJS. This was a pivotal moment as it marked the first time I developed something truly useful for users.

As my journey progressed, I became intrigued by the inner workings of communication protocols and the world of open-source software. My curiosity led me to participate in HacktoberFest, where I started trying to contribute to various organizations. Eventually, I stumbled upon RocketChat Apps, which opened up a new dimension of integration. This was exciting and novel, and I immersed myself in the Apps ecosystem. It was a joyous achievement when my pull request was merged into the Rocket.Chat repository, becoming a part of the Rocket.Chat 6.0 Release.

Joining Rocket.Chat came with a learning curve. Unexpectedly, my open-source journey paved the way for Google Summer of Code (GSoC). While I hadn't initially planned for it, the contribution mindset propelled me forward. I felt drawn to GSoC's mission of introducing more people to open-source, which led me to craft a proposal for Integrate Notion via RC App, just days before the deadline. It was a whirlwind of activity, including Creating a Figma design within a week. Miraculously, my proposal was accepted, bringing an indescribable sense of joy.

Transitioning into a Google Summer of Code Student was enlightening. As my mentor rightly said, getting selected is one challenge, but making the project a success requires relentless effort. The coding period had its share of ups and downs. Early on, we developed features, but they lacked a user-centered approach. The turning point arrived with valuable feedback from the community. This feedback reshaped our project into a more user-centric one, even though the challenges escalated.

The journey has been nothing short of a rollercoaster. We tackled seemingly impossible features within tight deadlines, all while dealing with Notion's limitations. This experience has been amazing and has firmly rooted me in the world of open-source. Once you dive in, there's no looking back. This is a journey I'm truly passionate about. If you're interested in venturing into open-source, feel free to connect with me on any of my social media platforms mentioned below.

## 💬 Connect With Me
<div align="center">

| **Student** | Nabhag Motivaras |
|:--------------------|:-------------------|
| **Organization** | [Rocket.Chat](https://rocket.chat/) |
| **Project** | [Integrate Notion Via RC App](https://summerofcode.withgoogle.com/programs/2023/projects/9v76k7Q8) |
| **GitHub** | [@Nabhag8848](https://github.com/Nabhag8848) |
| **LinkedIn** | [Nabhag Motivaras](https://www.linkedin.com/in/nabhag-motivaras-460b3b1aa/) |
| **Email** | <a href="mailto:nabhagmotivaras76@gmail.com">nabhagmotivaras76@gmail.com</a> |
| **Rocket.Chat** | [nabhag.motivaras](https://open.rocket.chat/direct/nabhag.motivaras) |
       
</div>



