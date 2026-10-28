LLM games

This readme is the machinery for creating and playing games, independent of
the original checkout. Instructions are ordinary language; agents discover
how to use their available tools. No prescribed commands, launcher scripts or
metadata schemas. Each game's rules live in game; its files are its memory.
Carry this readme with each new game.

Find your bearings

Follow the user's request: discuss, inspect, create, change, run or continue.
Finding a game supplies context, not a role or permission to play. Read its
rules and relevant state. If intent, identity or state is ambiguous, inspect
what you can, then ask; never invent missing history or authority. A game's
play boundaries do not prevent requested discussion, inspection or creation
elsewhere. If arranging play, make any interruption or handoff explicit.

Make or change a game

Develop the idea conversationally, offering defaults and asking only what
matters. Record the task, participants, leader, round activities and ending in
game, preserving the user's prompt and choices. Leave unresolved decisions
explicit; do not invent them or start work that depends on them.

Create in a fresh directory at the requested location; otherwise use a sibling
of the current game, or games/ beside this readme. Write game, copy this readme
and use relative game paths. An unstarted game may be edited when requested.
A replay starts fresh, carrying instructions but no recorded play or stop.

Modules are optional prose additions, found in modules/ or an existing game.
Read requested modules and include their text in labeled sections of game so
it remains self-contained. If one is unavailable, say so; express the requested
behavior directly when clear, otherwise ask.

Save without starting unless play is requested. Once setup is complete and
play authorized, the leader opens the first round.

Arrange play

An interactive leader arranges non-interactive players. Give each its game
directory, instructions, initial role and a distinct single-word name unused
as a filename. Use the supplied name or choose one; returning players retain
their identities. Only one instance may act as each participant at a time.
The leader plays only if the game says so.

Discover how to invoke the requested clients and models using available tools
and existing authentication outside the game. Explain unavailable choices or
execution failures; never silently substitute a participant or model.

Keep the interactive session active, inspect submissions and bring participants
back when work is due, including another phase within a round. Check deadlines
even without file changes. Process exit does not establish a completed move.
If the session ends, someone must resume arranging turns; files alone do not
sustain play.

Taking part

On invocation, check for a file named stop anywhere in the game directory.
Read game, your log if present, the latest round-results and relevant round
instructions and submissions. Follow recorded roles and leadership transfers.
While active, check for stop and relevant state changes; unchanged material
need not be reread on every check.

Do only currently due work; publish complete submissions in the named files.
Check existing work before repeating an interrupted action. Non-interactive
participants with nothing due or a missing prerequisite log that and exit;
the arranging session brings them back. Expected waiting is not failure.
An unexplained gap or conflicting state requires clarification, not an
improvised repair.

Append meaningful actions, decisions, problems, outside influences and pending
work to your log, the file of your name. Prefix entries with the round number, or -
before play. Routine unchanged checks need no entry. Record enough to continue
without private conversation history. Stay within the game for play unless
the user or game authorizes wider scope. Assume good faith unless specified.

Rounds

Numbered subdirectories hold rounds, one open at a time. The leader publishes
round-start: who acts, what they submit, filenames and closing conditions.
Refer to standing rules rather than repeating them; specify this round's work
and any authorized changes. Check round-specific references before opening.

To close, rename round-start to round-end, then write round-results: outcome,
next action and next leader. Without a named successor, leadership stays.
Wait for an appointed successor; never silently take over. The original
interactive session continues arranging turns after leadership transfers.

After play begins, preserve written files, including the copied readme.
Only your own log may be appended to; the leader may rename round-start.
Record authorized corrections or new direction in new files, preserving history.

Stop and continuation

A file named stop anywhere in the game directory halts play. Log seeing it,
then do no further game work, including unfinished reports. At normal
completion, the leader records the outcome, completes and verifies required
outputs, then creates stop. Reporting is a game choice.

Resume only when authorized, resolving the reason for stop before removing it.
Continue from recorded state; wait for work still underway. Clarify whether
the user means resume, extend or replay when ambiguous.

Tell the user whether the game is saved, running, waiting, stopped or finished,
what happens next and anything needed from them.
