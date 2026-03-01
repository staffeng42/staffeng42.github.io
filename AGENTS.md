Agents registry

This repository includes an interactive blog-writing agent useful for creating French blog posts and opening a PR for review.

- .github/agents/blog-writer/agent.py — interactive CLI to create a new post, copy images, run a local build (`npm install && npm run build`) and open a PR via `gh`.
- See .github/agents/blog-writer/README.md for usage and requirements.

Agent defaults
- Posts in French, author Staff42, images under `assets/images/posts/`, branch `post/YYYY-MM-DD-short-title`, PR title `Add post: <title>`.

To modify or extend the agent, edit the Python script and README in `.github/agents/blog-writer/`.
