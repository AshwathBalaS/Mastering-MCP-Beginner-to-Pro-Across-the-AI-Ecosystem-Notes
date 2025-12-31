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

**II) MCP Architecture and Components**

**A) Intro - MCP Architecture**

**B) Core Architecture of MCP**

**C) Key Components- Deep Dive**

**D) What is JSON-RPC 2.0**

**E) MCP Transport Layer**

**F) Transport Mechanism - STDIO**

**G) Transport Mechanism - SSE**

**H) Transport Mechanism - Streamable HTTP**



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

# **II) MCP Architecture and Components**

# **A) Intro - MCP Architecture**

In this module, we’re diving into the beating heart of MCP—its architecture and transport mechanisms. This is where everything comes together and you truly understand how MCP enables models to interact with their runtime environments.

We’ll start by looking at the MCP architecture. MCP isn’t just another protocol; it’s a flexible, modular bridge between models and the systems they operate in. Its design allows models to communicate in a structured, extensible, and transport-agnostic way.

At its core, MCP follows a client–server architecture. The MCP client sends a request enriched with contextual information. The MCP server receives this request, processes it using a structured format—most commonly a JSON-RPC 2.0 message—and then returns a well-defined response back to the client.

Next, we’ll take a deep dive into the key components of MCP. You can think of MCP as being built from three essential building blocks. First is the MCP server, which hosts the model or action logic. Second is the MCP client, responsible for sending requests and handling responses. Third is the transport layer, which governs how data flows between the client and the server.

We’ll explore each of these components in detail, helping you understand not just how they work, but also how you can implement your own MCP pipeline from scratch.

Starting with JSON-RPC, we’ll see how MCP leverages JSON-RPC 2.0—a lightweight protocol for remote procedure calls using JSON—to ensure consistent, structured communication between systems.

Then we’ll move on to the MCP transport layer, which answers a crucial question: how do these requests and responses actually move between the client and the server?

MCP doesn’t lock you into a single transport mechanism. It supports multiple options, starting with stdio (standard input/output). This is a simple and fast way for two processes to communicate, especially when they’re running on the same machine.

We’ll also discuss Server-Sent Events (SSE)—sometimes referred to as TSS—which allows the server to push real-time updates to the client over HTTP. While powerful, this approach may be deprecated in the future.

Finally, we’ll cover the recommended approach: Streamable HTTP. This is a robust and scalable option designed for stateless, web-based interactions. It’s particularly well-suited for production-grade systems, and we’ll even build an MCP server using Streamable HTTP in our hands-on demo.

By the end of this module, you won’t just understand how MCP is built and how it communicates. You’ll also be confident in designing and implementing your own transport-aware MCP applications.

# **B) Core Architecture of MCP**

First and foremost, remember that MCP follows a client–server architecture. It’s a simple and intuitive setup: you have a client, and you have a server. This structure forms the foundation of how MCP works.

By now, you should already know that MCP is a way for tools—such as AI assistants—to interact with structured data sources using a consistent and secure protocol. One important thing to note is that this entire architecture can run locally on your own computer. The client–server model does not strictly require the internet. Connecting to internet-based remote services is optional, not mandatory.

In other words, even though MCP supports remote services, the same client–server interaction can happen entirely on your local machine. This makes MCP both flexible and powerful.

Now let’s walk through the process step by step.

In step one, a tool with an MCP client initiates a request. This “host with an MCP client” represents tools such as cloud desktops or IDEs like Visual Studio Code, Cursor, or Windsurf. These tools must be MCP-compliant, which is very important. Being MCP-compliant means they know how to send structured queries or commands using the MCP protocol.

As you already know, the MCP protocol itself is built on JSON-RPC, which ensures that requests are structured, predictable, and standardized.

In step two, the MCP client sends the request to the MCP server using the MCP protocol. This protocol acts as a bridge between the client and the server. It provides a standardized way to query or access different data services.

Based on the request, it is routed to the appropriate MCP server. For example, if you ask, “Write me a poem and store it on my desktop,” the system knows it needs to communicate with a file system MCP server. If instead you ask for information about storage accounts in your Azure subscription, the request is routed to an Azure MCP server.

There is typically a one-to-one relationship between an MCP server and the data source it manages. MCP Server A might be connected to local data source A and handle all operations related to that data. MCP Server B could be connected to a different local database. MCP Server C might represent a remote service, acting as a bridge between local tools and external web APIs.

In the case of remote services, the MCP server communicates with external APIs over the internet, fetches the required data, and then relays the response back through the MCP protocol.

Once the request reaches the correct MCP server, the server executes the query or action. Each server accesses its designated data source. Local data sources are queried directly, while remote data sources are accessed via API calls.

After execution, the results flow back in the opposite direction. The data is returned from the data source to the MCP server, and then from the MCP server back to the MCP client. This two-way communication ensures that the client receives the final result in a structured and usable form.

This entire process enables the tool or assistant to understand, analyze, and act on data effectively. The client might summarize results, analyze logs, store files, or generate helpful responses based on the returned data.

To summarize, the MCP client acts as the requester—typically a tool or assistant. The MCP servers act as responders, each fetching or operating on data from their designated sources. The MCP protocol provides a standardized communication format between clients and servers. Finally, the data sources themselves can vary widely, ranging from local file systems and databases to third-party APIs.

With this, you should now have a clear understanding of how MCP operates using a client–server architecture.

# **C) Key Components- Deep Dive**

In the previous video, we established that MCP follows a client–server architecture. Now, we will take a deeper dive into this architecture to understand the key components involved and how they interact with each other.

The diagram discussed explains the MCP architecture by breaking it down into the roles of the MCP client and the MCP server, and how they communicate through three core components. These three components are tools, resources, and prompts. We will go through each of these in detail.

At a high level, let us first look at the MCP client. You can think of the MCP client as an AI agent that interacts with a language model (LM). The MCP client is responsible for interacting with the outside world or the application. It does this by invoking tools, meaning it can call specific tools and knows which tool to use when needed. The client has enough intelligence to determine the appropriate tool to invoke.

In addition to invoking tools, the MCP client can also query resources. This is useful when you want to read data from a database or communicate with a specific MCP server. The client can also interpolate prompts, which means it can automatically fill in prompt templates. These are the primary responsibilities handled by the MCP client.

Next, we look at the MCP server, which represents the application side of the architecture. The MCP server exposes functionality to the client. Traditionally, companies exposed APIs, but with MCP, there is a shift toward exposing MCP servers instead of APIs. This shift is significant because MCP servers expose tools, which are essentially functions that the model can invoke directly.

The MCP server also exposes resources, which are structured data assets that the model can query. In this relationship, the server exposes resources while the client consumes them. Similarly, the server exposes prompt templates, and the client fills in these prompts. This is how the MCP client and MCP server communicate with each other.

When we examine the components in more detail, the first component is tools. Tools are model-controlled, meaning the language model decides when and how to invoke them through the MCP client. Tools are simply functions that the model can execute. Examples include retrieving or searching for documents, finding relevant data, sending messages such as emails or notifications, or even updating records in a database. All of these actions are performed through tools invoked by the model.

The second component is resources, which are application-controlled. Resources are data assets exposed to the model by the application. While the model can query these resources, they are still managed and structured by the server. The server remains in control of the data, and the model only consumes it.

Examples of resources include files such as documents and spreadsheets, database records containing structured data, and even responses from third-party APIs. For instance, a weather API or any external service can act as a resource, providing live or stored data that the model can analyze.

The third component is prompts, which are user-controlled. Prompts are predefined templates that guide the model’s behavior and instructions. They provide structured and consistent interactions. Examples include question-and-answer templates, prompts for extracting information from documents, or prompts for summarizing meetings or conversations. Prompts help enforce consistency in how the model responds.

The output generated through MCP follows a structured format, typically using JSON, as defined by the JSON-RPC protocol. This ensures that responses are consistent and machine-readable.

Looking at the overall flow, the MCP server defines and exposes tools, resources, and prompts. In this sense, it replaces the traditional API layer. The MCP client, often acting as an AI agent, accesses the server. Based on the user’s goal or input, the model performs three key actions: it selects or fills in a prompt, queries relevant resources, and invokes appropriate tools.

This approach creates a structured and secure interaction model. The application remains in control of what the model can access and what actions it can perform. At the same time, the model retains autonomy in reasoning and decision-making, using only what is exposed through the MCP protocol.

If this feels too deep or complex right now, the key takeaway is simple: MCP uses a client–server architecture where the server exposes tools, resources, and prompts, and the client consumes and uses them alongside a language model to generate responses.

As mentioned, upcoming demos and deeper dives will make this architecture much clearer and help solidify your understanding of how MCP works in real-world scenarios.

# **D) What is JSON-RPC 2.0**

MCP stands for Model Context Protocol. In the initial lectures, we discussed what a protocol is, and we agreed that a protocol is essentially a set of rules. This naturally leads to the next question: what protocol does MCP use under the hood?

Under the hood, MCP makes use of JSON-RPC. To understand this, we first need to understand what JSON is. JSON stands for JavaScript Object Notation. It is a lightweight data interchange format that is based on JavaScript syntax but is language-independent. This means JSON can be used in any programming language such as Python, Java, or C#. Because of its simplicity and flexibility, JSON is widely used for data exchange in APIs, configuration files, and databases.

JSON-RPC builds on top of JSON. It is a lightweight remote procedure call (RPC) protocol encoded in JSON. RPC stands for Remote Procedure Call, which allows a client or programmer to call functions or procedures that exist on another system. In other words, you are invoking a function remotely, which is why it is called a remote procedure call. JSON handles the data format, and RPC handles the function invocation.

MCP specifically uses JSON-RPC version 2.0, which is the most widely adopted and improved version of the protocol. JSON-RPC 2.0 introduced several important enhancements over version 1.0. These include notifications, which are requests that do not expect a response, batch processing, and standardized error handling. JSON-RPC 2.0 is lightweight, language-agnostic, and designed specifically for client–server communication, which aligns perfectly with the MCP architecture.

The protocol is lightweight because it has minimal overhead and uses pure JSON. It is language-agnostic, meaning it works with any programming language that supports JSON, such as Java, C#, or Python. It follows the client–server model, where one side sends requests (the client) and the other side sends responses (the server). This makes it ideal for cloud applications, APIs, and inter-service communication.

Now let’s look at the key features of JSON-RPC. First, it uses JSON as the data format for both requests and responses. All communication—sending requests and receiving responses—is done using JSON. This ensures consistency and simplicity.

JSON-RPC supports requests, notifications, and batch requests. A request expects a response, such as calling a function and receiving a result. A notification, on the other hand, is a “fire-and-forget” call where no response is expected. Notifications are often used for logging or progress updates.

Every JSON-RPC request includes a method name. The method represents the function being invoked. Requests may also include optional parameters, which are the inputs to the method. Additionally, each request contains an ID, which uniquely identifies the request. This ID is extremely important because it must match between the request and the corresponding response. The ID allows the client to associate a response with the original request.

Responses in JSON-RPC contain either a result or an error object. If the method call succeeds, the response includes the result. If the call fails, the response includes an error object explaining what went wrong.

To understand this better, consider a simple example. A client sends a request to a server using JSON-RPC. The request specifies the JSON-RPC version, an ID, a method name, and parameters. For example, the client might call a weather method with the parameter San Francisco, indicating that it wants weather information for that city.

The server responds with a JSON message that again includes the JSON-RPC version and the same ID. The response contains the result, such as the temperature and weather conditions for San Francisco. The matching ID confirms that this response corresponds to the original request.

JSON-RPC also supports notifications, which do not include an ID and therefore do not expect a response. For example, a server might send a notification with a method called progress and a message such as “processing data.” This is commonly used to inform the client about the status of an operation without requiring a reply.

In summary, MCP relies on JSON-RPC to enable structured, lightweight, and language-independent communication between clients and servers. JSON-RPC provides a clean way for MCP clients and servers to interact, invoke methods, exchange data, and send notifications efficiently.

# **E) MCP Transport Layer**

After gaining a solid understanding of the protocol itself and having detailed discussions around JSON-RPC, it is now time to take a closer look at the MCP transport layer.

According to the official MCP specification, the transport layer is responsible for handling message conversion, enabling communication, standardizing interfaces, and ensuring flexibility across different transport mechanisms. Let’s go through each of these responsibilities one by one.

The first responsibility of the transport layer is message conversion. The transport layer converts MCP protocol messages into JSON-RPC 2.0 format for transmission. Once the message is processed, it converts the JSON-RPC response back into an MCP-compatible protocol message. This means there is a continuous back-and-forth conversion process. MCP protocol messages are transformed into JSON-RPC messages for transport, and JSON-RPC responses are then converted back into MCP protocol messages. The server processes return JSON-RPC responses, which the transport layer translates back into MCP-compatible messages that can be consumed by the AI model.

The second responsibility is enabling communication. The transport layer manages the underlying mechanics of how messages are sent and received between MCP clients and MCP servers. For example, in a chat application, when a user sends a message, the transport layer ensures that the message is delivered to the server correctly. Similarly, any responses or notifications from the server are routed back to the client. This ensures a smooth, reliable, and seamless communication flow between both sides.

The third responsibility is standardizing the interface. MCP provides a standardized way for applications to interact with external tools and resources, ensuring consistency across different implementations. For instance, whether you are using standard input/output (stdio) for local processes or HTTP with server-sent events (SSE) for remote communication, developers interact with the same consistent API-style interface. This greatly simplifies both integration and development, regardless of the underlying transport mechanism being used.

Finally, the transport layer ensures flexibility. MCP supports multiple transport mechanisms, including stdio, HTTP, and HTTP with server-sent events (SSE), to accommodate various communication needs. For example, an AI model running on a local machine might use stdio for fast local interactions. The same model, when deployed in the cloud, could use HTTP with server-side events to communicate with remote services. Importantly, this flexibility is achieved without changing the core MCP logic.

With this, you should now have a clear understanding of the MCP transport layer and its role in enabling flexible, standardized, and reliable communication within the MCP ecosystem.

# **F) Transport Mechanism - STDIO**

Now that we have studied the MCP transport layer, we know that two important transport mechanisms we need to understand are stdio (standard input/output) and SSE (server-sent events). Let’s start by looking at stdio in detail.

Stdio, or standard input/output, enables communication through standard input and standard output streams. These streams act as channels through which one process sends input and receives output from another process. This mechanism is very commonly used and is especially popular for local process communication.

Let’s look at the use cases where stdio is typically used.

A very common use case is when you are building command-line tools. For example, if you are creating a CLI application, you naturally expect input from the user and produce output in the terminal. If this CLI tool interacts with an AI model, stdio becomes a natural choice for communication.

Another common scenario is local integrations. Stdio is most often associated with local environments. For example, if you are integrating an AI model into a desktop application that works offline, stdio is a good fit. A practical example could be a desktop note-taking application that uses an AI model to summarize notes locally.

Stdio is also useful when you need simple inter-process communication. If the task is lightweight and does not require complex networking or streaming, stdio is ideal. For instance, a small utility that performs calculations or basic data processing—such as a simple calculator that performs additions—can efficiently use stdio.

Another important use case is when working with shell scripts. If you are automating tasks in a Unix or Linux environment using shell scripts, stdio is a natural choice. For example, a shell script might process text files and then pass the content to an AI model for summarization. The script sends input through standard input and receives the summarized output through standard output.

In all of these scenarios, using the stdio transport with MCP enables efficient and straightforward communication between processes. This makes it especially well-suited for local integrations, scripting environments, and lightweight tools.

You might now wonder how this looks in practice.

Typically, you will see a pseudo-code setup where stdio is configured using server parameters. In this setup, you define a command—such as npm or another executable—and then pass arguments or options. For example, you might invoke an MCP server related to the file system and specify which directories are allowed for access. This is done by providing the command and a list of arguments that define how and where the MCP server operates.

This structure aligns closely with what is shown in the official MCP documentation, where a command is defined along with the necessary arguments to control the behavior of the MCP server.

At this stage, the key takeaway is to understand which transport mechanism is being used and why stdio is chosen in certain scenarios. For now, having a basic conceptual understanding of stdio as an MCP transport mechanism is sufficient.

# **G) Transport Mechanism - SSE**

The Model Context Protocol (MCP) facilitates communication between clients and servers using various transport mechanisms. So far, we have already studied stdio, which is commonly used for local integrations. Now we will talk about SSE, which stands for Server-Sent Events, and this transport mechanism is particularly suited for scenarios where the server needs to push updates to the client.

In MCP, SSE enables server-to-client streaming. We usually call this streaming because the data flows continuously from the server to the client. At the same time, HTTP POST requests handle client-to-server communication. So the client sends requests using HTTP POST, and the server pushes updates back to the client using SSE.

Now let’s look at the use cases where SSE is typically used. The first and most common use case is server-to-client streaming, where real-time updates are required. SSE is ideal when the server needs to send real-time data to the client, and the client does not require a continuous outgoing connection for sending messages. For example, you can imagine an AI assistant that provides real-time stock price updates. In this case, the server is constantly sending stock price changes to the client. The server streams these updates using SSE, and the client receives them as they occur, without needing to repeatedly poll the server. So the client is not continuously talking to or pulling data from the server; instead, the server proactively sends real-time updates to the client.

Another important use case is working with restricted networks. SSE operates over standard HTTP, which makes it suitable for environments with strict network policies that may block non-HTTP protocols. A very good example is a corporate environment with restrictive firewalls. In such scenarios, an AI assistant can still receive updates from an MCP server using SSE over HTTP, ensuring compatibility with the network constraints while avoiding blocked protocols.

The next use case is implementing simple real-time updates. SSE is very useful for applications that require straightforward real-time notifications without complex bidirectional communication. SSE provides an efficient and lightweight solution for this. For example, consider an AI-powered news aggregator. If you build a news aggregator agent that sends breaking news alerts to users, the server can push these news alerts to connected clients using SSE. The client displays the alerts as they arrive, without initiating repeated requests. Again, the client is not always initiating communication; instead, the server is actively sending updates whenever new information is available.

In summary, SSE as a transport mechanism in MCP is advantageous when the primary requirement is server-to-client communication, when applications need to operate within networks that restrict non-HTTP protocols, and when implementing systems that require simple real-time updates without complex two-way communication.

Now, let’s briefly look at how this looks in practice. In a typical setup, you specify an SSE-based MCP client using an HTTP endpoint, for example http://localhost:<port>/sse. In the code snippets we will be running, you will see configurations where an MCP remote is specified as an argument. For example, you might call a remote MCP server using a URL like https://mcp.paypal.com. These examples are meant to demonstrate how SSE endpoints are defined and how MCP clients connect to remote MCP servers using HTTP and SSE.

So, overall, this is how Server-Sent Events (SSE) work as a transport mechanism in MCP, and why they are especially useful for real-time, server-driven communication scenarios.

# **H) Transport Mechanism - Streamable HTTP**

Hi folks, welcome back. In the MCP world, things are evolving very quickly. A few days ago, we learned about SSE or Server-Sent Events. However, that transport mechanism is soon becoming legacy and will be deprecated. So, what is it being replaced with? The answer is Streamable HTTP.

Streamable HTTP is the modern remote transport mechanism for MCP, introduced in the March 2025 update of the protocol. It replaces the older two-endpoint TSS-based approach. Previously, TSS required a two-endpoint design for handling requests and responses, but Streamable HTTP simplifies this with a single endpoint that combines request and response streams over standard HTTP.

Here’s how Streamable HTTP works: it uses a single HTTP endpoint to handle both HTTP POST and HTTP GET. The client sends JSON-RPC requests or batches via POST, indicating support for application and event streams in the Accept header. If the server supports streaming or needs to send notifications back to the client, it responds to the GET request using Server-Sent Events over the same endpoint. This is a key difference from the old SSE approach, where multiple endpoints were needed.

Streamable HTTP is a standardized and unified protocol. It defines transport using HTTP POST and GET with JSON-RPC, and optionally supports SSE. Security is built in, with features like HTTP security practices, origin validation, CORS, and authentication headers, which ensure that client-server messages are protected. This allows secure two-way data flow, maintaining privacy while enabling powerful integrations.

Streamable HTTP also provides real-time capabilities, supporting bidirectional streaming through Server-Sent Events over the same endpoint. This is particularly important for applications that require continuous updates from server to client and vice versa.

Use cases for Streamable HTTP typically involve scenarios where your MCP server is running on a cloud VM or virtual machine, and the client needs to connect to that HTTP endpoint. It simplifies communication between client and server while maintaining security and real-time interaction. Demos will soon be provided to show how to run an MCP server inside the cloud or a virtual machine and connect to it from a client using HTTP.

Another important advantage of Streamable HTTP is universal compatibility. Since it works over plain HTTP, it is compatible with existing middleware infrastructure and stateless, serverless platforms. This makes it suitable for a wide range of AI applications, including chatbots, ID assistants, and many more.

In summary, while SSE has been widely used, the way forward in MCP transport is Streamable HTTP. It simplifies endpoint management, supports real-time bidirectional streaming, ensures secure communication, and offers broad compatibility across platforms.
