<figure markdown>
  ![Image title](./images/title_light.png#only-light){ width="750" }
  ![Image title](./images/title_dark.png#only-dark){ width="750" }
</figure>


# Foreword

This is a self-study guide for computer science in the AI era, as well as a record of my four-year self-study journey in college.

This is also a gift dedicated to computer technology students worldwide. If this guide can provide even the slightest help, it will be a great encouragement and comfort to me.

The book currently includes the following sections (if you have better suggestions or want to join as a contributor, feel free to email me at [su2489544776@outlook.com](mailto:su2489544776@outlook.com) or open an [Issue](https://github.com/George-102/ai-cs-guide/issues)):

- **Usage Guide**: Given the vast resources covered in this book, I have developed corresponding usage guides based on different groups' available time and learning goals.
- **AI-CS Learning Plan**: A comprehensive and systematic self-study plan for CS in the AI era.
- **Essential Tools**: An introduction to AI-CSer efficiency tools such as Git, GitHub, Docker, Vim, LaTeX, GNU Make, VS Code, WSL, Oh My Zsh, Obsidian, and more.
- **Classic Book Recommendations**: Struggling with obscure textbooks? Don't blame yourself — the textbooks might just be poorly written. Anyone who has read CSAPP will appreciate the importance of good books. I will list must-read books and resource links across various CS fields.
- **High-Quality CS Courses**: I will categorize and compile **high-quality** CS courses from both domestic and international sources, including those I have attended and those contributed by the open-source community. I will introduce course characteristics and provide self-study suggestions. Most courses will have dedicated repositories with resources and assignment implementations.

## Where the gears start to turn — Buildathon

When I enrolled, I was a complete novice in computer science. Apart from playing computer games, I couldn't even download proper software. Yet, I embarked on my CS journey with curiosity and enthusiasm. Every day, I would attend classes punctually, listen attentively, take notes, and complete assignments. However, I gradually realized that each teacher had a different style, pace, emphasis, and level of enthusiasm. Some merely recited from outdated slides; others randomly called on students to answer questions from those same slides. Very few truly invested their passion in encouraging students to think critically. My enthusiasm was gradually eroded...

I had thought my university life would be uneventful — classes, study, entertainment. Within two months, DeepSeek emerged. Initially, I didn't think much of it, seeing it as just another all-purpose tool. I continued studying textbooks in the traditional order of CS fundamentals. It wasn't until I was about to enter my second year that I realized the profound changes in our field. While learning remains important, the landscape of knowledge has transformed dramatically. From DeepSeek to agents, skills, and RAG — new concepts and disciplines have quietly emerged. From traditional manual coding to today's AI-assisted programming and Vibe Coding, CS education has undergone a profound revolution.

Because of this, I found myself in confusion. I even doubted whether I was cut out for computer science. The childhood fantasies I had about being a geek were completely shattered by my first year. I often asked myself: given AI's capabilities, what knowledge should I master? Do I still need to learn Java and Python? Do I still need to study data structures and computer networks?

The turning point came at the end of my freshman year. I stumbled upon a keynote speech by Andrew Ng at the inaugural Buildathon, covering AI-assisted programming, rapid product prototyping, and the skill requirements for AI engineers. This speech truly pointed me in the right direction. I went to YouTube to watch the entire speech. The moment I finished, it was like Columbus discovering a new continent — I had opened the door to a new world.

In Andrew Ng's speech, I summarized several key ideas:

- **"Move fast and take responsibility."** AI-assisted programming accelerates independent prototype development by 10x. The dramatic reduction in prototype costs makes rapid, repeated trial-and-error a viable strategy. The real value lies in discovering projects worth deep development through experimentation.

- **Code is depreciating — developers must transition to system designers and AI commanders.** Programming tools have evolved through multiple generations: from GitHub Copilot to IDEs, then to highly agentized coding assistants. The speed of tool iteration creates substantial efficiency gaps — being half a generation behind can significantly impact output. The value of code itself is decreasing. AI can automatically generate code and migrate database architectures, making architectural decisions more reversible. Developers need to shift from code writers to system designers and AI commanders, focusing on core architecture and composite system construction.

- **"No need to learn programming in the AI era" is the worst career advice ever.** Andrew Ng strongly opposes this view, pointing out that every advancement in programming tools has historically enabled more people to acquire programming skills. The CFO, legal counsel, and front desk staff in his team have all improved efficiency by learning programming. The core skill of the future is "precisely telling the computer what to do," which requires understanding computer languages and programming logic. Non-technical personnel can quickly master basic programming through AI assistance, achieving cross-domain efficiency improvements.

- **AI engineers are in acute shortage, yet university courses have become severely outdated.** The unemployment rate among CS graduates has risen to 7%, yet enterprises still face a severe shortage of AI engineers. The core contradiction lies in university courses failing to cover key skills: AI-assisted programming, LLM API usage, RAG/Agentic workflow construction, and standardized error analysis processes. Emerging AI engineers need three major skills: using the latest AI programming tools, familiarizing themselves with AI building blocks (prompt engineering, evaluation techniques, MCP), and possessing rapid prototyping capabilities with basic product intuition.

Later, I followed Professor Ng's advice and started self-studying in these directions. I gradually gave up attending university classes and found many high-quality online courses. In such courses, you don't need to worry about anything — just work hard, be serious, and spend time. The frustration of being unable to put energy to use in class, and the feeling of getting no return despite putting in effort, disappeared completely. This suited me perfectly, and I fell in love with self-study.

If you are also struggling with learning computer science and share the same frustrations, watch Professor Andrew Ng's [Buildathon speech](https://youtu.be/kjg45_5WhqI?si=lcWv2E-pLhF-5StY) — that's where the gears of my destiny began to turn.

## Why was this guide written

During my sophomore fall semester studying operating systems, I found the lectures extremely boring — many examples were from ten years ago, and the lab manuals were from 13 years. In conversations with friends, I sensed their concerns about AI's rapid development and anxiety about future job prospects. By then, I had been self-studying for over a year and had compiled many resources, which I shared with friends. After all, who doesn't want to enjoy university while securing a good job or getting into graduate school?

With another year of accumulation, the resources became quite comprehensive, covering most courses in CS, AI, and software engineering. I created individual GitHub repositories for each course, compiling self-study materials and homework implementations. When calculating credits later, I opened my training program and realized it was already a subset of my self-study repository — only two years after I started. A bold idea emerged: perhaps I could create a self-study training program, recording the pitfalls and paths from my three years of self-study, combined with my thoughts on the AI era, to contribute my humble efforts to future CSers.

## Self-study or not?

The greatest advantage of self-study is the ability to adjust your learning pace entirely on your own terms. You can alter your study plan at any time, following your own progress rather than being confined to the training program and classroom.

Another benefit is learning from diverse sources. The first time I installed a dual-boot system, I made a mistake and erased my Windows. Fortunately, I had no valuable data. Later, I learned that modern SSDs don't completely erase data — as long as the new system doesn't occupy the original disk space, recovery is possible. It's precisely these trial-and-error experiences that allow me to continuously learn knowledge I wouldn't otherwise encounter.

The third advantage is time freedom. University life is inherently flexible, and self-study lets you arrange your own schedule. With proper time management, you can pursue self-study while still achieving good grades.

Are there downsides to self-study? Of course — every coin has two sides.

The first drawback is communication difficulty. The problems you encounter may not be shared by others, nor may they interest them. However, by asking questions on platforms like Google, StackOverflow, and AI, you can solve 90% of your problems. The second drawback is that many high-quality resources are in English, but translation software and plugins have largely solved this. The third and most difficult challenge is self-discipline. Without deadlines, it's truly terrifying. As content deepens and difficulty increases, persisting through an entire course is grueling. You need enough drive to force yourself to focus, understand thousands of lines of code, and endure hours of debugging — all without credits, grades, teachers, or classmates. Just one belief: you are getting stronger.

## Who is this book written for?

As I mentioned in the foreword, anyone aspiring to learn and master computer knowledge in the AI era can refer to this book. If you already have a CS foundation and are interested in a specific field, feel free to selectively study the content that interests you. Of course, if you're a complete novice like I was when I first entered university, I hope this book serves as your guide, helping you acquire the necessary knowledge and skills in the shortest time. In some sense, this book is more like a course search engine sorted by my experience, helping everyone experience high-quality CS courses without leaving home.

## Special Thanks

With deep reverence, I sincerely thank all the professors and developers who have made their course resources freely available. These courses embody decades of teaching dedication, yet they chose to selflessly share such high-quality CS education with everyone. Without them, my university life would not have been so fulfilling and joyful. Many professors, after receiving my thank-you emails, responded with hundreds of words — truly moving. They constantly inspire me: do things well, whether it's learning, research, or being a person.

## Join as a contributor

One's strength is ultimately limited. This book was written in my spare time after staying up late amidst heavy research, so imperfections are inevitable. Additionally, since I specialize in computer applications, many courses emphasize practical applications with less focus on mathematics, theoretical CS, and advanced algorithms. If you have rich self-study experience in other fields, feel free to submit a Pull Request or contact me via email ([su2489544776@outlook.com](mailto:su2489544776@outlook.com)).

## About study groups

This book supports page commenting. If you want to self-study a particular course, create a group chat (QQ or WeChat) and post a comment below the corresponding course page, specifying your learning goals and how to join. Additionally, many friends have established study groups in Issues — feel free to join them directly.

## Buy the author a coffee

This book is completely open-source and free. If you find this project helpful, consider giving the repository a star or buying the author a coffee.

<figure markdown>
  ![Image title](./images/sponsor.jpg){ width="500" }
</figure>
