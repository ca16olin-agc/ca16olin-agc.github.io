---
layout: page
title: Documentation
permalink: /documentation
---

## Computers of Space Exploration: Why it Matters


For the final project for the class Computer Architecture, our team of four decided to delve into research regarding computers of space exploration. We especially looked into the architecture and the physical properties of computers that were part of famous space missions, such as the Voyager mission, and the Apollo Program. Of the many potential topics that were available in this area, we decided to focus on the effect the harsh environment of space have on computers, and how different space exploration computers of history overcame them.


The culture of Franklin W. Olin College of Engineering tends to structure classes to be highly experienced based, project based, and design based. Naturally, most of the activities in Computer Architecture were based on labs and application of what we learned during class. Our team wanted a change in pace; we wanted to satisfy our curiosity for a topic rather than develop intuition and design sense regarding application. Therefore, we decided to lean towards a more research based project. (We are not saying application based classes are bad at all! We just wanted a little diversity in our experience.)


In addition to expanding our knowledge, this research project offered us the opportunity to push our learning and understanding of Computer Architecture to its limits. When an individual is designing a computer, there are a long list of specs he or she may consider, such as clock speed, instructions per cycle, throughput, and so forth. The previous specs are heavily considered in a standard computer architecture class, but what if the computer were to be sent into space? Computers of space travel have a weight of extra criteria thrown onto them. They must be able to function in dire conditions, even at the cost of efficiency. Our team felt that there would be great merit in understanding a Computer Architecture with different goals from the material we learned in class. This will also allow our fellow peers to think outside the box when we share our discoveries with them.


## Our Project Path and Story

Our team members initially gathered together with a deep curiosity of space exploration that we did not know how to channel. Of the recommended project directions offered from our instructor, we decided to “Teach somebody something cool about Computer Architecture,” by discussing computers of space travel. We immediately hit the school library and online databases to broaden our understanding and to narrow on a topic more specific than “space computers”. We found the Olin Library database to be especially helpful.


Despite our initial engagement with the project, our team struggled greatly in the following few days as members of our team suffered serious burnout and exhaustion. The rigor of classes outside of Computer Architecture contributed greatly to our burnout, but our team also felt very unfocused and unmotivated as we did not have a clear final goal for the project. We knew that we wanted to share with the class about computers that could endure the extreme conditions of space, but we did not know how to carry that out. A lack of communication was clear, as some of us thought we would explicitly study the Apollo Guidance Computer, while others quietly craved an implementation due to their Olin DNA.


The accumulation of our frustration and anxiety almost drove us to a pitfall; we wanted to build the Apollo Guidance Computer in verilog and get the project out of the way. Thankfully, our instructor stopped us from taking such a path, as we would have failed to achieve any of our team goals (listed in the first section!). The AGC as a standalone did not cover the interactions between the environments of space and the architectural decisions of the computer, as there were an abundant amount of understanding the user needed to operate the machine correctly. In other words, the astronauts operating the AGC had to take into consideration the harsh environments of space when inputting instructions, rather than just the computer being fail-proof to the environment.


After avoiding the pitfall, our team gathered to discuss and set a clear end product for the project. We reminded ourselves to stay loyal to our initial goal of teaching our peers to think differently about Computer Architecture. From there, we set our end product for the project to be a presentation to our peers that discussed the harsh conditions of space that would ruin a standard computer, space exploration computers from the past that tackled these issues, and two specific techniques such computers used: radiation hardening and redundancy management. Once we had our outline and key words communicated with one another, we were able to continuously work together as a team to achieve our end product.


## Work Plan and Reflection


At the very beginning of our project timeline, we developed a work plan with meeting dates and big deadlines such as when the research will be completed and when the poster will be made. However, without delving into the research and knowing more about the subject, we could not develop a completely feasible timeline for ourselves. Therefore, during the team meetings, we developed mini work plans, where we set the date for the next meeting, and allocated work amongst the team to be finished until that date.


As mentioned above in our project storyline, communication and goal-setting were a big issue for our team. A self-imposed midpoint check in helped our team reorganize and reestablish our goals. We found that having frequent shorter meetings and check ins allowed our team to allocate work better and have a clear direction.


Initially in our research process we found that everyone going off in their own direction and pulling up resources was inefficient as there was great redundancy in the material we unearthed. However, we also valued the discussion of a specific resource as it enhanced our understanding and appreciation for the topic. Therefore, a tactic we implemented was to break our team of four into two sub-teams and have each sub-team explore a topic together. We continued this setup into the write up process so that each member of the sub-team could critique each other's work.


Our original final product was intended to be a poster, displaying all the information we discovered and organized for our fellow students. However, our instructor told the class that he felt a more interactive presentation would be more effective than a static poster. Therefore, we have decided to abandon the poster, and switched to an interactive presentation, as we attempted to bring the audience to participate in our discussion of space computers.


## Future Iterations of our Project


To anyone who is reading our story, we welcome and challenge you to continue on our work. Two potential future iterations of this project may include further research, or more interestingly, an implementation of the redundancy management system. 


To future Computer Architecture students (or anybody else) who wants to delve into more research, we recommend that you use extensively the resources at your disposal. Our team discovered that the Olin Library database had an amazing collection of information that became the core of our project. During our research, we also discovered interesting sites such as a website dedicated to the AGC developed by an Olin alumni. It is important to remember that Olin has a lot of resources and connections despite its size.

An interesting implementation would be developing a circuit that introduces error into the CPU. For example, students may use the random function in verilog to generate error into some part of the computation process (For example, the ALU operations), and develop a circuit to counter that error. Such error can be countered by information redundancy, structural redundancy, and time redundancy. Afterwards, students may compare the time cost, and area cost of each implementation.

To the students who want to implement a redundancy management system demo, we recommend that you start out simple and not try and copy a space computer that you find online. Although the architecture of older space exploration computers are simpler than many today, they are still more complicated than the CPU implementations students have gone through in a standard Computer Architecture course. 


To anyone who is willing to continue on with our project, we will leave you on this website with all the resources we have used for our project. It is a great idea to start off by reading through our presentation and sifting through our resources.
