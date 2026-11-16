# AI-Study-Check

## Purpose
This offline interactive prototype explores overreliance on AI-generated answers during exam revision. It is a demonstration of two advice-presentation designs, not a live AI service or a validated experiment.

## How to run
1. Download and extract the ZIP file.
2. Open `index.html` in Chrome, Edge, or Firefox (double-click it).
3. Select one of the two versions and choose **Start demonstration**.
4. Complete three multiple-choice questions and review the feedback.
5. Select **View summary** and optionally **Download session JSON**.
6. Use **Restart / choose other version** to test the alternative version.

No installation, server, internet, account, or API key is needed.

## Source code
All source code is included in `index.html`:
- HTML: page structure and interactive elements
- CSS: styling and responsive layout
- JavaScript: question data, navigation, AI suggestions, feedback, summary, and JSON export

Open `index.html` with a text editor (e.g. VS Code) to inspect or modify the code. The HTML file is **not** merely a screenshot.

## Interaction versions
**Answer first, then see AI advice:** Participants give an independent answer, see the simulated AI suggestion, and then give a final answer. The app records both answers, so it can count changes.

**See AI advice immediately:** Participants see the simulated AI suggestion before their answer and then give a final answer. No independent initial answer is collected. It is therefore not possible to measure an individual's answer change in this version.

## Questions and simulated AI
The prototype uses three fixed exam-revision questions (silhouette score, overfitting, and imbalanced-class accuracy). The AI suggestions are **prewritten simulations**, not live AI-generated responses. Two suggestions are intentionally incorrect and one is correct. Correct answers are predefined for the demonstration.

## Session data
The **Download session JSON** button exports the selected version and the three responses. Option indexes are zero-based (`0` = A, `1` = B); `initial: null` means no independent answer was collected.

The app does not automatically send results to a server. The downloaded file remains wherever the user saves it.

## Evaluation limitations
- Comparing final-answer accuracy across the two versions is possible, but independent-to-final answer changes are measurable **only** in the answer-first version.
- Three fixed questions and a single demonstration session are not sufficient to establish a causal effect or generalise to students.
- Repeating the same questions in both versions introduces practice and memory effects.
- Fixed simulated AI suggestions do not measure real-time AI reliability.
- To evaluate effectiveness, recruit participants, counterbalance or randomise version order and question sets, and define accuracy and advice-following measures before testing.

## Suggested demonstration
Show one question in each version, then display the summary and downloaded JSON. Explain how the interface presents AI advice at different times and what the recorded responses can and cannot show.
