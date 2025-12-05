# Research Methodology

---
<br>
<br>


## Problem-driven research
---

PhD research means finding an important open problem and making significant progress towards solving the problem. Using the right methodology is key in this process, and this is one of the central learning outcomes of your PhD journey.

New students, having read many recent papers with exciting results, will often want to start right away with working on new methods to achieve similarly exciting results. There is typically a strong focus on method design and testing. What is often lost in the process is due consideration for the underlying problem that the method should address. Such work typically ends up with a vaguely defined problem and a method that lacks clear justification; it's not clear why the method is useful and what problem it actually solves. I call this approach "methods-driven tinkering".

In contrast, problem-driven research starts with identifying the actual problem before attempting to find new methods. This involves answers to the following questions:

Problem: What specific technical problem does your research address? Motivation: Why is this problem important? (What can a solution to the problem enable us to do?) State of research: Why are current methods unable to solve the problem? (technical limitations, assumptions, etc) Contribution: How does your proposed method address the problem? It is important to put significant thought into these questions, including writing it down formally, as this will frame your search for a method as well as how you evaluate it.

You can further maximise the impact of your work by exploring new problems which are significantly different from prior work. For example, if there is a widely-used but limiting assumption in the literature, your research could be the first to attempt to eliminate or relax this assumption. Exploring new problems can maximise your impact because others may follow your direction, in which case they are likely to cite your work. In contrast, it is relatively less exciting to work on iterative improvements, i.e. "doing more of the same", which may be easily overlooked (or ignored) by others in the field.

<br>


## Finding open problems and challenge tasks
---

My advice for finding open problems and challenge tasks:

Read: Start by reading papers in your area. In the process, try to identify limitations in existing algorithms, such as restrictive assumptions in the used models and algorithms. Assumptions in evaluation settings may also hint at limitations of the algorithms. Try to identify common limitations across algorithms to maximise the relevance and impact of your work. Survey papers often contain sections on open problems which can give useful inspiration. Once a technical problem has been identified, try to formulate challenge tasks which require a solution to the problem.

Play: Implement a collection of state-of-the-art and/or baseline algorithms in the field and test them on some recent benchmark tasks. By using these algorithms to solve difficult tasks, you will gain a deeper understanding of their inner workings and their limitations, some of which may not be apparent from their original papers. Based on this experience, try to identify important open problems and new challenge tasks, for example by modifying the tested benchmark tasks to highlight the open problem.

Talk: Seek out and use opportunities to talk about your research and the research of others, whether in informal chats or formal presentations (e.g. group meetings, institute seminars, conferences/workshops, etc). Talking about your work requires you to express your ideas in a clear and succinct way, and is an important channel to get feedback and suggestions from others. It often happens that PhD students bury themselves in their work, which carries a risk of missing out on useful ideas; talking with other people is one way to avoid that.


<br>

## Experimental evaluation
---

Systematic evaluation is a central element of a research methodology. Much of the research in our group is empirical, which means that claims and hypotheses are tested in practice.

An important question to consider is what evaluation tasks to use. The choice of evaluation tasks should be guided by your open problem, in that a solution to the problem is required to successfully complete the tasks. I call such tasks challenge tasks because they allow you to say "this task cannot be solved (well) with current methods due to the open problem". Using a non-contrived, ambitious challenge task gives your research a stronger justification and can force you to think outside the box to find novel ideas.

When designing experiments, try to have specific questions in mind that the experiments should answer. For example:

How does your method compare to other methods? (e.g. rewards, accuracy, sample complexity, compute time) How does your method scale in certain dimensions? (e.g. number of agents, actions, states) What is the contribution/effect of different components in your method? (ablation study) How does your method perform if certain assumptions are violated? If you observed a specific result and have a hypothesis to explain the result, you may want to design additional experiments to specifically test your hypothesis.

The use of baselines is crucial to set the bars for what constitutes good and bad performance. There are generally three kinds of baselines:

Best-case/worst-case: Best/worst-case (or upper/lower) baselines are useful to show the margin of possible improvement. Best/worst can mean different things depending on your work. For example, a best-case may be an exact method with "unlimited" compute time, or with access to privileged information that would normally not be available. A worst-case may be a method that is limited or basic in some specific sense. Alterations/ablations: If your method consists of several interacting components, it is important to show the effect of each component. For example, these may be elements of your network architecture and input, loss functions, or other sub-functions in your method. Ablation studies take your full method and remove or alter certain elements to show the performance under these ablated/altered versions. State-of-the-art: If suitable, it can be a good idea to include some recent state-of-the-art algorithms for comparison. Ideally, each algorithm should use hyper-parameters that were optimised for that algorithm specifically (rather than using the same hyper-parameters for all algorithms), to maximise performance of each algorithm. Importantly, try to think of sensible baselines early in your research rather than as an afterthought.

Once you have results from your experiments, you should use the right tools to understand the data. Use good visualisation, including second-order statistics (e.g. standard deviation/error). Statistical hypothesis tests should be used to establish whether observed differences are significant or due to variance. It is crucial to understand the meaning of statistical significance and how to apply such tests correctly. This guide on experimental design in RL research (and this guide on hypothesis testing) is a useful starting point.


<br><br>
<center><b><font color="red">THIS WEBSITE IS INTENDED EXCLUSIVELY FOR INTERNAL USE BY OUR TEAM.</font></b></center>
<!-- <center><b><font color="red">This website is intended exclusively for internal use by our team.</font></b></center> -->
