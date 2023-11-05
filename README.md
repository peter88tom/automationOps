# AutomationOps
automationOps is a morden approach to automation. AutomationOps methodology brings together the business users and technical team to plan, build, maintain, and continues improve automation. 

# Software robot delivery process
- The initial idea of automation something
- Evaluating whether the idea is technical feasible

- Calculating the return on investment(cost vs benefits)
- Documenting the process
- Implementing and testing the robot
- Lunching the robot to production
- Maintaining the robot


> #### Note:
> One of the crutial parts of robotic automation (RPA) is finding the suitable process to automate
> 
> In small organization might easy to spot promissing process.. The larger and more complex organisation, the harder it gets.


# Tips for finding pontetial process to be automate
- What is most people in the organization working on? More people -> more work -> more tasks to automate
- Idea to automate can come from the personal completing the process or someone else involved in the process.
- You can try [process mining](https://en.wikipedia.org/wiki/Process_mining) to help with analyzing and identifying potential processes with automation potential
- ideation workshop can be a valuable source of great automation ideas.
- You might have an idea that would improving efficiency but can not be completed even manually at the moment. Sometimes automation enables you to create entirely new process instead of automating existing one.
- See Figure 12. "Distribution of use cases by complexity of implementation and benefit realized across functions and sectors" in the excellent [ RPA use cases research report by Capgemini Research Institute](https://www.capgemini.com/wp-content/uploads/2018/10/Automation-Use-Cases_Digital1.pdf)
- Collect all possible idea in the backlog. Then decide which process to start with: depending on your use case, it could be the most straightforward process to automate or the one you think will have more signficant returns on investment. 

# Technical Feasibility Assessment
Technical feasibility is done to understand if the automation goal is realistic. You can develop some questions like:
- Could a robot complete the process by following unambiguous rules? For example this process:
  >Download the sales data Excel file, open the intranet website, log in, enter the sales data, take a screenshot, create a PDF document. Definitely something a robot could do!

You will have to ask yourself different questions like: 
1. can the robot operate without human interaction?.. 
2. Does the robot have access to all required accounts?
3. Is the data requires some transformation before the robot can use it?
> After thinking through questions you will have a better of whether the automation could be technical feasible.
>
>Sometime the result of technical assessment is that the automation is not technical feasible at all. The good part is that you found out the showstoppers as early as possible, without wasting time and money!

# Business Feasibility Assessment
After technical fisibility assessment, you know that the process could be automated. But just because something is technical doable, it does not neccessarily make business sense to do it.

When evaluating the feasibility of Robotic Process Automation project, you should complete a business feability assessment to understand  if the automation would lead to a positive returns on investment or not. You can ask yourself this questions:
1. Does the process repeat often?... The more often the process needs to be completed manually, the better the potential benefits of automating it.
2. If the process is manual and time-consuming but does not happen often, you need to consider the cost of implementing the automation.
3. Is the process stable or it changes all the time?.. If you expect the process to change often it might reason enough to decide not to automate it.
4. Is it easy for human operator to makes during the process or it's relatively error proof?
5. What positive effect will automating the process have on the organization
6. Do the positive effect justify the cost? 

# Documenting the process
After identifying a process as good candidate for automation, a good first step is to walk through it and document it in enough details. This documentation will serve as basis for implementing the software robot that will take over and handle the process in the future.

The initial documentation will not be perfect and does not needs to be. You will need to update it as you learn more during development.

Change is inevitable. Change is good. Embrace change. You will learn more about the process you're automating during the implementation. Be agile.

During this requirements gathering, the software robot developer needs to work closely with the business side to get familiar with the current process and the business domains it runs. This often means sitting next to the user when the process is run, asking all relevant questions, and exploring all the possible scenarios

# Process Definition Document(PDD)
The results of the process walkthrough are collected into a document.

In the most formal way we call this the Process Definition Document.
formal means some organization prefer to have very details and strictly processes for managing documentation. For example, writing down everything in minute detail, reviewed by multiple stakeholders, getting approvals, signing off, change management protocols.

### Contents of the PDD
  An effective PDD should provide clear answers to these questions:
  1. What is the process used for, and what it's end goal?
  2. What are the steps involved in the process
  3. Are there any decision points(logical branches)
  4. Who is in charge of the process
  5. By whom and how often the process executed?
  6. Does the process require human intervetions(Attende) or can it be entily handled by automation(Unattended)
  7. What are the systems involved in the process?
  8 Does the user need special authorization or roles to run the process
  9. What are the possible problems and exceptions that can happen during the procedure? How does the user handle those?
  
  		Read more details about documentation [here](https://robocorp.com/docs/courses/software-robot-delivery-process/documenting-the-process)

# Implementing and testing the robot
The implementation have to be start after you understand the process flow. The key to success you have to start small, adding more small steps at a time, running the incomplete robot more often. Nothing has to be perfect in the beggining.

Testing phase - You have to approach the robot implementation as an iterative process(code, run, code, run). This way you can add new functionality and test right away. This will help you noticing possible issues as soon as possible and can address them. If you complete the robot using this iterative approach, there are not many areas that you have not already tested.

Make sure to involve the subject matter experts in testing.

Involve the people who know about the process under automation and ask them to try the robot out in conditions as close as possible to the real world: does it work reliably? Does it do everything that it is supposed to do? Does it handle any potential exceptions and special cases?

# Documenting the Implementation
The robot itself might be good enough documentation. if your process is very complicated and involve multiple robot chained together, completing ten's of tasks and hundred's of steps, then you should consider documenting the implemented solution in a separate document and describe the flow in enough details.


# Lunching the robot to production
Before you can put your robot in production, it's recommended to checklist this:
1. Is the code correctly versioned and available for another developer if you're not available to work on the robot in the future?
2. Does the implementation follow [naming best practises](https://robocorp.com/docs/development-guide/qa-and-best-practices/naming)
3. Does the code respect the best practices in terms of [secret management](https://robocorp.com/docs/development-guide/variables-and-secrets/secret-management)?
4. How will the robot be executed?
5. Have you set up notifications for fail runs?
6. How will you monitor the robot?
7.  Read more [here](https://robocorp.com/docs/courses/software-robot-delivery-process/launching-the-robot-to-production)

# Maintaining the robot
Once the robot it's in production does not mean that you will never touch it again. there might be changes like a new step has been added to the process, a bug has discovered, new employee stepped in and needs to be notified of the runs and so on.

As analysis, having some general knowledge about the maintenance of the robot helps you with the technical and business feasibility assessment.

When doing this changes make sure to keep the Process Definition Document(PDD) is also updated

Also make sure changes are tested before sending them to production, also monitor the robot to verify the changes works as expected.


	


