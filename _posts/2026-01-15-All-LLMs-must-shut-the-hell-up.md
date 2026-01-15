---
layout: post
title: "All LLMs Must Shut The Hell Up"
date: 2026-01-15
---

I like building cool things. This is primarily why I was so excited when I first saw GPT-3 materially improve my code quality. And I thought: "Oh man! How many more cool things can I build now?!". Unfortunately, the better LLMs got at coding, they have had a completely opposite effect: my motivation dwindled and didn't fully understand why.

Of course I tried all sorts of things, starting from GitHub Copilot autocomplete and ending with Claude Code (Opus 4.5 is REALLY good). And while I could create code much faster, it seemed like my speed of building software didn't really improve. And more importantly, my ratio of reading code to writing code got completely obliterated.

At some point, you get tired of reading code: the typical "LGTM" attitude wins. And at exactly that point, you are no longer the author of the code. The _I_ in _I like building cool things_ is gone. You see, the sentence is not _I like seeing cool things get built_: it's _I like building cool things_.

![Claude chair](/assets/1/claude_chair.jpeg){: style="max-height:400px;" }

My love of writing code comes from thinking, theorycrafting, tinkering with technology, figuring out problems and eventually finding a solution. I "win" over a problem. I get to add that to my awesome collection of problems that I have solved and technologies I now have experience with. I remember literally crying tears of joy when I figured out all the problems with my first AWS ECS deployment after having no previous experience with cloud or Docker (it took me three days and I was mentally ready to escape to the forest on day two). I understand some people don't get their kicks from solving technically challenging problems - for those of you, the rest of the blog post might not make much sense.

GitHub Copilot did not change my satisfaction of coding because all it did was suggest lines of code I already had in my head. It simply sped up the process of pressing buttons on the keyboard, which was awesome.

Claude Code and other agents are a completely different beast. And I think the biggest problem lies in their UX design. When I write code, it is my sacred time of flow. I dive deeply into a mountain of files, multiple of them open in my editor. My focus is entirely in my IDE and all that is happening is a mental building of blocks in my head. Most of the time I don't actually write code. I start writing code when the solution is already obvious and all that is left is explaining that solution to a computer.

![Meeting chart](/assets/1/meeting_chart.png)

Agents don't let me get there. Just imagine having an entire coding day filled with "5 minute meetings". A chat interface forces me to involuntarily activate my social skills, despite logically knowing that this text is not being read by a human being. It stops being a tool and instead becomes a coworker behind a screen. It is so easy to just anthropomorphize the agent that you need to constantly keep fighting your own instincts. You feel bad when you scorn it for making a mistake, which to me is just pure insanity. Would I curse and swear at any of my other software if it didn't work properly? Of course! It does not have feelings! Exact same logic applies to LLMs, but it simply does not "feel" that way.

Another problem with an agentic chat approach is that you no longer understand your own code structure. Before, you needed to know where things are, how they are built, what exactly is being changed and for what reason. Now, you need to figure all that out from the LLMs output, giving even more impressions of having to "review" the code of a coworker. If you are patient enough to be reviewing PRs all day long then you are clearly a better man than me.

So, I needed to find some solution. I want to go back to this GitHub Copilot-like experience but I don't want to lose out on the extra capabilities. I don't want to be exposed to chat interfaces or having to verbalize the inner workings of my mind to an LLM, which causes me to drop out of flow.

For this reason, I've made an [extension for VS Code](https://marketplace.visualstudio.com/items?itemName=grzracz.llm-implement) that solves the problem a little bit. The previous CTRL+I shortcut still exposed you to a (small) chat interface. I've changed it so instead the LLM is told to figure it out. If there's a comment, do what the comment says. If there's a bug, fix it. But don't ask me any questions: you are a tool, you have no right to speak in my holy tongue.

![All machines](/assets/1/all_machines.jpg)

Feel free to use the extension but beware it is of "works on my machine" code quality.

I'm not entirely sure it will solve the problem, but it's a start. And now the solutions I build are entirely mine - mostly because I know what's supposed to be there. I **could** have written it myself again if need be. The LLM just simplifies the process of looking up documentation/snippets of code I've written in the past, similarily to how GitHub Copilot simplifies the moving a line of code from my head into the IDE.

I still use browser-based or terminal-based chat interfaces for brainstorming, ping-ponging ideas and getting unstuck. But when it comes to writing code, **all LLMs must shut the hell up**.

_No GPUs were harmed in the making of this blog post._
