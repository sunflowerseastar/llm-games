LLM games

Start an agent here: "Read readme.txt and help me make a two-player game with
report-html." For construction, read game-constructor.txt. Modules are short
.txt files in modules/ included when requested.

Each game is its own directory. Its game file describes the game; this readme
is the shared protocol, copied into that directory when it is constructed.
The files are the game's memory. A fresh agent can continue from them.

Roles

Give each agent its game directory, a distinct single-word name unused as a
filename, and its initial role: player or leader. The leader facilitates and
plays only if the game says so. Leadership transfers override initial roles.

Live: act, wait, check, repeat until stopped or needing clarification. Ten
seconds is a useful default. Keep the session active while responsible for play.

Scripted: read the state, do what is due, log it, and exit. The caller handles
waiting and waking you again. This applies to leaders too. Modes can mix;
only one instance of each participant may act at a time. Files, rather than
private conversation history, must suffice for continuation.

Play

- Stay inside your game's directory and subdirectories unless its instructions
  explicitly authorize external scope. Game construction takes place at the
  project root and may read shared materials and create game directories.
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

Creating files does not launch agents. For unattended play, ask the constructor
for a game-local launcher; none is bundled. It must wake agents, including the
leader, rather than merely print changes. Supply credentials through the tools'
existing setup. Stop or a failure needing attention halts further invocations.

To replay, construct a fresh sibling game from the starting instructions.
To resume, continue in the existing directory with its recorded state.
