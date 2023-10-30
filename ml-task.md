### ML Task: Design an AI Solution for Sales Optimization

#### Objective:

Your task is to design and document an AI-driven solution aimed at achieving the following specific outcomes:

1. **Predict Deal Outcomes**: Forecast whether a deal will close as "WON" or "LOST" based on interactions and other variables at each stage of the sales process.

2. **Identify Bottlenecks**: Analyze the sales process to highlight stages where deals are most likely to stall or fail.

3. **Salesperson Performance**: Provide a metric to evaluate the performance of each salesperson based on their ability to move deals through the sales pipeline.

4. **Managerial Insights**: Generate summaries and actionable insights for sales managers to improve team performance.

#### Background:

Our sales team follows a structured process with the following stages:

- Solution Presented
- Proposal
- Decision Maker Call/Pitch
- Verbal Commitment
- Negotiation
- Free Trial
- Paid Trial
- Contract Sent
- Closed (WON)

**Note**: A deal can be marked as "LOST" at any stage in the process, not just after the "Contract Sent" stage.

Multiple types of interactions occur at each stage, through channels such as email, voice calls, and video calls. Each deal is primarily overseen by a single salesperson but can involve additional team members and professionals from other departments based on the deal’s complexity. We have access to the contents of all emails sent and received and transcripts of voice and video calls made during the sales process.

#### Data Available:

- Email contents (text)
- Transcripts from voice and video calls (text)
- Deal size (numerical)
- Sales stage timestamps (datetime)
- Salesperson assignment history (text)

#### Deliverables:

1. A written document outlining:

   - The approach and methodology you would take for data preprocessing, feature extraction, and model selection.
   - Evaluation metrics for the success of the AI solution.
   - Any limitations or challenges you anticipate and how you would address them.

2. (Optional) A simplified code snippet or pseudocode to demonstrate key steps in your proposed pipeline.

3. A short presentation to walk us through your proposed solution.

#### Evaluation Criteria:

- Innovation and creativity in approach
- Practicality and feasibility of the solution
- Clarity and comprehensiveness of the written document
- Ability to articulate thoughts during the presentation
