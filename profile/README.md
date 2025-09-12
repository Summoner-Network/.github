# Summoner Platform

<p align="center">
  <a href="https://summoner.org">
    <img src="https://summoner.org/static/images/summoner-logo.png" alt="Summoner Logo" width="160"/>
  </a>
</p>

<p align="center">
  <strong>Build, run, and coordinate autonomous agents over a WAN</strong>
</p>

<p align="center">
  <a href="https://summoner.org">Website</a> •
  <a href="https://discord.gg/kExRQ9S5">Discord</a> •
  <a href="https://twitter.com/SummonerNetwork">Twitter</a>
</p>

> **What is Summoner?**
> A modular runtime and SDK for networked AI agents. It lets you compose, run, and coordinate agents across machines. The Python client SDK pairs with a Rust server, and an optional desktop app provides a visual interface. Start with examples, then assemble your own SDK from modules.


## Table of contents

* [Start here](#start-here)
* [One‑minute tryout](#one-minute-tryout-examples-path)
* [Build an SDK from modules](#build-an-sdk-from-modules-recipes-path)
* [Desktop UI](#desktop-ui-optional)
* [Repository index](#repository-index)
* [Concepts in one page](#concepts-in-one-page)
* [Troubleshooting](#troubleshooting)
* [Contributing](#contributing)
* [Contact](#contact)

## Start here


<p align="center">
  <a href="https://summoner.org">
    <img src="../img/summoner_intro_rounded.png" alt="Summoner Logo" width="250"/>
  </a>
</p>

Choose the path that matches your goal. Each link points to a dedicated repo with its own README.

1. **Try examples quickly**

   * Repo: **[summoner-agents](https://github.com/Summoner-Network/summoner-agents)**
   * What you get: runnable agents that demonstrate the SDK patterns and messaging.

2. **Read the docs**

   * Repo: **[summoner-docs](https://github.com/Summoner-Network/summoner-docs)**
   * What you get: concepts, protocol sketches, and design notes.

3. **Build your own SDK from modules**

   * Repo: **[summoner-sdk](https://github.com/Summoner-Network/summoner-sdk)**
   * What you get: a template you customize via `build.txt` to assemble an SDK with the modules you choose.

4. **Use a desktop UI**

   * Repo: **[summoner-desktop](https://github.com/Summoner-Network/summoner-desktop)**
   * What you get: a visual interface for running agents and servers locally.

5. **Contribute a module**

   * Repo: **[starter-template](https://github.com/Summoner-Network/starter-template)**
   * What you get: a minimal module template you can publish and later include from `summoner-sdk` recipes.


## One‑minute tryout (examples path)

<details>
<summary>
<b>(Click to expand)</b> Pre-requisities and installation steps:
</summary>
<br>

**Prereqs**

* Python 3.11 or newer
* `git`
* macOS or Linux. Windows users can use WSL2 or git bash via VScode.

**Steps**

```bash
# 1) Get examples
git clone https://github.com/Summoner-Network/summoner-agents
cd summoner-agents

# 2) Set up the SDK and venv
source build_sdk.sh setup

# 3) Activate the venv
source venv/bin/activate

# 4) Install agent requirements
# If you want a single agent's deps:
pip install -r agents/agent_EchoAgent_0/requirements.txt
# Or install all agents' deps via the provided script if present:
bash install_requirements.sh

# 5) Run an agent
python agents/agent_EchoAgent_0/agent.py
```

If you opened a new terminal later, activate the venv again:

```bash
source venv/bin/activate
```

> 📝 **Note:** 
> Some agents have their own extra instructions in their README. Follow those when present.

</details>

## Build an SDK from modules (recipes path)

<details>
<summary>
<b>(Click to expand)</b> Use <b>summoner-sdk</b> to assemble your own SDK from a list of modules:
</summary>
<br>



```bash
# 1) Get the template
git clone https://github.com/Summoner-Network/summoner-sdk
cd summoner-sdk

# 2) Edit the recipe in build.txt
# Add one module name per line. Example:
#   summoner-agentclass
#   my-org/my-private-module@v0.2.1

# 3) Build and set up
source build_sdk.sh setup

# 4) Activate the venv
source venv/bin/activate

# 5) Start a sample server or client if provided by your module set
python user_space/myserver.py  # example entry point
```

**Developer branch options**
If you need the `dev` branch of `summoner-core` during setup, the script supports:

```bash
source build_sdk.sh dev_setup   # install using dev branch
source build_sdk.sh dev_reset   # reset then set up from dev branch
```

</details>

## Desktop UI (optional)

<details>
<summary>
<b>(Click to expand)</b> If you prefer a visual interface, use <b>summoner-desktop</b>:
</summary>
<br>

```bash
git clone https://github.com/Summoner-Network/summoner-desktop
cd summoner-desktop
# See repo README for Node.js requirements and run commands
```

</details>

## Repository index

| Repo                                                                         | Purpose                                                                                                      |
| ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **[summoner-core](https://github.com/Summoner-Network/summoner-core)**       | Core runtime components used by agents and servers. Python client SDK, Rust server implementation.           |
| **[summoner-agents](https://github.com/Summoner-Network/summoner-agents)**   | Example agents that exercise the SDK patterns such as `@receive` and `@send(multi=True)` and relay behavior. |
| **[summoner-docs](https://github.com/Summoner-Network/summoner-docs)**       | Conceptual documentation, design notes, and protocol outlines.                                               |
| **[summoner-sdk](https://github.com/Summoner-Network/summoner-sdk)**         | Template repo that assembles an SDK from modules listed in `build.txt`.                                      |
| **[summoner-desktop](https://github.com/Summoner-Network/summoner-desktop)** | Desktop application for running and inspecting agents and servers.                                           |
| **[starter-template](https://github.com/Summoner-Network/starter-template)** | Minimal template for authoring a new module that others can consume via `summoner-sdk`.                      |

**Summoner native modules (public)**

* **[summoner-agentclass](https://github.com/Summoner-Network/summoner-agentclass)**
  Adds security and orchestration features to `SummonerClient`. Includes cryptographic envelopes, DID support, and access helpers for the Summoner API.


## Concepts in one page

* **Agents** interact over TCP using a decorator‑based SDK. Typical patterns use `@receive` for inbound messages and `@send(multi=True)` to fan out to peers.
* **Servers** are available in Python for iteration and in Rust for performance. The Rust server mirrors Python behavior.
* **Orchestration** can involve local groups or WAN relays. Connector agents bridge external ecosystems.
* **Security** follows a staged design: self‑issued identities, cryptographic envelopes for integrity and confidentiality, and replay protection using nonces and timestamps.


## Troubleshooting

* If an agent fails to import a module, ensure the venv is active and the agent’s `requirements.txt` is installed.
* If a script is not executable, run `chmod +x build_sdk.sh` or `chmod +x install_requirements.sh` as needed.
* On Windows, use WSL2 to avoid socket and path issues.


## Contributing

* Use **starter-template** to bootstrap a module.
* Follow repository‑specific CONTRIBUTING or `docs/doc_development.md` when present.
* Open an issue on one of our public Github repos for design proposals or protocol questions.


## Contact

* Discord: [Join the server](https://discord.gg/kExRQ9S5)
* Twitter: [@SummonerNetwork](https://twitter.com/SummonerNetwork)
* Email: [info@summoner.to](mailto:info@summoner.to)
