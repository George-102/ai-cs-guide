<figure markdown>
  ![Image title](./images/title_light.png#only-light){ width="750" }
  ![Image title](./images/title_dark.png#only-dark){ width="750" }
</figure>

# Foreword

This is a self-study guide for computer science in the AI era, as well as a record of my four-year self-study journey in college.

This is also a gift dedicated to computer technology students worldwide. If this guide can provide even the slightest help to everyone, it will be a great encouragement and comfort to me.

The book currently includes the following sections (if you have better suggestions or want to join the contributors,Welcome to email [su2489544776@outlook.com](mailto:su2489544776@outlook.com) or ask questions in [issue](https://github.com/George-102/ai-cs-guide/issues):

- Usage Guide for this Book: Given the vast resources covered in this book, I have developed corresponding usage guides based on different groups of people's free time and learning goals.
- A comprehensive and systematic AI-CS learning plan for reference: I have developed a comprehensive and systematic self-study plan for computer science (CS) in the AI era based on my own experience.
- Essential Tools: An introduction to some AI-CSer efficiency tools, such as IDEs, VPNs, StackOverflow, Git, GitHub, Vim, LaTeX, GNU Make, Docker, workflows, and more.
- Classic book recommendation: Are you struggling with the obscurity and confusion of textbooks? Don't look for reasons within yourself, it may just be that the textbooks are poorly written. Those who have read CSAPP will surely appreciate the importance of good books. I will list and recommend must-read books and resource links in various computer science fields.
- **Compilation of high-quality CS courses at home and abroad**: I will categorize and compile **high-quality** CS courses from both domestic and international sources, including those I have attended and those contributed by the open-source community. I will introduce the characteristics of their course content and provide corresponding self-study suggestions. Most courses will have a separate repository to maintain related resources and assignment implementations for everyone to learn and reference.

## Where the gears start to turn - Buildathon

When I enrolled, I was a complete novice in computer science. Apart from playing computer games, I couldn't even download proper software. Yet, I embarked on my journey in computer science with curiosity and enthusiasm. Every day, I would punctually attend classes, listen attentively to the teacher's lectures, take notes, and complete assignments. However, I gradually realized that each teacher had a different teaching style, pace, emphasis, and enthusiasm. Some merely recited from outdated PowerPoint presentations, while others merely added the step of randomly selecting students to answer questions on the slides. Very few truly invested their passion in education to encourage students to think critically. My enthusiasm was gradually eroded... I had thought my university life would be uneventful, consisting mainly of classes, studies, and entertainment. Within two months, DeepSeek emerged. Initially, I didn't think much of it, seeing it as just another all-purpose tool that could assist me. I continued to study the textbooks in the usual order of the four major components of computer science. It wasn't until I was about to enter my second year that I finally realized the significant changes in my major. While learning remains important, the professional knowledge has undergone tremendous changes. From DeepSeek, to later agents, skills, and RAG, new concepts and disciplines have quietly emerged. From traditional manual code development to today's AI-assisted programming and Vibe Coding, computer science education has undergone profound changes.

Because of this, I once found myself in a state of confusion. I even doubted if I was cut out for studying computer science. The childhood fantasies I had about being a geek were completely shattered by my experience during my first academic year. I often ask myself, given AI's capabilities, what knowledge should I master? Do I still need to learn Java and Python? Do I still need to study data structures and computer networks?

The turning point came at the end of my freshman year. I stumbled upon a keynote speech given by the renowned Andrew Ng at the inaugural Buildathon, which revolved around AI-assisted programming, rapid development of product prototypes, and the skill requirements for AI engineers. This speech truly guided me towards my direction in studying computer science. I went to YouTube to watch the entire speech of Andrew Ng. The moment I finished watching it, it was like Columbus discovering a new continent - I had opened the door to a new world.

In Andrew Ng's speech, I summarized several key ideas:

- **"Act swiftly and take responsibility"**. AI-assisted programming accelerates independent prototype development by 10 times. The significant reduction in prototype costs makes rapid and multiple trial-and-error feasible, and the true value lies in discovering projects worthy of in-depth development through trial and error.

- **Code is depreciating, and developers need to transition to becoming system designers and AI commanders**. Programming tools have undergone multiple generations of evolution: from GitHub Copilot to IDEs, and then to highly agentized programming assistants. The speed of tool iteration creates substantial efficiency gaps, and being half a generation behind can significantly affect output capabilities. The value of code itself is decreasing. AI can automatically generate code and migrate database architectures, making architectural decisions more reversible. Developers need to transition from code writers to system designers and AI commanders, focusing on controlling core architecture and building composite systems.

- "No need to learn programming in the AI era" is the worst career advice ever. Andrew Ng strongly opposes the view that "there is no need to learn programming in the AI era", pointing out that every advancement in programming tools in history has enabled more people to acquire programming skills. The CFO, legal advisor, and front-end personnel in his team have all improved their work efficiency by learning programming. The core skill in the future is to "precisely tell the computer what to do", which requires understanding computer language and programming logic. Non-technical personnel can quickly master basic programming skills through AI assistance, achieving cross-domain efficiency improvement.

- **AI engineers are in acute shortage, yet university courses have become severely outdated**. The unemployment rate among computer science graduates has risen to 7%, yet enterprises still face a severe shortage of AI engineers. The core contradiction lies in the failure of university courses to promptly cover key skills: AI-assisted programming, large language model invocation, RAG/Agentic workflow construction, and standardized error analysis processes. Emerging AI engineers need to master three major skills: using the latest AI programming tools, familiarizing themselves with AI building blocks (prompt engineering/evaluation techniques/MCP), and possessing rapid prototyping capabilities and basic product intuition.

  

Later, I followed the advice given by Professor Andrew Ng and started self-studying in these directions. I gradually gave up attending university classes, and during this period, I found many high-quality online courses. In such courses, you don't need to worry about anything; all you need to do is work hard, be serious, and spend time. The feeling of being unable to put your energy to use in the classroom, and the feeling of not getting any return despite putting in more time, disappeared completely. This was perfect for me, and I fell in love with self-study from then on.

If you are also unhappy about learning computer knowledge and share the same troubles as me, you might as well watch Professor Andrew Ng's speech at [Buildathon](https://youtu.be/kjg45_5WhqI?si=lcWv2E-pLhF-5StY), because that's where the gears of my destiny began to turn.

## Why was this guide written

During my sophomore fall semester when I was studying computer operating systems, I found the lectures extremely boring, and many of the examples used were from ten years ago. The lab manuals were even from 13 years ago. Later, in conversations with friends, I could sense their concerns about the rapid development of AI and anxiety about future job prospects. At that time, I had been self-studying for over a year and had compiled a lot of resources, which I shared with my friends. After all, who doesn't want to enjoy their university years while also securing a good job or getting admitted to graduate school?

But with another year of accumulation, the content of the resources has become quite rich, covering most courses in computer science, artificial intelligence, and software engineering. I have also created individual GitHub repositories for each course, compiling the self-study materials and homework implementations I have used. When calculating my credits later, I opened my training program and realized that it was already a subset of my self-study repository, and this was only two years after I started self-studying. Therefore, a bold idea emerged in my mind: perhaps I could create a self-study training program, recording the pitfalls and paths I encountered during my three years of self-study, and combining my own thoughts on the AI era, in the hope of contributing my humble efforts to future CSers.

## Self-study or?

The greatest advantage of self-study lies in the ability to adjust the learning pace entirely according to one's own schedule. You can alter your study plan at any time. Follow your own progress, rather than being confined to the training program and classroom.

Another benefit of self-study is learning from others' strengths. The first time I installed a dual operating system on my laptop, I made a mistake and erased my Windows. Fortunately, I didn't have any valuable data. Later, I learned that modern solid-state drives (SSDs) don't completely erase data. This means that the data might not be completely overwritten. As long as my new system doesn't occupy the original disk space, I might be able to recover the data in the unused space. It's precisely these trial and error experiences that allow me to continuously learn various knowledge that I wouldn't ordinarily encounter.

The third advantage of self-study is the freedom of time. University life is inherently relatively free, and self-study allows one to arrange their own study time and plans. As long as the time is properly arranged, you can still achieve good grades while pursuing self-study.

Is there any downside to self-study? Of course, every coin has two sides.

The first disadvantage of self-study is the inconvenience of communication. The problems you encounter may not necessarily be encountered by others, nor may they interest others. However, by being adept at asking questions on platforms such as Google, Stack Overflow, and AI, I believe you can solve 90% of your problems. The second disadvantage is that many high-quality courses and resources are in English, but I believe this is no longer a difficult problem to solve. Nowadays, translation software and plugins have almost perfectly solved this problem. The third and most difficult issue is self-discipline. For self-study, not having a deadline (DDL) is truly terrifying. As the learning content deepens, the difficulty of learning also increases, and it can be quite torturous to persist through the entire course. You have to have enough motivation to force yourself to settle down, understand thousands of lines of code frameworks, and endure hours of debugging. And all of this without credits, grades, teachers, or classmates, with only one belief - you are getting stronger.

## Who is this book written for? Who is this book written for

As I mentioned in the preface, anyone aspiring to learn and master computer knowledge in the AI era can refer to this book. If you already have a certain foundation in computer science and are merely interested in a specific field, you can selectively choose the content you are interested in for learning. Of course, if you are a novice who knows nothing about computers, just like I was when I first entered university, I hope this book can serve as your guide, allowing you to acquire the necessary knowledge and skills in the least amount of time. To some extent, this book is more like a course search engine sorted according to my experience, helping everyone experience high-quality computer courses without leaving home.

## Special Thanks

Here, with a heart filled with reverence, I sincerely thank all the professors and developers who have made their course resources freely available. These courses and resources embody the accumulation and dedication of their decades-long teaching careers, yet they have chosen to selflessly share such high-quality CS education with everyone. Without them, my university life would not have been so fulfilling and joyful. Many professors, after receiving my thank-you emails, would even respond with hundreds of words, which truly touched me. They also constantly inspire me to do things well, whether it's learning, research, or being a person.

## You also want to join the ranks of contributors

One's strength is ultimately limited. This book was written by me in my spare time after staying up late amidst heavy scientific research, so it is inevitable that there may be imperfections. Additionally, as I specialize in computer applications, many courses emphasize practical computer applications, with relatively less emphasis on mathematics, theoretical computer science, and advanced algorithms. If any experts wish to share their self-study experiences and resources in other fields, they can directly initiate a Pull Request in the project. They are also welcome to contact me via email ([su2489544776@outlook.com](mailto:su2489544776@outlook.com)).

## Regarding the establishment of the communication group

This book supports page commenting functionality. Therefore, if you want to self-study a certain course, you can create a group chat (either on QQ or WeChat) and post a comment below the corresponding course page, specifying your learning goals and the way to join the communication group. In addition, many friends have already established similar group chats in the issue, and you can choose to join them directly.

## Want to treat the author to a cup of afternoon tea

The content of this book is completely open-source and free of charge. If you find this project genuinely helpful to you, you can give the repository a star or treat the author to a cup of afternoon tea.

<figure markdown>
  ![Image title](./images/sponsor.jpg){ width="500" }
</figure>

