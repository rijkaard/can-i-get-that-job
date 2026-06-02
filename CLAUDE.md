
This project helps candidates apply to jobs.

When you are asked to help with a job application, the following steps must be followed:

- detailed critique of spec vs applicant's expertise
- back and forth with the applicant to agree on a strategy, what to highlight, if and how to frame weak spots, etc.
- cover letter
- job-specific cv - create a modified copy of one of the reference html resumes under cv/ to match the narrative for the current spec, highlighting relevant skills and competences

Project structure:

- cv/ **never modify** contains one or more resume
- cv-projects/ **never modify** contains several files, each listing a type of projects I 
- voice/ **never modify**  contains examples of writing from the candidate
- specs/ **never modify** contains job specs; if the user points at a job spec outside this directory, proceed but ask the user to move the spec in your next interaction
- tasks/ contains the details of a job application and all the intermediate results; you are responsible for creating a new sub-directory and copying the job spec there
- LOG.md contains timestamped, single-line summaries of each step executed; it can point to other files for details
- TASKS.md contains single-line sets of tasks to be executed; it can point to a job specs/ and a file under tasks/ for details
- updates/ contains potential updates to cv and and projects should any surface while interacting with the applicant; **never** modify files under cv/ or cv-projects/, **always** add a file under updates/

Prefer spawning separate agents to execute each step: your task is to act as a relay.
Each agent must write its work to a relevant file under tasks/<subdir>
Since each step builds on the previous ones, point the agent to the relevant files.
Update LOG.md and TASKS.md frequently.


Should disaster strike, a new agent pointing to this directory **must** be able to resume the work, at most repeating the step that was interrupted.
