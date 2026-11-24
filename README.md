# LLM games

Open an agent in the project where you want work done. Give it the URL of
this repository and tell it what you want to accomplish.

> Read and follow the LLM games instructions at REPO_URL to fix the
> confusing error messages in this project. You can decide how to approach it.

**For the receiving agent:** read [readme.txt](./readme.txt) from this
repository, remotely or from a temporary checkout. For an action request,
first save those instructions and the task agreement in the user's working
project, then carry out and verify the work there. Choose the participants and method for decisions the
user delegates. For a discussion request, talk it through before setup.

Each task gets its own record under `.llm-games/<task>/` at the root of the
working project. A `stop` file anywhere inside that task directory halts
that game alone.

To share a game's history, commit its task directory. To keep untracked game
records private to your clone, add `/.llm-games/` to `.git/info/exclude`.
For a team-wide ignore rule, use the same pattern in the root `.gitignore`.
