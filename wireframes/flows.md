# User flows (draft for review)
Version: v1 · Date: 2026-11-09 · Time: 10:26 · Created by: Claude

Sources: brief.md, claude/problem-statement.md, claude/persona.md, claude/solution.md. All participant evidence is simulated class practice data, not real evidence. External research is about other people and organizations, not Shelfwise users. Flows describe what the persona does, not screens.

Symbols: oval = start or end, rectangle = step, diamond = decision, parallelogram = person enters something, dashed = unhappy path.

## Flow A · Stock keeper
Goal: get a delivery from the cartons into the app correctly. This is our reading of F1 to F5, not a stated goal (persona.md).
Chosen directions: 1.3 and 2.2 (solution.md).

Entry point: a supplier delivery arrives (brief.md, F1 to F5).
1. Brings the cartons to where the app is (solution.md 1.3).
   Unhappy path: the stock can't be moved, so counting happens away from the app the old way. Exit (persona.md; solution.md 1.3, "Against it").
2. Opens the order for this delivery (brief.md F1).
3. [enters] Counts one item and enters the number that arrived; it is saved right away (solution.md 1.3, 2.2).
4. [decision] Interrupted?
   Unhappy path: leaves, comes back and continues from the last saved item, back to 3 (solution.md 2.2).
5. [decision] More items left? Yes: back to 3.
6. [decision] Any difference from the order? Yes: hand over to Flow B. Who records it: I don't know (persona.md).
7. Confirms the delivery (brief.md F5).

End point: stock is updated from a real count.
Reason: 4 of 5 were interrupted while counting, and P4 counts and records at the desk at the same time (solution.md 1.3, 2.2).

## Flow B · Shop owner
Goal: stock in the app matches real stock after a delivery (persona.md).
Chosen direction: 3.1 (solution.md).

Entry point: a delivery has a line where what arrived differs from the order. It comes from Flow A step 6, or the owner received it; I don't know which (persona.md).
1. Opens the delivery with the difference.
   Unhappy path: the owner is never told about it; I don't know what happens. Exit. Keeping open differences in view (3.2) was not chosen (solution.md).
2. [decision] What kind of difference: short, extra, damaged or wrong? (problem-statement.md, Problem 3)
   Unhappy path: the kind doesn't fit, so only a number is recorded and the reason is lost. Exit (problem-statement.md, Problem 3).
3. [enters] Enters the kind together with the number (solution.md 3.1).
4. [decision] More differences? Yes: back to 2.
5. Confirms the delivery (brief.md F5).

End point: each difference keeps its reason in the delivery record. Follow up with the supplier is outside the chosen direction (solution.md; 3.2 and 3.3 not chosen).
Reason: P1, P3 and P5 recorded only a number, while P4 writes what happened in the notes (solution.md 3.1).

## Open points
- How the owner learns about a difference: I don't know. Direction 3.2 was not chosen (solution.md).
- Whether Flow A and Flow B are done by the same person: I don't know. No role is given for P1 to P5 (persona.md).
- Both flows rest mostly on one simulated participant, P4 (solution.md).
