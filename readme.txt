LLM games

In the machinery checkout, start an agent with: "Read readme.txt and help me
make a game." For construction, read game-constructor.txt. Modules are short
.txt files in modules/ included when requested, such as report-html.

The instructions themselves are the machinery. Use ordinary language and the
few file conventions below. Agents work out how to use their available tools;
the project does not prescribe commands, scripts, or metadata formats.

Each game is its own directory, independent of the machinery checkout. Its
game file describes the game; this readme is the shared protocol, copied there
at construction. The files are the game's memory. A fresh agent can continue
from them, even after the directory is moved.

Roles

Give each agent its game directory, a distinct single-word name unused as a
filename, and its initial role: player or leader. The leader facilitates and
plays only if the game says so. Leadership transfers override initial roles.

Start with an interactive leader and non-interactive players. The interactive
session arranges play and stays active until stopped or needing clarification.
Each player reads the state, does what is due, logs it, and exits. If waiting
on someone else, log that and exit; the session arranging play brings you back.
Only one instance of each participant may act at a time. Files must suffice for
continuation without private conversation history.

The game leader decides what happens in play; arranging turns is a separate
responsibility. If leadership transfers, the initial interactive session keeps
arranging turns, including for the new leader, without keeping the old role.

Play

- Stay inside your game's directory and subdirectories unless its instructions
  explicitly authorize external scope. During construction, read the shared
  materials and create the game in the user's chosen location.
- Rounds are numbered subdirectories, one open at a time. The leader opens a
  round by writing round-start: who may play, what to submit, the filenames,
  and when it ends. Follow those instructions.
- The leader closes the round by renaming round-start to round-end, then
  writes round-results: the outcome, what happens next, and who leads next.
  If no successor is named, the leader stays. If a successor does not act,
  the game waits; nobody silently takes over.
- Append each action, including reads and outside influences, to your own log:
  the file of your name. Prefix lines with the round number, or - before play.
- On every wake or check, read your log and the latest round-results, even if
  you have submitted. Follow any leadership transfer before acting.
- Setup drafts may be revised until the first round opens. After that,
  preserve written files; only your own log may be appended to, and the leader
  may rename round-start to round-end. Publish complete submissions. Changes
  of direction belong in subsequent instructions, not rewritten history.
- Check for stop anywhere under the game before acting. If present, do
  nothing further except log that you saw it. Resume only when it is removed.
- At normal completion, the leader records the outcome, finishes any outputs
  required by the game, then creates stop. An earlier stop means halt now,
  not permission to finish reports or other work.
- If the state is unclear or inconsistent, log the issue and seek clarification.
  Assume good faith unless the game says otherwise.

Running

Creating files does not start play. When asked to run a game, bring in the
requested players non-interactively using what is available here. Give each
its name, initial role, game directory and these instructions. Find out what
you can; ask only for what is missing. Use existing authentication and explain
unavailable choices rather than silently replacing a requested agent or model.

Follow the files to see what is due and what has been done. Bring participants
back when they have more to do, even within the same round. Check deadlines
even when no files change. A finished invocation is not proof of a completed
move. Keep play moving, honor stop, and bring failures needing attention to the
user. If the interactive session ends, play needs someone to resume arranging
turns; do not promise that it will continue by itself.

To replay, construct a fresh sibling game from the starting instructions.
To resume, continue in the existing directory with its recorded state.
