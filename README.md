# Mastering-MCP-Beginner-to-Pro-Across-the-AI-Ecosystem-Notes
This Repository contains my "Mastering MCP: Beginner to Pro Across the AI Ecosystem" Course Notes from Udemy

**I) Introduction**

**A) Title - Introduction to MCP**

**B) What is MCP ?**

**C) What is a Model ?**

**D) What is Context ?**

**E) What is a Protocol ?**

**F) Demo: Something that we shall build together**

**G) History & Transition to MCP**

**H) Key Features & Benefits of MCP**

**I) A Quick intro to Anthropic & Claude**

**J) Why the mention of Anthropic for MCP**

**K) Adoption by Big Vendors**

**L) How is it trending on Github Stars**





# **I) Introduction**

# **A) Title - Introduction to MCP**

Just a music about "Introduction to MCP"

# **B) What is MCP ?**

So, let's try and address the $1 million question — the reason why you are here, or why you actually enrolled in this course. The question is: What is MCP, or the Model Context Protocol? Let’s take a look.

MCP is an open protocol — that’s very important. It is a protocol that standardizes how applications or AI systems provide context to Large Language Models (LLMs). Now, when we talk about two things — “MCP is open” — it means that it is publicly accessible and free. It is vendor-neutral, which means it provides interoperability across different environments. You can use it with Microsoft, Azure, AWS, or even with blockchain frameworks. Being vendor-neutral, it ensures flexibility and avoids vendor lock-in.

It is also community-driven. As an open standard, MCP encourages contributions from the developer community. Moreover, it provides a standardized integration framework, offering a universal way to connect AI systems to external data sources. This is very important — you are connecting your AI applications to external data sources seamlessly.

Now, you might have heard people say: “Think of MCP like a USB-C port for AI applications.” Initially, I used to read that and get confused about how exactly to explain it. So, I started looking into what USB-C actually does and why it was created.

Initially, we had many different types of cables — Type A, Type B, Type C, and even proprietary ones like Apple’s Lightning cable. The problem was that you needed different cables for different devices. Then came the concept of USB-C. The beauty of USB-C is that you just need one cable that can connect to a wide variety of devices — phones, laptops, cameras, and more. That’s its magic: one universal connector for everything.

Now, they’re saying: think of MCP like a USB-C port for AI applications. Let’s understand that analogy.

If you look at this figure (mentally visualize it), it shows the world without MCP. In that world, everything runs on APIs. You would have different APIs — a Google API, a Calendar API, a Slack API, and so on. Each of these APIs has its own structure, authentication, and quirks. So, just imagine a developer having to create integrations with all these different third-party APIs. It’s like having to keep different cables for different devices — tedious and inconsistent. While you can run AI applications this way, it’s challenging because the developer must code a lot of integration logic for each API.

Now, what does MCP do here?
In our analogy, consider your laptop as a model — think of it as a large language model. Then your MCP is like your USB-C connector or adapter. Into this adapter, you can plug different MCP servers. Every vendor — like Gmail, Slack, or WhatsApp — that previously had its own APIs, now provides an MCP server. All you need to do is bring in that server and plug it into the MCP adapter. Once done, your AI application can communicate with it seamlessly.

At the top, if you visualize, the model (LLM) connects to the MCP, and you plug various MCP servers into it. These servers translate the model’s generic requests into specific API calls required to interact with external tools. That’s the power of MCP.

So, MCP provides a standard way to connect AI models to different data sources and tools. You can connect not just to third-party APIs, but also to databases, internal systems, and more. It acts as a universal bridge between your LLM and external information sources.

This open standard was developed by Anthropic, one of the key contributors to the AI ecosystem. We’ll dive deeper into that later.

Now, let’s understand why MCP came into existence. MCP provides a growing list of pre-built integrations that your LLM can directly plug into. Every major vendor is now building MCP-compatible servers. A great example is Azure — it has introduced Azure MCP servers. With these, you no longer need Terraform or complex setup scripts. You can simply use Azure MCP and interact in natural language with your cloud resources. We’ll explore this in more detail later.

Another key benefit is flexibility — MCP allows you to switch between LLM providers and vendors easily because it is vendor-neutral. Today you might be using LangChain, tomorrow Azure, and the next day AWS — all of them can interoperate because they agree to follow the MCP protocol.

Finally, the best part is that MCP uses industry best practices for securing your data within your infrastructure. So, you don’t need to worry about data exposure when integrating with different tools.

Don’t worry if you’re still a bit confused — we’ll do a deep dive into MCP soon. We’ll break it down step by step: what is a model, what is context, and what is a protocol — and then we’ll connect it all to truly understand what the Model Context Protocol is all about.

# **C) What is a Model ?**

As we are starting with the Model Context Protocol (MCP), I always like to begin by breaking things down into their root words. I tell my daughter the same thing — whenever you’re studying a subject, try to deconstruct it and look at its basic components. That’s exactly what we’re going to do here.

The very first root word is “Model.”
Now, you might be wondering — what exactly is a model? In the world of AI, a model is like a smart brain. It’s a brain that has been trained to perform a specific task — such as understanding text, recognizing images, or making decisions.

So, when we talk about models, we’re really talking about these intelligent systems that have learned from data to perform well-defined functions. You must have heard of many machine learning models out there, and they all follow the same fundamental idea.

When it comes to models, I always tell everyone to remember the two P’s — Pattern and Prediction.
These two are key, especially in the predictive side of AI (not yet in the generative side). Data always has patterns hidden within it. What a model does is it studies these patterns and then uses that knowledge to make predictions.

In other words, the model learns the patterns from large amounts of data and then uses that understanding to answer questions or predict outcomes. That’s what the two P’s stand for — Pattern and Prediction — study the pattern, make the prediction.

Let’s look at some examples of models you might already be familiar with.

Take a House Price Prediction Model, for instance. If you input the square-foot area of a house, the model should be able to tell you the approximate price of that property. Here, the model is learning the relationship between house size and price — studying the pattern to make a prediction.

Another common one is the Spam vs. Not Spam model, which is a classifier. When you receive an email, platforms like Gmail use such models to analyze its content and decide whether it should go to your inbox or the spam folder. Again, it’s identifying patterns in the text to make a predictive decision.

A third example can be seen on platforms like Udemy or Netflix. For instance, if someone purchases a course from me on Udemy, the system’s recommendation model might show, “These are three other courses that are often bought together.” It’s using clustering techniques to group similar user behaviors and suggest relevant items. This again is a model at work — analyzing data patterns to make useful predictions.

At the end of the day, all these are models — whether they’re predicting house prices, classifying emails, or recommending courses.

However, what we are really interested in here is the Large Language Model (LLM) — the “L” in MCP.

By now, everyone has heard of large language models like ChatGPT, Claude, or Gemini. These are advanced AI models that provide the generative capabilities of artificial intelligence.

A Large Language Model is an advanced type of AI trained on a massive corpus of text data to understand, generate, and manipulate human language. It uses deep learning techniques, most notably the transformer architecture, to perform complex tasks such as translation, summarization, question answering, and conversation — all with remarkable fluency and contextual awareness.

So, remember — an LLM is a specific kind of model designed for understanding and generating language. Of course, models can also be built for images, videos, and other modalities — but in our case, we’re focusing on language.

So, now that we’ve clearly understood what a model is, we’ll move on to the next key concept: Context.

# **D) What is Context ?**

After having a good look at what a model is, it’s now time to take a closer look at the next important part — context.

Now, what does context actually mean?
If we think about it in simple English, context refers to the situation, background, or surrounding information that helps you understand the meaning of something.

For example, imagine you’re having a conversation with someone and they suddenly start talking about something without any explanation. Naturally, you’d say, “Wait, give me some background.” You’d want to understand the situation or scenario first — and that background information is what we call context.

To understand context even better, let’s look at a simple example. Suppose you ask someone, “What’s the capital?” The other person might respond, “That’s a very weird question — you haven’t given me the context.” And they’d be right! Without context, they don’t know which capital you’re referring to.

But if you say, “I’m planning a trip to France — what’s the capital?” then you’ve provided the context. You’ve given background information — that you’re talking about France — which helps the other person understand your question correctly. So, context provides clarity and relevance by giving additional information around a topic.

Now, when we bring this idea into the world of AI and talk about models, specifically LLMs, the question becomes: what kind of context are we passing to these models?

Remember, the Model Context Protocol (MCP) standardizes how AI models interact with external tools and data sources by defining certain key components. Don’t worry — we’ll dive deeper into each one soon. But broadly, these components are: tools, resources, and prompts.

Let’s start with tools.
You can think of tools as functions or actions that the AI model can invoke. Examples include querying a database, sending an email, creating a document, or performing an API call. Every MCP server will have its own specific set of tools that it can perform.

Next, we have resources.
Resources are the structured, often read-only data or content that the AI model can access. These could include files, database views, or API endpoints — essentially, any source of information the model might need to refer to while performing its task.

And finally, we have prompts — something most of you are already familiar with.
When you interact with ChatGPT, for instance, you’re providing prompts. These are predefined templates or workflows that guide how the AI model interacts with data or tools. Prompts can combine resources and tools together to help the model perform more complex, multi-step tasks effectively.

By organizing the context into these components — tools, resources, and prompts — MCP enables AI models to interact with external systems in a structured and standardized manner.

So remember, by leveraging MCP’s standardized approach to context, AI models can perform tasks much more effectively. They can access and manipulate relevant information as needed — securely and efficiently.

In summary, when we talk about the “context” in Model Context Protocol, we’re referring to these structured elements — tools, resources, and prompts — that together define how an AI model interacts with the world around it.

Don’t worry if this still feels a bit abstract — we’ll do a deeper dive into each of these components in the upcoming lectures.

# **E) What is a Protocol ?**

Right, so we’ve looked at Model, and we’ve looked at Context. Now it’s time to take a look at the final piece — Protocol.

So, what exactly is a protocol?
A protocol is nothing but a set of rules — a simple set of rules or instructions that you have to follow.

For example, if somebody says “Hi,” you respond with “Hello.” If someone says “Hello,” you might say “Hi there.” You wouldn’t respond with something totally unrelated — that would be going against the protocol. So, in essence, a protocol defines a consistent way of interaction.

Now, let’s take this idea into the world of machines — how do machines talk to each other?
Machines, just like humans, also follow protocols. There are many different types of them. For instance, you might have heard of SSH, HTTP, or TCP — all of these are examples of protocols.

So, in simple terms, a protocol is a set of rules or instructions that tell different systems how to communicate or work together.

If you visualize it, you’ll see there’s a sender on one side and a receiver on the other. The sender is communicating with the receiver, and both are following a specific protocol to make sure the information is transferred correctly and consistently.

Now, when we talk about protocols in the context of MCP (Model Context Protocol), what does that mean?

In this case, the protocol in MCP refers to an open specification — something that is publicly accessible and free for anyone to use. It is vendor-neutral, which means it’s not tied to any one company or provider. Major technology vendors like Microsoft, AWS, Oracle, and many others have adopted the MCP standard, ensuring broad compatibility across platforms.

MCP also follows a client-server architecture. This is very important. You’ll often hear the terms MCP Client and MCP Server. Don’t worry — we’ll do a deeper dive into this architecture later. But for now, just remember: this protocol ensures consistent implementation by following the client-server model.

That means, no matter where in the world someone is working on MCP — whether it’s a developer in the U.S. or a company in India — everyone follows the same structure: there must be a client and a server.

This standardized design helps with reducing duplication. You might recall the earlier example of third-party APIs — where every API had its own keys, authentication mechanisms, and unique integration logic. Developers had to spend enormous effort building and maintaining all those individual integrations.

MCP solves that problem. It eliminates redundant integration efforts, allowing developers to plug into standardized MCP servers instead of writing custom code for every API.

Another major advantage is that MCP supports ecosystem development. Because it’s an open, shared standard, it enables global growth and collaboration around a common framework. Developers, organizations, and vendors all know exactly what rules to follow, making it easier to build, scale, and connect systems together.

So to summarize:
A protocol is simply a set of rules or instructions that define how different systems talk to each other or work together. And that’s exactly what the “P” in Model Context Protocol stands for.

With this, I think you now have a clear understanding of what Model, Context, and Protocol each mean — and why they come together beautifully under the term MCP: Model Context Protocol.

Hats off to the brilliant mind who coined this term — it perfectly captures the essence of how modern AI systems communicate and interact.

# **F) Demo: Something that we shall build together**

Now I'd like to give you a quick snippet of what we shall be building together. I’m saying “building together”, so I will be with you all throughout the process. I would encourage you all to actually work along with me, and wherever you have any issues, feel free to ask questions. I’ll be there helping you in real time.

The first thing to remember with MCP (Model Context Protocol) is that it is LLM agnostic and AI framework agnostic. That’s why, as part of this lecture series, I’ve tried to touch upon every popular framework and LLM that is widely used today. You’ll see examples using Gemini, OpenAI, Azure OpenAI, and others. MCP was originally introduced by Anthropic, and we’ll cover cloud, desktop, and very popular frameworks like LangChain, which we’ll work on together. We’ll also work with LlamaIndex and Google’s Agent Development Kit, along with OpenAI’s Agent SDK.

This sounds very exciting! We’ll explore different use cases, various LLMs, and frameworks. Here’s a quick summary of what we’ll cover:

First, we’ll look into Cloud Desktop, where enabling MCP is very straightforward. I’ll show you a snippet where you simply ask, “Give me the most expensive product and its price.” Behind the scenes, the MCP server writes the SQL for you automatically—you don’t have to write it. We’ll do this together, including the Python code needed. Here, the user communicates in natural language with an SQLite MCP server that talks to an SQLite database, using LangChain to orchestrate it.

Next, we’ll explore LlamaIndex. In this example, instead of Gemini, we’ll use Azure OpenAI. You’ll see how you can ask it to, for instance, “Write me a story or poem and store it on my desktop.” ChatGPT can’t do this directly, but with MCP, it’s possible—restricted only to directories you allow, without touching the rest of your file system.

Then, we’ll explore Azure MCP server. With this, you no longer need Terraform to query your Azure resources. You can simply ask questions like, “Show me the resources or resource groups in my subscription,” using OpenAI’s Agent SDK with Azure MCP server.

To make things more interesting, we’ll integrate PayPal to create invoices using natural language. You’ll be surprised at how you can generate a new invoice on your PayPal account simply by asking for it. This is done through PayPal’s MCP server, combined with Gemini or any other LLM you choose.

Finally, we’ll explore Google’s Agent Development Kit (SDK). This recent addition from Google allows you to perform tasks like creating invoices in natural language format.

Initially, we’ll cover some theory and architecture, which is very important. Then, we’ll proceed step by step: starting with Cloud/Desktop as a no-code option, and then moving into more coding-focused approaches with Python.

# **G) History & Transition to MCP**

Hello and welcome. In this lecture, we'll take a look at the transition to MCP, outlining the evolutionary journey from using standalone LLMs to adopting the Model Context Protocol (MCP), which is a structured approach for integrating LLMs with real-world tools, services, and databases.

So, how did this all start? Initially, we had an LM, which stands for Large Language Model. Here we are talking about models like ChatGPT, LLaMA, and Gemini. At that point, we were quite happy giving a prompt to the LM, such as “Hey ChatGPT, can you write me a story?” or “Can you write me a poem?” or “Can you summarize this text for me?” This was the most basic setup. In this scenario, the LM operated independently without access to external tools or data sources.

However, the problem with this setup was its limitations due to the trained data. LLMs were trained up to a certain time period, for example, December 2023 or 2024, which meant they could not provide information about recent events or real-time data. So, if you wanted insights based on recent information, standalone LLMs were unable to help.

Then came the concept of LM plus tools. OpenAI introduced a concept called function calling, which allowed LLMs to connect to external tools—potentially dozens of them. This marked the start of primitive agentic behavior, where the LM could invoke external functions or tools to get information. For instance, asking “What is the current weather in London?” would trigger a third-party API call. LongChain also provided similar functionality under its tool-use framework. While this enabled LLMs to interact with live data, it had its limitations. Integrating multiple APIs required a lot of coding, and these integrations were often hard-coded or tightly coupled, making it difficult to scale or standardize. If a developer had to integrate ten different APIs, this became a significant challenge.

To address these limitations, the concept of MCP (Model Context Protocol) was introduced. Here, the LM no longer talks directly to the services. Instead, it communicates via the MCP, which acts as a gateway or bridge between the LM and the backend services. This MCP architecture decouples the LLM from backend logic, enabling standardization, reusability, scalability, and enhanced agentic behavior. Essentially, the LM sends requests through the MCP, which then orchestrates communication with the appropriate service. This way, the LM does not need to know the specifics of each backend service, making the overall system much more modular and maintainable.

Over time, this architecture evolved further. Your computer now acts as an MCP host, which communicates with multiple MCP servers using the MCP protocol. For example, you can have an Azure MCP server, a PayPal MCP server, and others like OCI or Oracle. Each MCP server handles a specific resource or service, such as a database or third-party API, and knows how to interact with it. The MCP host orchestrates these interactions, ensuring that the LM can interact with live databases, APIs, and other systems in a controlled, observable, and secure manner.

The main outcome of this evolution is that LLMs can now interact with live services in real-time without being tightly coupled to each backend system. MCP provides a standardized bridge between LLMs and real-world resources, enabling scalable, reusable, and secure integration. This transition from standalone LLMs to MCP-enabled LLMs allows us to combine the power of language models with real-world tools, APIs, and databases in a seamless way.

I hope this gives you a clear understanding of how we moved from standalone LMs to LM + tools, and finally to LM + MCP interacting with live services. Thanks for watching.

# **H) Key Features & Benefits of MCP**

Hello and welcome. In this lecture, we'll take a look at the features and benefits of MCP and understand why it has become so important and popular. We'll go through each feature one by one.

The first feature is standardized integration. Previously, before MCP, developers had to write a lot of code to integrate LLMs with third-party APIs or tools. This involved specifying metadata for each tool and writing custom code for each integration. With MCP, a universal protocol or set of rules was established to connect models to external data. Industry leaders like Microsoft, AWS, and Oracle agreed on this standard, which simplifies development and avoids the need for custom connectors. Developers no longer need to build integration logic from scratch, saving significant time and effort.

Next, MCP provides a plug-and-play architecture. It follows a simple client-server setup where an MCP client communicates with an MCP server. The server could be a file system, Azure, or other service MCP server. When testing MCP, it becomes evident how flexible it is—if you change the MCP server in the configuration JSON, the system works without major modifications. This flexibility enables faster setup and deployment.

Another critical benefit is enhanced security. MCP employs OAuth authentication and token-based verification to ensure secure access to MCP servers. Data is protected with end-to-end encryption using TLS or SSL. MCP also emphasizes explicit user consent for data access and tool execution. For example, when connecting Claude Desktop to a file system MCP server, the user is prompted to grant permission before access is allowed. This ensures secure, compliant, and trustworthy interactions.

MCP also addresses the limitations of LLMs regarding real-time data. Traditional LLMs are trained up to a specific time period, meaning they cannot provide recent or live information. With MCP, LLMs can fetch up-to-date information by connecting to databases or APIs. For example, you can query a SQLite database or fetch the current weather in London. This capability boosts the relevance of responses, making the output much more useful and accurate.

A significant advantage of MCP is interoperability. MCP supports working across AI models, platforms, and frameworks. This means code written for OpenAI can also work in Gemini, LangChain, LlamaIndex, or Azure OpenAI. This cross-platform and cross-framework support ensures MCP can operate in diverse environments without requiring major code changes.

Another major benefit is reduced hallucinations. Generative AI models often produce hallucinated responses because they rely solely on their training data. MCP mitigates this by providing access to structured, factual data from external sources, such as databases and APIs. This significantly reduces misinformation and improves the reliability of responses.

Finally, MCP supports agentic workflows, which are becoming increasingly important in the era of AI agents (2025–2026). MCP enables multi-step tasks where one agent can interact with another agent or external service. It allows complex automation and multitasking by orchestrating interactions between LLMs and third-party data sources. This enhances automation and the capabilities of AI systems.

In summary, MCP provides standardized integration, plug-and-play architecture, enhanced security, access to real-time data, interoperability across platforms, reduced hallucinations, and supports agentic workflows. These features make MCP a powerful framework for extending the capabilities of LLMs in a structured, secure, and scalable way. In the upcoming sessions, we will deep dive into coding and no-code exercises to better understand MCP and its practical applications.

# **I) A Quick intro to Anthropic & Claude**

If we are studying MCP, it becomes quite important to understand Anthropic and Claude, as many people often get confused between the two. So let’s clarify this first. Anthropic is a company, similar to OpenAI. Just as OpenAI created ChatGPT, Anthropic, which is an AI research and product-based company, created a product called Claude. It is crucial to distinguish clearly between the company (Anthropic) and the product (Claude).

I always recommend visiting the Anthropic website at anthropic.com to read more about their work. They focus on AI safety and responsible AI, and they also have an Anthropic Academy, similar to OpenAI Academy, for learning purposes.

Looking at their products, the main offering is Claude. Just like OpenAI has ChatGPT, Anthropic has Claude. Unlike OpenAI, which has a wide range of models like GPT-3.5, GPT-4, GPT-4-turbo, and more (O1, O3, etc.), Anthropic has kept things relatively simple. The Claude model family is structured to scale intelligence and cost in a straightforward way.

The Claude models are named based on concepts from English literature: Haiku, Sonnet, and Opus.

Haiku is the smallest and fastest model, analogous to a three-line poem. It is lightweight and economical.

Sonnet is in the middle—offering a balance of performance and speed, similar to a 14-line structured poem.

Opus is the most advanced, designed for complex and creative tasks, akin to a full creative work.

The Claude model family emphasizes security, trustworthiness, and reliability, which is similar to claims by other AI companies. Each model in the family is optimized for different levels of performance and use cases, allowing users to select based on their needs for speed, intelligence, or creativity.

In the next lecture, I will explain why we are discussing Anthropic and Claude in the context of MCP and how it fits into our learning path.

# **J) Why the mention of Anthropic for MCP**

So now, the question that might be coming to your mind is: “Hey, we have actually subscribed to the MCP course, so why are they talking to us about Anthropic Cloud? We are not interested in that.” But the thing is, Anthropic is the company that actually created MCP, the Model Context Protocol. Back in November 2024, Anthropic released MCP and even made it open source, understanding that this is the future of AI applications. A lot of people talk about MCP as just hype, but it is not—it is genuinely the future.

MCP is described as an open standard for connecting AI assistants to the systems where data lives. This includes everything we learned about tool calling: talking to databases, file systems, multiple servers, and more. Previously, developers had to write extensive code or call third-party APIs to achieve this functionality, but now MCP simplifies the entire process.

Reading further, MCP is described as an open standard that enables developers to build two-way connections between data sources and AI-powered tools. MCP introduces three major components for developers. The first is the Model Context Protocol specification and SDK. By accessing this, you can see that the Python SDK is available, and for our course, we will be using Python for all our work. SDKs are also available in other languages like TypeScript, so developers have flexibility depending on their environment.

The second component is local MCP server support in the Cloud Desktop app. MCP is baked directly into the cloud chatbot, acting as a client. This allows you to connect to various servers, such as a SQLite database or a file system, and interact with them via natural language. We will work hands-on with these in the course.

The third component is the open-source repository of MCP servers, which is where the magic happens. There are many reference servers available, and the list is growing every day. During the course, we will work with several of these, including SQLite and file system servers, and we might also explore some GitHub examples.

Additionally, Azure has recently introduced its own MCP server, allowing you to interact with Azure cloud services in a natural language format. This demonstrates the increasing adoption and importance of MCP across ecosystems. You can also install pre-built MCP servers through the Cloud Desktop app and follow the Quick Start guide, making it easy to start building right away.

So, the main takeaway from this lecture is: Anthropic and Cloud are important because Anthropic created MCP and made it open source, providing a standardized, scalable, and secure way for AI assistants to interact with real-world data and systems. In the next lecture, we will see how other companies have quickly started adopting MCP into their ecosystems.

# **K) Adoption by Big Vendors**

So guys, no one is actually stopping you from creating or designing a protocol. Remember, a protocol is simply a set of rules that everyone has to adhere to. However, the success of any protocol always depends on how widely it is adopted.

Now, you might be wondering: if Anthropic introduced MCP in November 2024, what was the adoption like? You’ll be surprised—it spread like wildfire. All the big companies started adopting it very quickly. For example, by April 2025, OpenAI and Microsoft had already announced support for MCP. They confirmed that their AI agents would integrate MCP, and OpenAI began working on their Agents SDK, which included MCP support.

Amazon was also an early adopter. By the end of April 2025, Amazon announced that their Amazon Q Developer CLI would support MCP. This demonstrates how rapidly major tech companies recognized the importance of MCP. Even though MCP was created by Anthropic—a competitor to ChatGPT and Amazon Bedrock—these companies understood the potential of MCP and incorporated it into their own stacks. They realized that MCP would be the future of AI applications, especially for interacting with third-party APIs or accessing external data sources like SQLite, Oracle, SQL Server, or others.

By April 2025, Azure not only adopted MCP but also created its own MCP server. This shows that adoption wasn’t just passive—they saw the value and invested in building their own infrastructure. The list of MCP servers is growing day by day. Amazon provides Knowledge Base Retrieval, and Azure now has its own server, among many others. These servers simplify operations—developers no longer need Terraform or complex code to list Azure Storage, Cosmos DB, or other resources.

In this course, we will explore this practically, doing deep dives into the code and working hands-on with these MCP servers. For now, the key takeaway is how quickly and widely MCP was adopted, and why it is considered a fundamental technology for the future of AI applications.

# **L) How is it trending on Github Stars**

A lot of times, people ask me how they can check the popularity of any open-source software or technology. If you are learning something new, you may want to see how widely it is being adopted. One of the best ways to check this is by looking at the GitHub star history.

If you search on Google for “GitHub star history,” you will find a website called StarHistory.com. On this site, you can enter the repository name and even compare multiple repositories. When I was creating this course, I wanted to check the popularity of MCP, because so many people were talking about it. I was genuinely surprised by what I saw.

For example, the pink graph represents Lama Index, which is a very popular framework in the AI world, just after LangChain. Its star history shows a gradual increase over time. The purple graph represents LangGraph, another popular LangChain framework, which sits around 10K stars. The blue graph is OpenAI’s Swarm, also around 20K stars. The yellow graph shows MetaLLaMA, which is widely known but still around 10K stars.

Now, look at MCP—the red graph representing the Model Context Protocol servers repository. Its growth is explosive, like a rocket. Since its launch in November 2024, the trajectory has been almost vertical. By 2025, it has already crossed 50–60K stars, which is far higher than many older frameworks. The only project that could potentially catch up is A2A, Google’s Agent-to-Agent protocol, but for now, MCP clearly dominates in popularity.

If we align the timeline, we can see that MCP achieved this level of adoption extremely quickly. Compare this to other frameworks that started in 2022 or 2023, and it’s clear why MCP has generated so much interest. This rapid adoption is precisely why this course exists—to help you understand MCP in depth and see how it works under the hood.
