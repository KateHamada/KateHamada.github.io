---
layout: essay
type: essay
title: "Reflect on Your Use of AI in ICS 314"
date: 2025-12-15
published: false
labels:
  - AI
  - Software Engineering
---
## Introduction
Artificial intelligence (AI) can be used as a learning tool as well as a tool to “cheat” depending on how a student chooses to use it. For Software Engineering specifically, I think AI is a very helpful tool that many could argue is “cheating” when it comes to Software Engineering since it could basically in theory write all of your code for you. However, I don’t see it as cheating since there are website creation sites that take out the coding aspect making it easier for people to create websites which is essentially what AI is doing as well. Throughout this course I’ve used ChatGPT, Co-Pilot, as well as Claude which have been very useful in helping me the final project as well as other assignments.

## Personal Experience with AI
### Experience WODs
For Experience WODs like the beginning ones dealing with Typescript, I would use AI mainly to help me get unstuck at the beginning. I prompted ChatGPT with something like: “Explain how to approach this WOD step by step without giving the full solution.” Or I would ask how do I do this specific calculation. This was useful for understanding the structure of the task, but I avoided asking for full code because relying too much on AI slowed me down when debugging. In addition to that in the later WOD's I would just attempt it myself with little to no AI prompting and then watch the youtube video to see what I was supposed to do. Which helped me the second time that I did the Experience WODs, if I did a second time.

### In-class Practice WODs
For in-class Practice WODs, I would typically ask more generalized questions like asking how to do something instead of how to fulfill the prompt so that I can understand what to do for the actual inclass WOD's since ChatGPT would sometimes take a while to analyze the prompt and provide code that I could start testing/using. 

### In-class WODs
During in-class WODs, I would ask ChatGPT to do a section of what the WOD was asking me to do since sometimes if you put the entire prompt into ChatGPT it'll mess up something. For example the Justin Bieber WOD, even though I couldn't get my code working, I just asked ChatGPT if the function I created accounts for edge cases that the WOD wanted like so:

```
Does this account for not including "babylon" since it's not just baby? 

function hasBaby(lyrics: string[]): boolean { 
  const lowerCased = lyrics.map(str => str.toLowerCase());
  lowerCased.filter(str => str.includes('baby')); 
  if (lowerCased.length > 0) { 
    return true; 
  } 
  return false; 
}
```

### Essays
For most of my technical essays I pretty much just copied and pasted my essay into ChatGPT and asked it to give me suggestions on titles and headings which helped since I would usually blank on coming up with creative titles/headings.

### Final project
For the final project I would typically ask either ChatGPT and/or Co-Pilot:
```
How do I fix this error?
Type '{ interest?: { connectOrCreate: { where: { name: string; }; create: { name: string; }; }; } | undefined; name: any; purposeStatement: any; mainContact: any; email: any; image: any; approvalDate: Date; expirationDate: Date; }' is not assignable to type '(Without<RioCreateInput, RioUncheckedCreateInput> & RioUncheckedCreateInput) | (Without<RioUncheckedCreateInput, RioCreateInput> & RioCreateInput)'.
  Type '{ interest?: { connectOrCreate: { where: { name: string; }; create: { name: string; }; }; } | undefined; name: any; purposeStatement: any; mainContact: any; email: any; image: any; approvalDate: Date; expirationDate: Date; }' is not assignable to type 'Without<RioUncheckedCreateInput, RioCreateInput> & RioCreateInput'.
    Type '{ interest?: { connectOrCreate: { where: { name: string; }; create: { name: string; }; }; } | undefined; name: any; purposeStatement: any; mainContact: any; email: any; image: any; approvalDate: Date; expirationDate: Date; }' is not assignable to type 'RioCreateInput'.
```
Then I would let it analyze my code if it was Co-Pilot or I would copy and paste the section of code that is related into ChatGPT. Then add the changes, which would work out about half of the time but sometimes it would just lead to ESLint errors where I would then copy and paste the ESLint error into AI and ask it how to fix it.

### Learning a concept / tutorial
When learning new concepts like functional programming or Underscore methods, I asked prompts such as: “Explain JavaScript reduce with a simple example related to arrays of objects.” AI was very useful here because it provided intuitive explanations and examples, but the downside was that examples sometimes oversimplified edge cases relevant to the course.

### Answering a question in class or in Discord
I didn’t use AI in order to answer a question in discord because the one time I did answer a question was when I had already done the assignment and so I didn’t need an outside source to tell me how to help.

### Asking or answering a smart-question
When answering a smart question I definitely wouldn’t need to use AI because I should be able to understand what the question was asking. Since the question was about understanding the requirements for an assignment I was able to respond without using AI.

#### Smart Question:
I'm slightly confused on the presentation requirements for https://courses.ics.hawaii.edu/ics314f25/morea/project-management/experience-team-presentation.html.


It looks like the 2nd and 3rd bullet points are talking about the same thing:
```
- The next three minutes should present your GitHub project page for the Final Project Milestone M1. Note: you do not have to have an HTML mockup for this presentation. As an alternative, you can embed pictures of paper-and-pencil mockups into this page. Here’s an example GitHub project page from Bowfolios: https://bowfolios.github.io/.
- The final two minutes should present your M1 Project. Make sure the Project is organized according to the IDPM guidelines. Here’s an example Project Board from BowFolios: https://github.com/bowfolios/bowfolios/projects/3.
```

Is it okay if we present our landing page for the second bullet point, and then talk about the M1 project for the third bullet point?

### My response:
“The second bullet point isn't talking about the website your building, its talking about presenting a github.io page that talks about the website like this: https://bowfolios.github.io/”
However, if the subject of the question was something I was unfamiliar with then I would use AI to try to find an answer for the smart question. I technically didn’t ask any smart questions so that doesn’t apply here.

### Coding example
For coding examples, I used prompts such as: “Give an example of using underscore .pluck on an array of objects.” AI was useful for seeing basic syntax quickly, but I often had to modify the example to match the exact data structures used in the WODs.

### Explaining code
I used AI to explain unfamiliar code with prompts like: “Explain what this function is doing line by line.” This was very helpful for understanding logic flow, though sometimes the explanations were longer than necessary or assumed intent that wasn’t explicitly in the code.

### Writing code
When writing code, I occasionally asked: “Write a simple function that satisfies these constraints <description>.” AI helped me get started, but the generated code often needed significant revision, and debugging AI-written code sometimes took longer than writing it myself.

### Documenting code
For documentation, I didn't use any AI because I typically understood what a section of code was doing without AI. I only really use AI as a starting point and can typically read code and understand what it's doing. 

### Quality assurance
For QA tasks, I asked questions such as: “What’s causing this ESLint error in my code? [pasted error here]” AI was especially useful here, as it helped identify common mistakes quickly, though I still needed to understand the fix to avoid repeating the same error later.

## Impact on Learning and Understanding
Overall, the incorporation of AI has had a noticeable impact on my learning experience in ICS 314. AI tools improved my comprehension by helping me quickly clarify unfamiliar concepts and see concrete examples, especially when learning new software engineering patterns or JavaScript features. At the same time, relying too heavily on AI could challenge skill development, since it sometimes reduced the need to struggle through problems on my own, which is where much of the learning happens. When used intentionally, AI enhanced my problem-solving abilities by acting as a guide rather than a solution, but it also required discipline to ensure I was understanding why something worked instead of just accepting an answer.

## Practical Applications
I personally didn't do the HACC nor have I used AI for real world Software Engineering challenges as I only have experience with software engineering from this class. However in a real world context, I would assume that AI could be helpful for brainstorming system designs, generating starter code, and identifying potential edge cases when planning features under time constraints.

## Challenges and Opportunities
One challenge I encountered when using AI in the course was that its responses were sometimes too generic or did not fully align with the specific constraints and expectations of ICS 314 assignments, which required careful verification and revision. Additionally, it could be tempting to rely on AI for quick answers rather than fully engaging with the problem-solving process. However, there is an opportunity to further integrate AI into software engineering education by using it as a guided learning tool—for example, to provide structured hints, automated code reviews, or targeted feedback—while still encouraging independent thinking and deep understanding.

## Comparative Analysis
Compared to traditional teaching methods, AI-enhanced approaches in software engineering education tend to increase engagement by providing immediate, personalized feedback and examples tailored to a student’s specific questions. While lectures and static tutorials support long-term knowledge retention through structured explanations, AI tools can reinforce understanding by allowing students to actively explore concepts and receive clarification on demand. However, practical skill development is most effective when AI is used alongside traditional methods, as hands-on practice and instructor guidance ensure that students build foundational problem-solving skills rather than relying solely on AI-generated solutions.

## Future Considerations
In the future, AI is likely to play an increasingly important role in software engineering education by offering more adaptive learning experiences, such as personalized feedback, intelligent code reviews, and real-time debugging support. Advancements in AI could help instructors identify common student misconceptions and provide targeted interventions, but challenges will remain in ensuring academic integrity and preventing overreliance on AI-generated solutions. To be most effective, AI toolRIBows-logo.pngs should be designed to support learning and exploration while still encouraging critical thinking, creativity, and independent problem-solving.

## Conclusion
Overall, AI has been a valuable supplement in the Software Engineering course, enhancing comprehension, efficiency, and confidence when learning complex concepts and tackling challenging problems. At the same time, this experience highlighted the importance of using AI intentionally, as meaningful learning still depends on active engagement and personal effort. Moving forward, AI should be integrated as a guided learning aid—such as for structured hints, concept explanations, and feedback—rather than a replacement for hands-on practice, ensuring students develop strong foundational skills alongside the benefits of AI support.
