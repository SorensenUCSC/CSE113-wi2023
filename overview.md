---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: "Overview"
layout: single
classes: wide
---

## Class Description

Welcome to CSE 113: Parallel and Concurrent Programming! In this class, we will explore many aspects of parallel computing, from instruction-level parallelism in seemingly sequential programs to thread-level parallel programs that can efficiently execute across the many cores of today's multiprocessors. We will learn how to write programs that execute efficiently and correctly in concurrent environments. This class will give you the necessary foundation to solve problems using concurrency: a powerful skillset as today's computers are becoming more and more parallel.

## Teaching Staff

We have a great teaching staff this quarter! All of them are passionate about parallel programming. Please get to know them and take advantage of the office hours and mentoring sessions they provide

* *Grad TAs*: 
  * Reese Levine
  * Jessica Dagostini
  * Devon McKee


* *Undergrad Graders/Tutors*
  * Sanya Srivastava 
  * Kyle Little
  * Anish Pahilajani

## Necessary Background

The prerequisites for this class are CSE 12 (systems), CSE 101 (data-structures and algorithms), and recommended CSE 120 (architecture). You will need some foundation in all of those topics to succeed in this class. You will need to know data-structures and algorithms as we will extend some of these sequential concepts to their natural parallel counterparts. You will need some systems background as we will discussing many aspects of the hardware/software interface. Parallel programming is most efficiently executed on parallel hardware: Thus, it is helpful to understand shared  hardware resources (e.g. the memory hierarchy) of the underlying architectures. 

Because this is an upper division class, I do expect a general CS foundation. For the homeworks, I will assume that you are:

- comfortable using a linux command-line
- programming in a high-level language (e.g. Python)
- programming in a low-level language (e.g. C)
- a high-level understanding of computer architecture

## Class Modules

This class will be split into 5 modules, each of which are roughly two weeks:

* **Module 1: Introduction, Background and ILP** This module will introduce the class and provide a programming, compiler, and architectural refresher. We will discuss how modern hardware exploits parallelism within a sequential thread (ILP) and how to write parallel code in C++.

* **Module 2: Mutual Exclusion** This module will discuss the fundamental problem of mutual exclusion. We will discuss the theory behind mutual exclusion, how it is implemented in practice, and specialized mutual exclusion implementations. 

* **Module 3: Concurrent Data Structures** This module will discuss concurrent objects and how to reason about them. We will discuss several implementations and show how they can be used in load balancing and software pipelining.

* **Module 4: Reasoning about Concurrency** This module will discuss how to reason about concurrent programs, including memory consistency and fairness. 
 
* **Module 5: Heterogenous Parallelism (GPGPU)** This module will discuss heterogenous programming, with a focus on GPGPU programming. We will discuss the SIMT programming model, hierarchical execution, and different architectural considerations when optimizing programs.

## Class Format

Each class is 65 minutes. I will plan to be available 10 minutes before class starts and 10 minutes afterwards. 

_Non-protected materials_ will be hosted on this website. This includes the schedule, lectures, and references, etc.

_Protected materials_ will be hosted on a Canvas website that you will need your university credentials to access. These materials include homeworks, zoom links, lecture recordings, tests, grades, etc.

_A Class forum_ will be provided in Piazza. If you organize other forums outside of the class Piazza (e.g. discord), you must adhere to academic integrity and be kind to each other. 

## Quiz/Attendance

Live discussions and synchronous class attendance are a valuable part of the learning experience. I expect you to make an effort to synchronously attend this class, whether on Zoom on in-person.

I plan to upload recordings of the class to canvas, but this is not a substitute for attendance. This will be graded using a small quiz given at the end of the class. Please do not submit the quiz unless you either attended or watched the lecture. If you submit a quiz without this, it will be considered a breach of academic integrity. 

You can have up to 3 absences that will not affect your grade. 

_If synchronous attendance drops significantly then I will stop recording lectures and make attendance a part of the grade_

## Accessibility

UC Santa Cruz is committed to creating an academic environment that supports its diverse student body. If you are a student with a disability who requires accommodations to achieve equal access in this course, please submit your Accommodation Authorization Letter from the Disability Resource Center (DRC) to me by email, preferably within the first two weeks of the quarter. I would also like us to discuss ways we can ensure your full participation in the course. I encourage all students who may benefit from learning more about DRC services to contact DRC by phone at 831-459-2089 or by email at drc@ucsc.edu.

## Office Hours:

### Instructor Office Hours:

I will provide 2 office hours per week: Thursdays from 3 - 5 PM. 

My office hours can be remote or in-person. My physical office is E2-233. I will provide a Zoom link on canvas. I manage the office hours through a Google doc sign-up sheet. I will reset the list around noon on Thursday and notify with a canvas announcement. Any name on the list before then will be erased.

Please sign up for only 1 slot at a time. If there is no other student waiting at the end of your slot, you are welcome to stay. If you want to discuss an issue that you think others might also be interested in, please add the issue to the spreadsheet. If you see your issue listed, please add your name and we add more people to the discussion. 

The sign-up sheet is meant to provide fairness; as such I will be strict about keeping to the schedule. Please forgive any abruptness.

### TA and tutor Office Hours:

|    **TA/Tutor**   |   **Days**  |                   **Times**                   |          **Modality**         |                                      **Zoom Link/Signup/Location**                                      |
|:-----------------:|:-----------:|:---------------------------------------------:|:-----------------------------:|:-------------------------------------------------------------------------------------------------------:|
|    Devon McKee    |     Thu     |                1:30PM - 3:30PM                |             Remote            |                  https://ucsc.zoom.us/j/6705118855?pwd=alQ1SmlFbzFXMlQrYVFET1JiK1pJQT09                 |
| Jessica Dagostini |     Mon     |                12:00PM - 2:00PM               |             Hybrid            |                      BE-151, https://calendly.com/jessicadagostini/office-hours-113                     |
|    Reese Levine   |   Tue/Wed   |                12:00PM - 1:00PM               |   Remote Tue,  In person Wed  | BE-153A, https://docs.google.com/spreadsheets/d/1Hq6pG0rp0u-h68ADaKMkZkqwva_A0jlW2IUaLUHO0ZM/edit#gid=0 |
|  Anish Pahilajani | Mon/Wed/Fri |                6:00PM - 7:00PM                |             Remote            |                             https://piazza.com/class/lckt6jighkv5d1/post/20                             |
|  Gurpreet Dhillon | Mon/Wed/Fri | 11:00AM - 12:00PM (M/F), 12:00PM - 1:00PM (W) | Hybrid Mon/Fri, In person Wed |      https://docs.google.com/spreadsheets/d/1PLG5hJcd1ogbPXoGxLLXHwA-J0FgdKkFwMJ1GPmfxrE/edit#gid=0     |
|    Kyle Little    |   Mon/Fri   |  11:00AM - 1:00PM (M), 10:30AM - 11:30AM (F)  |             Hybrid            |   https://docs.google.com/spreadsheets/d/1EUVZQueNAoQEQClENMamtaqQpENN9DttlnW8Jyiut4w/edit?usp=sharing  |
|  Sanya Srivastava |   Tue/Thu   |   2:00PM - 3:00PM (T),  1:00PM - 2:00PM (Th)  |             Hybrid            |   https://docs.google.com/spreadsheets/d/1SrQU4Djbvn3jYOR-CHTfqc-uMraFlHi7x0UpEFV7TbU/edit?usp=sharing  |

## Asynchronous Communication

For any questions outside of office hours: Please post to the class Piazza. If it is a sensitive topic, you can post only to the teaching staff. Please do not message me directly unless it is an emergency. I may not respond. 

If your question is more general, make it visible to the rest of class. If it isn't clear if it is a sensitive question or not, please start out by making the question to the teaching staff and we can advise on making it public or not. Feel free to answer questions that your classmates post or freely participate in discussions there.

Please do not email us individually. Those emails get buried, or they might not be seen by the right member of the teaching staff. This especially applies to grading questions; if you have questions about your grade do *not* email a grader directly. Write a private post on Piazza.

We will strive to reply to homework questions and discussions within 24 hours. Do not plan on, or expect help, outside of regular business hours (after 5 pm or weekends)

## Homework:

There will be one assignment per module, for a total of 5 homeworks.

We plan to redesign our homework setup to account for the large class. We aim to use github classroom with automatic feedback. Because this is a new setup, there may be some friction getting started. We appreciate your patience and understanding. I will update the class as we make progress.

While we don't have all the details yet, we will provide a docker for you to develop in. We plan to enable a git-based workflow where you push your current solution to a repo and receive feedback from a server. You will be graded on the server feedback rather than the results from your own machine. This is to help provide fair (and scalable) grading across the increasing diversity of devices that everyone has these days. Someone with an M1 processor will get very different results than someone with an Intel X86 processor.

_Architectural differences are very interesting to discuss and I hope we can have detailed discussions about how your machine's results differ from the server on Piazza_

Homeworks are due at midnight on their due date, but do not plan on help after 5 pm. You will have 10 days for each assignment. You have an additional 4 days to turn homework in late without penalty. After that, late work will not be accepted. 

## Tests:

There will be two asynchronous tests in this course: a midterm and a final. The midterm will be worth as much as a single homework assignment (10%). The final will be worth 30%.

You will get the test as pdf worksheet when it is assigned. You must turn it in by the due date. No late tests will be accepted. You have 1 work-week (5 days) for the midterm, and you have 12 hours for the final. 

The midterm will be given halfway through the class: assigned on Monday, Feb. 13 and due on Feb. 17. 
The final will be given on Wednesday, March 22.

I will design the tests to take ~180 minutes. These are open note/book/internet tests. However, it is not open friend or question. That is, while the test is active, you are not allowed to discuss the test with another person (either in the class or online). For example, you *can* google concepts that are on the test. You *cannot* post a test question to stackoverflow. You cannot use any AI assisted tool (ChatGPT or Github co-pilot) to help with the tests.

_a note on timing_: my tests are designed to take 180 minutes *if* they were given in-person. In practice, students take much longer on take-home tests because you can spend time validating answers and less time studying beforehand. Because of this, many students spend much longer on take-home tests. Please consider this when budgeting time.

## Late Policy:

You have 4 free late days for each homework assignment. No homework will be accepted after that.

The midterm and final will *not* be accepted late.

## Grade Breakdown

- Attendance/Quiz: 10%
- Homeworks: 50% (10% each)
- Midterm: 10%
- Final Exam: 30%

If you want to discuss a grade, please contact the teaching staff no later than 1 week after the grades are posted.

## Academic Integrity

One of the joys of university life is socializing and working with your classmates. I want you to make friends with each other and discuss the material. 

**That said, I expect all assignments (code, write-ups, and tests) to be your own original work.**

If you work together with a classmate on an assignment, please mention this, e.g. in the comments of your code. If you use a figure you didn't create in a write-up, then it needs a citation. Please review the [universities policy on plagiarism](https://guides.library.ucsc.edu/citesources/plagiarism)

This class has a zero tolerance policy on cheating. Please don't do it. I would much rather get a hundred emails asking for help than have to refer anyone for academic misconduct.

As a final note on cheating: the economic condition facing computer science graduates is volatile in the near future. It is crucial that you spend your time at University learning the material deeply. If you cheat, you will not be able to stand out from your colleagues that put in the effort when it comes time to find a job. Cheating will have an devastating and unforgiving impact on your immediate career opportunities. Don't do it.  

## Privacy

I plan to record lectures in class. Please be aware that:

- Things you do or say will be recorded. I doubt that this will be an issue, but if you want me to remove any part of the recording, please just let me know.
- Many forums (e.g. zoom chats, Piazza posts, etc.) chats are not private. Please be respectful and kind and assume everyone can see what you are typing.

## Using AI Tools

We are in an exciting time for AI. You have surely seen tools such as Github co-pilot and ChatGPT. These tools have incredible potential and they are improving every day. 

However, the educational community has not had sufficient time to understand the impact they will have on learning objectives. This class has been designed to be taken *without* the use of AI tools. If you use them for your assignments (or especially tests), it will be considered academic misconduct. To be clear: it is not acceptable to use the tools and modify the AI output. Just do not use the tools at all when doing coursework for this class.

For those of you who are interested in exploring such tools, I will provide the following option to you (only for the homeworks):

*after* you have completed the assignment, you can use the AI tools to see how they could help solve the problem. Please submit a non-AI version of the assignment first. Afterwards, try to use the AI tools. Write several paragraphs explaining how you approached the tools, what prompts you used, what the tools suggested, and if the tools were correct or incorrect. 

Submitting this extra report can provide up to 5 points extra credit (not to exceed 100%) on each homework assignment. There is no rubric for the extra credit and points will be given at our discretion.

## Acknowledgements

This page is based off of Professor [Lindsey Kuper](https://users.soe.ucsc.edu/~lkuper/)'s CSE232, Fall 2020 website
