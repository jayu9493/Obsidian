- Root cause analysis (RCA) is the process of discovering the root causes of problems in order to identify appropriate solutions.
- Root cause analysis can be performed with a collection of principles, techniques, and methodologies that can all be leveraged to identify the root causes of an event or trend.
- **The first goal** of root cause analysis is to discover the root cause of a problem or event. **The second goal** is to fully understand how to fix, compensate, or learn from any underlying issues within the root cause. **The third goal** is to apply what we learn from this analysis to systematically prevent future issues or to repeat successes.
### Eight Techniques to do Root Cause Analysis(RCA):
 1. Pareto Charts 
 2. Ishikawa Fishbone Diagram 
 3. 5 Whys
 4. Failure Mode and Effect Analysis (FMEA) 
 5. Fault Tree Analysis 
 6. 8D Report Template Checklist
 7. DMAIC Template
 8. Scatter Diagram
---
#### Pareto Chart:
- This is basically bar graphs.
##### 80/20 Rule – The Pareto Principle
- The 80/20 Rule (also known as the **Pareto principle** or the law of the vital few & trivial many) states that, for many events, roughly 80% of the effects come from 20% of the causes.
- [[Pareto-Chart-Excel-Template.xls | format excel file for pareto chart]]
- 
- ![[Pasted image 20240904000007.png | center | 500]]
---
#### Fishbone Diagram:

- It is also known as Ishikawa diagram or Cause-and-effect diagram.
- It is a visual representation that helps identify and categorize potential.
- It resembles a fish skeleton, where the problem is placed at the head of the fish, and the main causal categories are represented as the fish's bones or branches. branches includes categories such as people, process, equipment, materials, environment and management.
##### Steps of fishbone diagram tool:
step 1. define the problem --> place the problem statement at the head of the fishbone diagram.
step 2. Identify the main Categories --> Draw the main branches, such as people, process, equipment, materials, environment and management.
step 3. Analyze potential causes --> Under each branch, brainstorm and add potential causes relevant to the problem. 
step 4. Drill down to sub-Causes --> Add sub-causes under each main cause to explore the root cause.
![[Pasted image 20231022133652.png | center |500]]

---
#### FEMA(Failure Mode and Effects Analysis):

- The failure mode and effect analysis, focuses on failures that happen within a particular system. This is  not most popular method but effect in maintenance POV.
- If you have established every single failure in a system, you will then analyze them one by one to understand the consequences of these failures.
![[Pasted image 20240917231242.png | Test  | center | 600 ]]
- One of the first steps to take when completing an FMEA is to determine the participants. You need the right people with the right experience. This could include process owners and designers. All qualified personnel should be involved to catch potential failure modes. Practitioners also should consider inviting customers and suppliers to gather alternative viewpoints.
- Once the participants are together, the brainstorming can begin. When completing an FMEA, it’s important to remember **Murphy’s Law: “Anything that can go wrong, will go wrong.”** Participants need to identify all the components, systems, processes, and functions. Any of these factors could potentially fail to meet the required level of quality or reliability. The team should not only be able to describe the effects of the failure but also the possible causes.
##### Criteria for analysis:
- An FMEA uses three criteria to assess a problem: 
	1. the severity of the effect on the customer, 
	2. how frequently the problem is likely to occur
	3. how easily the problem can be detected.
-  Participants must set and agree on a ranking between 1 and 10 (1 = low, 10 = high) for the severity, occurrence, and detection level for each of the failure modes. Although FMEA is a qualitative process, it is important to use data (if available) to qualify the decisions the team makes regarding these ratings.

|      **Description**       |      **Low Number**\|      |      **High Number**      |                                **Notes**                                 |
| :------------------------: | :------------------------: | :-----------------------: | :----------------------------------------------------------------------: |
|        **Severity**        |       **Low impact**       |      **High impact**      |                      **Rank the impact of failure**                      |
| **Probability of Failure** |    Not likely to occur     |        Inevitable         | Rank the probability of a failure occurring during the expected lifetime |
|       **Detection**        | Very likely to be detected | Not likely to be detected |     Rank the probability of detecting the problem before it happens      |
|                            |                            |                           |                                                                          |

- After ranking the severity, occurrence, and detection levels for each failure mode, the team will be able to calculate a risk priority number (RPN). The formula for the RPN is:
<div style="text-align: center; font-size: 14px; font-weight: bold;">
RPN = severity x occurrence x detection
</div>
- Once all the failure modes have been assessed, the team should adjust the FMEA to list failures in descending RPN order. This highlights the areas where corrective actions can be focused. If resources are limited, practitioners must set priorities on the biggest problems first.
- When the priorities have been agreed upon, one of the team’s last steps is to generate appropriate corrective actions for reducing the occurrence of failure modes, or at least for improving their detection. The FMEA leader should assign responsibility for these actions and set target completion dates.
---
#### Fault Tree Analysis:

- **Fault tree analysis** (**FTA**) is a type of [failure analysis](https://en.wikipedia.org/wiki/Failure_analysis "Failure analysis") in which an undesired state of a system is examined. This analysis method is mainly used in [safety engineering](https://en.wikipedia.org/wiki/Safety_engineering "Safety engineering") and [reliability engineering](https://en.wikipedia.org/wiki/Reliability_engineering "Reliability engineering") to understand how systems can fail, to identify the best ways to reduce risk and to determine (or get a feeling for) event rates of a safety accident or a particular system level (functional) failure
##### Performing the fault tree analysis:

- **Step 1:** Define the undesired event: Event should be specific and measurable, like a component failure or a system malfunction. It’s also important to define the event in clear, consistent terms, since it serves as the starting point for your fault tree diagram.
- **Step 2:** Identify the contributing events and factors: Contributing factors tend to fall into two broad categories: basic events and intermediate events.
	1. **Basic events** - those events that cannot be further broken down into simpler events
	2. **Intermediate events** - located between the lower-level basic events and the top event (the primary undesired event being analyzed). Intermediate events are caused by other events in the fault tree and, in turn, cause other events.
- **Step 3:** Construct the fault tree - Using standard gate symbols and event symbols, construct a graphical representation of the relationships between the undesired (or output) event and its contributing factors (also called input events).
	- The fault tree should be organized hierarchically, with the undesired event at the top and the contributing factors branching out below it.
	- There are two main types of logic gates used in fault trees: **AND gates** and **OR gates**.
		- **AND gates**: Use AND gates when all contributing events must occur simultaneously for the undesired event to occur.
		- **OR gates**: Use an OR gate when any one of the input events is sufficient to cause the output event. In other words, the output event happens if at least one of the input events connected to the OR gate happens.
	- Though less commonly used, **NOT gates**, **XOR gates**, **K/N gates** and **INHIBIT** **gates** can also help identify specific relationships between input and output events.
		- **NOT gates**: NOT gates represent the inverse of an input event. If the input event does _not_ occur, the output event will occur.
		- **XOR gates** (Exclusive OR gates): Use an XOR gate when exactly one of the input events must occur for the output event to happen.
		- **K/N gates:** K/N gates, also known as voting gates or threshold gates, are used when a specific number of the input events (K) out of all the possible input events (N) must occur for the output event to happen.
		- **INHIBIT gates**: Like an AND gate, an INHIBIT gate indicates that an output event will occur if both input events and a conditional event (a condition or restriction that can apply to any gate) occurs.
- **Step 4:** Gather failure data -  you calculate the probability of the undesired event occurring and identify the most critical contributing factors. Use either a qualitative or a quantitative data analysis method.
	- A qualitative analysis focuses on understanding the structure of the fault tree, the relationships between events, and the identification of critical paths and minimal cut sets (the smallest set of events that can create the undesired event). Qualitative analysis can help prioritize remedial actions and identify areas for further investigation.
	- A quantitative methodology, on the other hand, involves calculating the probability of the undesired event occurring based on the failure probabilities of the basic events. Quantitative analysis can help inform risk management decisions and evaluate the effectiveness of proposed improvements.
- **Step 5:** Perform the analysis
- **Step 6:** Interpret the results
- **Step 7:** Implement improvements and monitor progress
##### Example of fault tree analysis:
![[Pasted image 20240918160031.png | center | 600]]

---
#### 8D Report Template Checklist:
- 8D stands for the eight disciplines you will use to establish an 8D report, First introduced by [Ford](https://en.wikipedia.org/wiki/Eight_disciplines_problem_solving), the 8D method offers a consistent way of identifying a problem and solution, making it optimal for organizational learning. Many different fields use this method to aid in product and process improvement.
- These are the points for 8D Report Template Checklist.
- **D0:** "Recognize and define the problem."
- **D1:** "Form a cross-functional team."
- **D2:** "Describe the problem clearly."
- **D3:** "Implement immediate containment actions."
- **D4:** "Identify and verify the root cause."
- **D5:** "Determine permanent corrective actions."
- **D6:** "Implement and validate corrective actions."
- **D7:** "Establish preventive measures to avoid recurrence."
- **D8:** "Close the report and recognize team efforts."
- __[[8D-Problem-Solving-Checklist.pdf]]__
---
####  DMAIC Method:

- DMAIC means # Define, Measure, Analyze, Improve, Control.
- **Step 1 – Define:** The [Define](http://www.dmaictools.com/dmaic-define "define phase") phase is about developing a focused problem statement that describes in measurable terms what the project will deliver.
- **Step 2 – Measure :** The [Measure](http://www.dmaictools.com/dmaic-measure) phase is about documenting the current process and assessing baseline performance.  Some of the important tools in this phase include trend charts, basic [Pareto charts](http://www.dmaictools.com/dmaic-analyze/pareto-chart "pareto chart"), [_process flowcharts_](http://www.dmaictools.com/dmaic-measure/process-flowcharts), _Gage R&R_, and process capability measurement (sigma level, also referred to as _process sigma_)
- **Step 3 - Analyze:** The [Analyze](http://www.dmaictools.com/dmaic-analyze "six sigma analyze phase") phase in DMAIC isolates the _top causes_ behind the metric or [CTQ](http://www.dmaictools.com/dmaic-definitions#ctq "critical to quality feature") that the team is tackling.  In most cases there will be no more than three causes that must be controlled in order to achieve success – if too many causes are identified, then the team has either not isolated the primary causes or the project goal is too ambitious to achieve success with a single project.
- **Step 4 - Improve:** The [Improve](http://www.dmaictools.com/improve "DMAIC Improve Phase") phase focuses on fully understanding the top causes identified in the Analyze phase, with the intent of either controlling or eliminating those causes.
- **Step 5 - Control:** DMAIC’s [Control](http://www.dmaictools.com/control "DMAIC Control Phase") phase is about sustaining the changes made in the Improve phase.  The best controls are those that require no monitoring (irreversible product or process design changes).
---
#### Scatter Diagram:
- ![[Pasted image 20240918164930.png | center | 400]]
- 