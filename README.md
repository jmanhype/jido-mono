# Jido Monorepo

This monorepo contains all the Jido agent framework packages as Git submodules:

- **jido** - Core Jido agent framework
- **jido_action** - Action system for Jido agents
- **jido_signal** - Signal handling for Jido agents
- **jido_workbench** - Development workbench for Jido
- **req_llm** - LLM request handling
- **llm_db** - Database integration for LLMs

## Structure

Each package is added as a Git submodule, maintaining its connection to the original agentjido repositories.

## Getting Started

Clone the monorepo with all submodules:

```bash
git clone --recurse-submodules https://github.com/jmanhype/jido-mono.git
```

Or if you've already cloned it:

```bash
git submodule update --init --recursive
```

## Development

Each submodule remains tied to its original repository:
- Changes in submodules can be pushed back to their original repos
- Updates from original repos can be pulled into submodules
- Each package maintains its own git history

### Updating a submodule

```bash
cd jido  # or any other submodule
git pull origin main
cd ..
git add jido
git commit -m "Update jido submodule"
```

### Updating all submodules

```bash
git submodule update --remote --merge
```
