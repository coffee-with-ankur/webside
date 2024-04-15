---
title: >-
  Reducing Friction between Development Teams and Complex Infrastructure:
  Interview with Dhivya, Head of Delivery
cover: >-
  https://res.cloudinary.com/dwphg8fpc/image/upload/v1710872074/Blog-Reducing-Friction-between-Development-Teams-and-Complex-Infrastructure_1x_yuqdys.jpg
date: 2023-09-19T18:30:00.000Z
tagName: BlockChain
position: 3
isVisible: true
description: >-
  In today’s technology landscape, companies are facing increasing pressure to
  deliver software quickly and efficiently. However, the challenge of managing
  complex infrastructure can create friction between development and operations
  teams, leading to inefficiencies and delays in the development process.
---

\
1\) In today’s technology landscape, companies are facing increasing pressure to deliver software quickly and efficiently. However, the challenge of managing complex infrastructure can create friction between development and operations teams, leading to inefficiencies and delays in the development process.

Please tell us the challenges faced due to this friction from your experience.

Interesting to start with this part. This rift between the development and operations team is actually what is called the DevOps divide. 

The most obvious one is a delay in the delivery. With a larger DevOps divide, communication and collaboration is sub-optimal. This can be further worsened if both teams have a difference in vision/priorities/strategies leading to further misunderstanding. With so much difference between the two core teams, the delivery will be riddled with bugs, issues, gaps, process leaks, and delays. 

One other challenge I have faced very often as a DevOps manager is a lack of visibility. Outside the team, not many people are even aware of what is happening. A true form of a closed black box. it is so close you have access to it but it is so opaque that you think nothing happens. This also causes issues with people not that familiar with the operations part as they think no work is happening. When one does not understand infrastructure operations that well, we tend to map it to regular applications. but status updates/jira tickets are and cannot be on the same level. And suddenly no one understands what is happening which over time results in, I don’t know what the Ops team is doing. And now you are left to fight the perception that you are working on something. 

However, the one challenge that is a force multiplier is that this DevOps divide results in finger-pointing and blaming when things don’t work as is. The devs team often says the environment is always unstable hence the productivity was impacted. The ops team says that the logs were clear, you should have just gone and fixed it. The Dev team thinks it is not my work as it is the work of a DevOps engineer and this goes on and on. This finger-pointing goes beyond one incident and often keeps the team in the ‘Storming’ phase in the Tuckerman model. When it hits this you are no longer only dealing with unstable environments but also with people who are not too keen to work together. 

2\) What according to you are some of the most common sources of friction between development teams and infrastructure teams?

Incident response and RCA’s are probably the most common source of friction IMO. Actually, it is not directly that. Incident response is a symptom of a much deeper problem i.e. a sense of ownership of the stability of the environment. While the ops team works on creating the infra and the dev teams build the application, these pipelines are what keep the system running. One fault on it means a direct impact and the productivity dips. As serious as it sounds, I have often seen more of where the DevOps person is to fix this and less of, hey let me get my hands dirty. A counterpart to it could be the lack of skill but c’mon, at one point in time all of us were proficient in only one stack. We then evolved. But DevOps comes across as a scary world to many of the devs I have worked with who just literally and figuratively freeze when the pipelines fail. They don’t want to go to the deeper darker world of DevOps 😀 

The other side of this coin is that in many teams the Dev teams are not enabled with enough information to be able to fix the issues. Sometimes it is just expertise and sometimes there is a lack of a how-to. 

We need our DevOps to build environments in such a way that we know, acknowledge, and work towards the idea that one day this environment will be maintained by a developer who doesn’t have god/super admin access.

3\) Can you share any examples of how friction between these teams has negatively impacted a project or a company?

What DevOps does is usually the one behind the scenes. They build the backbone of the entire application. You wouldn’t see a state-of-the-art UI as an output to show. but it will ensure that the API’s are not hacked. You will not see database entries in millions of records but it will ensure that all resources scale enough at the right time for those millions of records to be inserted. DevOps usually comes into focus when things break. 

There are plenty of examples of how the divide can lead to a bad reputation for an organization. 

Longer downtime, no disaster recovery planned, Security vulnerabilities, Truck factors of 1 or 2, Innovation dies down as we are always firefighting. 

Let’s say that the dev team plans a rollout with some eye-catching code without informing the Ops team. This leads to increased sales which is great for the company but now with the Ops team in the blind, the infra has not been revamped to handle the new scale. HPA and ASG are not just click of buttons. As a result of this, the site crashes leading to bad business values. 

Another classic example is cloud migration. Anytime we speak of this, the development teams say that this is not on us the DevOps team will take care. But in reality, it is a combined effort as the DevOps team needs to know what to migrate. Without this knowledge from the development team, it is possible that some things are left out, and hence post-migration, there is a downtime, bad user experience, or just significant delays in the migration as it is not working. 

Another thing is a hotfix/patch deployment. When a critical bug is reported, the development team rushes to fix it as it causes an impact on the revenue. While it is busy on this, the DevOps team is unaware and is sipping pina coladas on the beach. Suddenly when all is fixed, the DevOps team gets a message to deploy ‘right away’ as it is a patch. This is immense pressure on the DevOps team who until a few seconds ago were unaware. While emergency patches are unavoidable, including the DevOps team from the beginning helps in reducing the pressure and planning much better. 

4\) When it comes to reducing friction, what are some strategies that have worked well in your experience?

The one thing that worked wonderfully well was building a cross-functional team. At CoffeeBeans, we invested time into making DevOps a mindset across the org. All devs had to undergo mandatory training to learn about the basics of ci/cd pipelines. This gave them a vast understanding of how things were built and removed the fear of the big black box. We also had DevOps 101 for the non-technical teams such as business analysts, and talent acquisition so that they know what is expected when we say DevOps and everything related. 

The other tiny effort that made a lot of difference is having a slightly different format of updates in Jira cards. We did not talk about Given-When-Then, we spoke about which environment, what is the downtime, and who are the stakeholders to be informed. We retained Acceptance criteria though. 

Another thing that worked and helped immensely when new people were on board was having a standard set of questions in a checklist for every application we built. This ensured that we were maintaining standardization and consistency across projects and most importantly, we were not missing out on anything critical. This list also helped us chalk out very clearly what the project needs and what it does not. a crucial point that helped us with our client communications. 

5\) We often hear about the importance of balancing agility and innovation with stability and reliability. Can you share any insights on how to do this effectively in a complex infrastructure environment?

1. The mantra of any application now is CI/CD. Once setup, this is a significant game changer in the way agility can be infused with stability 
2. Define the vision/priorities/goals and ensure both teams understand that. 
3. Draw a virtual line between components in an infrastructure based on criticality. Must-go ones have to be in a stable state all the time. the other segments that can afford a shift/downtime can be used in innovation and playground
4. Use IaC
5. different deployment strategies like A/B, the canary that let you reduce the risk of downtime giving you enough space to explore and innovate
6. Exhaustive monitoring and alerting

6\) What are some potential risks or pitfalls to avoid when trying to reduce friction between development teams and infrastructure teams?

1. buy-in from the leadership – Make sure your leadership knows the why behind the what of changes in the DevOps strategies. 
2. Assuming everyone knows – don’t assume everyone knows the reason/rationale/approach behind changes or even that it is happening. Communicate
3. Not addressing tech debts soon enough
4. Wanting everything yesterday – This is a double-edged sword. With the time to market being the least ever, it is common for everyone to expect all deliverables yesterday. and for the things we don’t understand, we often tend to underestimate the complexity and time needed. We should leave the work to the experts and have due faith in that. 
5. Unclear processes for change management 
6. Undefined SLAs in change management

7\) Finally, can you offer any advice or best practices for organizations looking to improve collaboration and reduce friction between these teams?

1. Invest in automation. 
2. Give space and time to clear out the tech debts. This goes a long way in ensuring the rigidity and reliability of the system. 
3. Acknowledge the cultural and mindset differences between the development and operations teams. Their work expects different kinds of working styles. Even their format of Jira updates wouldn’t be the same. 
4. don’t downplay it when someone says it takes me that long to build an environment
5. if the pipelines are red for long and red often, the root cause is something other than a devops people being a truck factor. 

## Conclusion

Reducing friction between development teams and complex infrastructure requires a combination of technical solutions and cultural changes. By adopting DevOps practices, automating infrastructure, using containerization, fostering communication and collaboration, and providing adequate training, you can ensure that both teams are working together towards the same goal, which is to deliver high-quality software quickly and efficiently. With the right approach, organizations can reduce friction, improve efficiency, and deliver software faster and more effectively.
