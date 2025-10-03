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
  <a href="https://discord.gg/9HMeXnMycE">Discord</a> •
  <a href="https://twitter.com/SummonerNetwork">Twitter</a>
</p>

> **What is Summoner?**
> A modular runtime and SDK for networked AI agents. It lets you compose, run, and coordinate agents across machines. The Python client SDK pairs with a Rust server, and an optional desktop app provides a visual interface. Start with examples, then assemble your own SDK from modules.


## Click your way through Summoner

<p align="center">
  <a href="https://summoner.org">
    <!-- <img src="../img/summoner_intro_rounded.png" alt="Summoner Logo" width="250"/> -->
    <img src="https://github.com/Summoner-Network/.github/blob/main/img/summoner_intro_rounded.png" alt="Summoner Logo" width="250"/>
  </a>
</p>

**Start with Prereqs and follow your branch.** Each path covers platform-specific requirements and installs (click the badges in order).


├── <a href="#install-essential-dependencies" title="Start here - install required tools"><img alt="① Prereqs - install Python, Rust, git, build tools" src="https://img.shields.io/badge/①-Prereqs-6f42c1"></a> <sup><b>&emsp; ☜ &emsp;<em>Start here!</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <a href="#install-your-summoner-sdk" title="Use the SDK: create a venv and fetch core modules"><img alt="② Use the SDK - create venv and fetch core modules" src="https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7"></a> <sup><b>&emsp; ☜ &emsp;<em>If you want to create agents with the SDK</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <a href="#start-a-new-project-fresh" title="Scaffold a new project from the SDK template"><img alt="③ Start New Project - scaffold from SDK template" src="https://img.shields.io/badge/③-Start%20New%20Project-4f9bff"></a> <sup><b>&emsp; ☜ &emsp;<em>Scaffold your own workflow with the SDK</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <a href="#i-want-to-directly-test-the-agent-examples-with-the-sdk" title="Run example agents quickly"><img alt="③ Run Agents - launch example agents quickly" src="https://img.shields.io/badge/③-Run%20Agents-4f9bff"></a> <sup><b>&emsp; ☜ &emsp;<em>Launch example agents in seconds</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <a href="#i-want-to-develop-a-module" title="Author a reusable SDK module"><img alt="② Develop a Module - author a reusable extension" src="https://img.shields.io/badge/②-Develop%20a%20Module-008f99"></a> <sup><b>&emsp;  ☜ &emsp;<em>If you want to author an SDK extension</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <a href="#merge-module-into-sdk" title="Include your module in an SDK recipe"><img alt="③ Merge into SDK - include your module in the SDK build" src="https://img.shields.io/badge/③-Merge%20into%20SDK-00bcd4"></a> <sup><b>&emsp; ☜ &emsp;<em>How to include your module in an SDK</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; └── <a href="#desktop-ui-optional" title="Optional: desktop GUI (requires npm)"><img alt="② Desktop UI - optional GUI (npm required)" src="https://img.shields.io/badge/②-Desktop%20UI-ff69b4"></a> <sup><b>&emsp;  ☜ &emsp;<em>Try the GUI to launch a local server and your agents</em></b></sup>


---

### <img alt="Prereqs" src="https://img.shields.io/badge/Prereqs-6f42c1"> Install Essential Dependencies

Before you build or run anything, make sure these tools are in place.
The commands below are safe to run more than once. If a tool is already installed, the installer will say so and exit.


<details>
<summary><img alt="All platforms icon" width="16" src="https://cdn.simpleicons.org/gnometerminal/6f42c1">
 <b>All platforms: What you need and why</b></summary>
<br>

* **Python 3.9 or newer**. Runs SDK tools and agents.
* **Git**. Clones the repositories.
* **Rust toolchain**. Needed only for the high-performance server on macOS, Linux, or WSL2. Not used on native Windows.
* **Node.js 18+ with npm**. Needed only if you plan to use the Desktop UI.

Use the platform sections below to check versions and install missing items.

</details>


<details>
<summary><img alt="Apple logo" width="16" src="https://cdn.simpleicons.org/apple/6f42c1"> <b>Install on macOS</b></summary>
<br>

**First, check what is already installed.**
Running these checks does not change your system.

```bash
python3 --version || echo "Python not found"
git --version || echo "Git not found"
rustc --version && cargo --version || echo "Rust toolchain not found"
node --version && npm --version || echo "Node not found (Desktop UI only)"
```

**Next, install missing tools.**
These commands install Python, Git, rustup, and Node. The `-y` on rustup accepts defaults.

```bash
brew install python git
brew install rustup
rustup-init -y
brew install node   # only if you want the Desktop UI
```

**Finally, verify the installation.**
If a command prints a version, you are good to go.

```bash
python3 --version
git --version
rustc --version && cargo --version
node --version && npm --version   # only if you installed Node
```

**If you run this again later**
Homebrew is safe to re-run. It will report already installed packages.
Use `rustup update` to upgrade Rust when you need it.
</details>
<a id="ubuntu-debian-prereqs"></a>
<details>
<summary><img alt="Ubuntu" width="16" src="https://cdn.simpleicons.org/ubuntu/6f42c1">
<img alt="Debian" width="16" src="https://cdn.simpleicons.org/debian/6f42c1">
<b>Install on Ubuntu or Debian</b></summary>
<br>

**First, check what is already installed.**
These checks are safe to run any time.

```bash
python3 --version || echo "Python not found"
git --version || echo "Git not found"
rustc --version && cargo --version || echo "Rust toolchain not found"
node --version && npm --version || echo "Node not found (Desktop UI only)"
```

**Next, install missing tools.**
This installs Python, venv, pip, Git, and build tools. It also installs Rust with rustup. Node is optional.

```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip git build-essential pkg-config libssl-dev
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
sudo apt install -y nodejs npm   # only if you want the Desktop UI
```

**Finally, verify the installation.**

```bash
python3 --version
git --version
rustc --version && cargo --version
node --version && npm --version   # only if you installed Node
```

**If you run this again later**
`apt install` is safe to re-run. It will confirm what is already installed.
Use `rustup update` to upgrade Rust when you need it.

</details>


<details>
<summary>
<img alt="Windows logo" width="16" src="https://img.icons8.com/?size=100&id=JSovFPeJN9IG&format=png&color=6f42c1">
 <b>Install on Windows (native)</b></summary>
<br>

On native Windows the stack uses the Python server. The Rust server is not used here.
You can still install Node if you want the Desktop UI.

**First, check what is already installed.**
Run these in PowerShell.

```powershell
python --version   # or: py -3 --version
git --version
node --version; npm --version   # only if you want the Desktop UI
```

**Next, install missing tools.**
Download and install from these pages. During Python setup, select "Add python.exe to PATH."

* Python: [https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/)
* Git for Windows: [https://git-scm.com/download/win](https://git-scm.com/download/win)
* Node.js (optional): [https://nodejs.org/](https://nodejs.org/)

**Finally, verify the installation.**
Run the same checks again in PowerShell. If a command prints a version, you are done.

**If you run this again later**
Installers usually detect existing versions and do not replace them without asking.

</details>


<details><summary>
<img alt="Windows logo" width="16" src="https://img.icons8.com/?size=100&id=JSovFPeJN9IG&format=png&color=6f42c1">
<img alt="Ubuntu logo" width="16" src="https://cdn.simpleicons.org/ubuntu/6f42c1">
 <b>Install on Windows with WSL2 (Rust server support)</b></summary>
<br>

If you want the Rust server on Windows, use WSL2 with Ubuntu.

**First, enable WSL2 and install Ubuntu.**
Run this in PowerShell.

```powershell
wsl --install -d Ubuntu
```

**Next, open the Ubuntu terminal.**
Follow the [**Ubuntu or Debian**](#ubuntu-debian-prereqs) section above inside WSL. Install Python, Git, Rust, and Node if you want the Desktop UI.

**Finally, verify the installation.**
Use the version checks from the Ubuntu section.
Localhost usually works across Windows and WSL. If needed, run `hostname -I` in Ubuntu and bind to that address.

**If you run this again later**
Use the same checks and installers inside WSL.
Use `rustup update` in WSL when you want to upgrade Rust.

</details>








---







### <img alt="Use the SDK" src="https://img.shields.io/badge/Use%20the%20SDK-0b5ed7"> Install your Summoner SDK

You can start from the **SDK template** (clean SDK) or from **summoner-agents** (SDK + examples). Both come from the same template. The installer creates a virtual environment and composes the SDK. You can re-run it safely.

> [!NOTE]
> **About the server.** On native Windows you use the **Python server**. The Rust server is not available on Windows. To try Rust on Windows, use **WSL2**.


<details>
<summary><img alt="Template icon" width="16" src="https://cdn.simpleicons.org/github/0b5ed7"> <b>Option A - Use the SDK template</b></summary>
<br>

**Create your own SDK repo from the template.** Click **Use this template → Create a new repository** on the [**SDK template**](https://github.com/Summoner-Network/summoner-sdk#getting-started), then clone it and enter the folder.

```bash
git clone https://github.com/<your-account>/<your-sdk-repo>.git
cd <your-sdk-repo>
```

**Choose features in `build.txt`.** List the modules you want your SDK to include. This step is optional and you can keep the default `build.txt` as-is. For custom builds, see the [**`build.txt` format**](https://github.com/Summoner-Network/summoner-sdk#buildtxt--test_buildtxt-format) in the template README.

**Use the installation procedure for your platform.** See the sections below for platform-specific commands.

</details>
<a id="use-an-sdk-with-agent-examples"></a>
<details>
<summary><img alt="Agents repo icon" width="16" src="https://cdn.simpleicons.org/github/0b5ed7"> <b>Option B - Use an SDK with agent examples</b></summary>
<br>

**Download the SDK with agent examples.** Clone the [`summoner-agents`](https://github.com/Summoner-Network/summoner-agents) repository and enter the folder.

```bash
git clone https://github.com/Summoner-Network/summoner-agents.git
cd summoner-agents
```

**Use the installation procedure for your platform.** See the sections below for platform-specific commands.

</details>


<details>
<summary>
<img alt="Apple logo" width="16" src="https://cdn.simpleicons.org/apple/0b5ed7">
<img alt="Ubuntu" width="16" src="https://cdn.simpleicons.org/ubuntu/0b5ed7"> 
<img alt="Debian" width="16" src="https://cdn.simpleicons.org/debian/0b5ed7"> 
<b>Install on macOS, Ubuntu or Debian</b></summary>
<br>

**Run the installer.** Choose **either** approach, both will perform the same setup.

* **Either** run in the current shell so `venv/` auto-activates:

  ```bash
  # From your project root (template or summoner-agents)
  source build_sdk.sh setup
  ```

* **Or** run as a separate process, then activate manually:

  ```bash
  bash build_sdk.sh setup
  source venv/bin/activate
  ```

**Verify the installation.** Confirm that Python sees the SDK and view the interpreter path.

```bash
python3 -c "import summoner, sys; print('summoner OK', sys.executable)"
```

**Reset when needed.** Return to a clean state, then re-run setup.

```bash
bash build_sdk.sh reset
```

Read more: [POSIX install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/installation.md)

</details>


<details>
<summary>
<img alt="Windows logo" width="16" src="https://img.icons8.com/?size=100&id=JSovFPeJN9IG&format=png&color=0b5ed7">
 <b>Install on Windows (native)</b></summary>
<br>

**Open a PowerShell terminal.** You can use Windows Terminal, PowerShell 7+, or VS Code's integrated terminal (PowerShell profile).

**Allow scripts for this session only.** This temporarily lets you run the installer. Close the terminal after use to revert.

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

**Run the installer.** This composes your SDK, creates `venv\`, and installs dependencies from `build.txt`.

```powershell
.\build_sdk_on_windows.ps1 setup
```

**Activate the environment.** Your prompt should show `(venv)`.

```powershell
.\venv\Scripts\Activate.ps1
```

**Verify the installation.** Confirm that Python sees the SDK and view the interpreter path.

```powershell
python -c "import summoner, sys; print('summoner OK', sys.executable)"
```

**Reset when needed.** Return to a clean state, then re-run setup.

```powershell
.\build_sdk_on_windows.ps1 reset
```

Read more: [Windows install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/windows_install.md) • [SDK template](https://github.com/Summoner-Network/summoner-sdk) • [`build.txt` format](https://github.com/Summoner-Network/summoner-sdk#buildtxt--test_buildtxt-format)

</details>


<details>
<summary>
<img alt="Windows logo" width="16" src="https://img.icons8.com/?size=100&id=JSovFPeJN9IG&format=png&color=0b5ed7">
<img alt="Ubuntu logo" width="16" src="https://cdn.simpleicons.org/ubuntu/0b5ed7">
 <b>Install on Windows with WSL2 (Rust server support)</b></summary>
<br>

**Enable WSL2 and install Ubuntu.**

```powershell
wsl --install -d Ubuntu
```

**Open the Ubuntu terminal.** Go to your SDK project folder.

**Run the installer.** Choose **either** approach, both will complete the same setup.

* **Either** run in the current shell so `venv/` auto-activates:

  ```bash
  source build_sdk.sh setup
  ```

* **Or** run as a separate process, then activate manually:

  ```bash
  bash build_sdk.sh setup
  source venv/bin/activate
  ```

**Verify the installation.** Confirm that Python sees the SDK and view the interpreter path.

```bash
python3 -c "import summoner, sys; print('summoner OK', sys.executable)"
```

**Networking tip.** `localhost` usually works across Windows and WSL2. If it does not, you can use the WSL IP:

```bash
hostname -I
```

Read more: [POSIX install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/installation.md)

</details>








---








### <img alt="Start New Project" src="https://img.shields.io/badge/Start%20New%20Project-4f9bff"> Start a new project (fresh)

<a id="start-a-new-project-fresh"></a>

Create a clean SDK you own and extend. First define a **composition recipe** in `build.txt`, then install for your platform, and set up self-contained agent folders so they stay compatible with the Desktop app.


<details>
<summary><img alt="List icon" width="16" src="https://cdn.simpleicons.org/textpattern/4f9bff"> <b>Define your SDK recipe</b> <code>build.txt</code> (and optional <code>test_build.txt</code>)</summary>
<br>

**To build your Summoner SDK**, you need to tell the installer which packages to include from each Summoner module. Modules are GitHub repositories created from the template repository [starter-template](https://github.com/Summoner-Network/starter-template). Each module provides one or more packages under its `tooling/` directory.

<!-- **Tell the installer what to include.** You list which packages to pull from Summoner modules (repos built from the template). Each module contributes one or more packages under its `tooling/` directory. During install, those packages are merged under `summoner/…` so you import them uniformly. -->

**Include an entire repository (all packages).** If you want to include every package under that repository’s `tooling/` directory, put the repository URL on its own line in `build.txt`.

<!-- **Include an entire module (all packages).** Put the repo URL on its own line. The installer will copy every package under that repo's `tooling/`. -->

```txt
https://github.com/Summoner-Network/summoner-agentclass.git
```

**Include only specific packages.** If you want to include a subset of packages from a repository, add a colon after the repository URL, then list the package folder names from `tooling/` on the following lines.

<!-- **Include specific packages only.** Add a colon after the repo URL, then list the `tooling/` subfolders you want. This keeps your SDK small and intentional. -->

```txt
https://github.com/Summoner-Network/summoner-agentclass.git:
aurora
```

**Optional quick tests.** Use `test_build.txt` for a minimal smoke test (often the starter template). You can switch between `build.txt` and `test_build.txt` by running `setup build` or `setup test_build`.

```txt
https://github.com/Summoner-Network/starter-template.git
```

**You can change the recipe any time.** Edit `build.txt` or `test_build.txt` and re-run `setup` to rebuild your SDK. Nothing breaks if you re-run; the script is idempotent.

**Imports after install.** You can import the core and any included packages in the same way:

```python
from summoner.server import SummonerServer
from summoner.client import SummonerClient
from summoner.your_package import hello_summoner
from summoner.aurora import SummonerAgent
```

Read more: **[`build.txt` format](https://github.com/Summoner-Network/summoner-sdk#buildtxt--test_buildtxt-format)** • **[SDK template](https://github.com/Summoner-Network/summoner-sdk)**

</details>


<details>
<summary>
<img alt="Apple" width="16" src="https://cdn.simpleicons.org/apple/4f9bff">
<img alt="Ubuntu" width="16" src="https://cdn.simpleicons.org/ubuntu/4f9bff">
<img alt="Debian" width="16" src="https://cdn.simpleicons.org/debian/4f9bff">
<b>Install on POSIX platforms (macOS, Ubuntu, Debian)</b>
</summary>
<br>

**Run the installer.** Choose **either** approach, both will complete the same setup.

* **Either** run in the current shell so `venv/` auto-activates:

  ```bash
  source build_sdk.sh setup
  ```

* **Or** run as a separate process, then activate manually (two steps but equivalent result):

  ```bash
  bash build_sdk.sh setup
  source venv/bin/activate
  ```

**Check that Python sees the SDK.** This prints a confirmation and the exact Python path in use.

```bash
python3 -c "import summoner, sys; print('summoner OK', sys.executable)"
```

**Reset later if needed.** This clears generated artifacts and reinstalls from your recipe.

```bash
bash build_sdk.sh reset
```

Read more: **[POSIX install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/installation.md)**

</details>


<details>
<summary>
<img alt="Windows" width="16" src="https://img.icons8.com/?size=100&id=JSovFPeJN9IG&format=png&color=4f9bff">
<b>Install on Windows (native)</b>
</summary>
<br>

On native Windows the **Python server** is used. The Rust server is not used here.

**Open a PowerShell terminal.** You can use Windows Terminal, PowerShell 7+, or VS Code's integrated terminal (PowerShell profile).

**Run the installer.** First allow scripts **just for this session** (reverts when you close the window), then build and activate:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\build_sdk_on_windows.ps1 setup
.\venv\Scripts\Activate.ps1
```

**Check that Python sees the SDK.** This prints a confirmation and the `venv` path.

```powershell
python -c "import summoner, sys; print('summoner OK', sys.executable)"
```

**Reset later if needed.** This does a clean rebuild using your current `build.txt`.

```powershell
.\build_sdk_on_windows.ps1 reset
```

Read more: **[Windows install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/windows_install.md)** • **[SDK template](https://github.com/Summoner-Network/summoner-sdk)** • **[`build.txt` format](https://github.com/Summoner-Network/summoner-sdk#buildtxt--test_buildtxt-format)**

</details>


<details>
<summary>
<img alt="Windows" width="16" src="https://img.icons8.com/?size=100&id=JSovFPeJN9IG&format=png&color=4f9bff">
<img alt="Ubuntu" width="16" src="https://cdn.simpleicons.org/ubuntu/4f9bff">
<b>Install on Windows with WSL2 (Rust server support)</b>
</summary>
<br>

WSL2 with Ubuntu gives you parity with Linux/macOS, including the Rust server.

**Enable WSL2 (PowerShell).**

```powershell
wsl --install -d Ubuntu
```

**Run the installer inside Ubuntu.** Choose **either** approach, both will complete the same setup.

```bash
# Either:
source build_sdk.sh setup
# Or:
bash build_sdk.sh setup && source venv/bin/activate
```

**Check that Python sees the SDK.**

```bash
python3 -c "import summoner, sys; print('summoner OK', sys.executable)"
```

**Networking tip.** `localhost` usually works across Windows and WSL2. If it does not, use the WSL IP:

```bash
hostname -I
```

Read more: **[POSIX install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/installation.md)**

</details>


<details>
<summary><img alt="List icon" width="16" src="https://cdn.simpleicons.org/textpattern/4f9bff"> <b>Keep your project Desktop-compatible</b></summary>
<br>

**Where your code lives.** You can place your code wherever it makes sense for your project. If you plan to use the Desktop app, keep each launchable agent and its dependencies inside a single, **self-contained agent folder**.

**Agent folder shape the Desktop can import.** The Desktop's import feature works with **any self-contained agent folder** laid out like this:

```txt
folder/
  agent.py           # entry point (calls your agent's .run() in an asyncio context)
  requirements.txt   # dependencies for this agent only
  README.md          # what it does, how to run, scenarios (recommended)
  configs/           # optional: per-environment settings
    client_config.json
  state/             # optional: local files the agent uses
  utils.py           # optional: helpers for this agent
```

**Entry point expectations.** In `agent.py`, expose a `main()` that can accept an optional `--config`, build a `SummonerClient`, wire handlers/hooks, and call `client.run(...)`. Prefer config files over many CLI flags so environments can change without code edits.

**Stable imports.** Use the `summoner` namespace so your imports remain consistent as your SDK evolves:

```python
from summoner.client import SummonerClient
from summoner.server import SummonerServer
# plus any composed packages you included via build.txt
```


**Entry point expectations.** In `agent.py`, expose a `main()` that can take an optional `--config`, build a `SummonerClient`, wire handlers/hooks, and call `client.run(...)`. Favor config files over many CLI flags so environments can change without code edits.

**Imports that stay stable.** Keep imports under the `summoner` namespace so they remain consistent as you evolve your SDK:

```python
from summoner.client import SummonerClient
from summoner.server import SummonerServer
# plus any composed packages you included via build.txt
```

**Pull a ready-made example agent (optional).** You can copy a single agent from [`summoner-agents`](https://github.com/Summoner-Network/summoner-agents) into your project with the helper script `get_agent` (Bash):

```bash
# list available agents from the repo (default branch: main)
bash get_agent --list

# fetch one agent into agents/ (creates agents/agent_<Name>)
bash get_agent SendAgent_0

# overwrite if it already exists
bash get_agent SendAgent_0 --force
```

* The script downloads from [`summoner-agents`](https://github.com/Summoner-Network/summoner-agents) and supports `--branch` and `--repo` if you need a different ref or fork.
* It requires Bash and standard tools (`tar` plus `curl` or `wget`).
* On Windows, you can run it from VS Code's integrated **Bash** (or Git Bash).

Read more: **[Design fundamentals](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/fundamentals/design.md)**

</details>






---






### <img alt="Run Agents" src="https://img.shields.io/badge/Run%20Agents-4f9bff"> Start with runnable agent examples

You can use the [`summoner-agents`](https://github.com/Summoner-Network/summoner-agents) repo when you want ready-made agents you can run immediately. The SDK recipe for this repo is already set, so your focus is simple: 
- [✓] **install the agent's requirements**, 
- [✓] **start the server**, 
- [✓] **then run the agent**.

Think of it as three small switches you flip on, in order.



<details>
<summary><img alt="Package" width="16" src="https://cdn.simpleicons.org/pypi/4f9bff"> <b>Install agent dependencies</b></summary>
<br>

This section assumes you already installed the SDK for this repo (see **Install your Summoner SDK** above).

**Activate the virtual environment.** This ensures Python installs into the right place. Run this **whenever you open a new terminal**:

```bash
# POSIX (macOS/Linux/WSL2)
source venv/bin/activate
```

```powershell
# Windows (PowerShell)
.\venv\Scripts\Activate.ps1
```

**Install requirements for one agent.** This is the quickest way to try a single agent. Point to that agent's **self-contained folder**:

```bash
pip install -r path/to/your/agent/folder/requirements.txt
```

**Install requirements for all agents (bulk).** From the repo root (Bash):

```bash
bash install_requirements.sh
```

* The script scans for agent folders and installs each `requirements.txt`.
* On Windows, use **Git Bash** or **VS Code** with a **Bash** terminal.
* If you later see `ModuleNotFoundError`, install that agent's requirements and try again.

</details>


<details>
<summary><img alt="Server" width="16" src="https://cdn.simpleicons.org/gnometerminal/4f9bff"> <b>Launch the Summoner server</b></summary>
<br>

Most agents rely on the server as their messaging backbone. **Start the server first**, then launch agents in a second terminal.

**Activate the virtual environment.** This guarantees the server uses the SDK you installed:

```bash
# POSIX (macOS/Linux/WSL2)
source venv/bin/activate
```

```powershell
# Windows (PowerShell)
.\venv\Scripts\Activate.ps1
```

**Run with the default config.**

```bash
python server.py
```

**Use a custom server config** (only if an agent's README asks for it):

```bash
python server.py --config configs/<server_config>.json
```

Leave the server running in this terminal. Open another terminal (and activate the venv there too) to run agents.

</details>


<details>
<summary><img alt="Robot" width="16" src="https://cdn.simpleicons.org/robotframework/4f9bff"> <b>Run an agent</b></summary>
<br>

**Activate the virtual environment.** This makes sure the agent imports the SDK and its own dependencies:

```bash
# POSIX (macOS/Linux/WSL2)
source venv/bin/activate
```

```powershell
# Windows (PowerShell)
.\venv\Scripts\Activate.ps1
```

**Run with defaults.** Execute the entry point in the **self-contained agent folder**:

```bash
python path/to/your/agent/folder/agent.py
```

**Run with a custom agent config** (when provided by that agent):

```bash
python path/to/your/agent/folder/agent.py --config configs/<agent_config>.json
```

**Find the right config.** Look in the agent folder's README for flags, environment variables, or a recommended config file.

**Typical workflow (two terminals).**

* **Terminal A — server**

  ```bash
  source venv/bin/activate          # POSIX
  # .\venv\Scripts\Activate.ps1     # Windows
  python server.py
  ```
* **Terminal B — agent**

  ```bash
  source venv/bin/activate          # POSIX
  # .\venv\Scripts\Activate.ps1     # Windows
  pip install -r path/to/your/agent/folder/requirements.txt
  python path/to/your/agent/folder/agent.py
  ```


**Common errors**

* If you see "cannot import summoner…", make sure the virtual environment is active in this terminal. If it is not active, activate it and run the command again.
* If you see "address already in use", stop any other server processes that may be running, or change the server port in the configuration file and try again.
* If an agent cannot connect, make sure the server terminal is still running and that your local firewall is not blocking the connection.


</details>


<details>
<summary><img alt="Folder" width="16" src="https://cdn.simpleicons.org/textpattern/4f9bff"> <b>How agent folders are discovered (Desktop app)</b></summary>
<br>

The Desktop app can import and run **any self-contained agent folder** with this minimal shape:

```txt
folder/
  agent.py
  requirements.txt
  (optional) README.md, configs/, state/, utils.py
```

Keeping this structure makes your agent easy to import, run locally, and share with teammates.

</details>



---










<br>
<br>
<br>









## Start here



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


## Prerequisites

<details>
<summary>
<b>(Click to expand)</b> Pre-requisities and installation steps:
</summary>
<br>

**Prereqs**

* Python 3.9 or newer
* `git`
* macOS or Linux. Windows users can use WSL2 or git bash via VS code.

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

* If an agent fails to import a module, ensure the venv is active and the agent's `requirements.txt` is installed.
* If a script is not executable, run `chmod +x build_sdk.sh` or `chmod +x install_requirements.sh` as needed.
* On Windows, use WSL2 to avoid socket and path issues.


## Contributing

* Use **starter-template** to bootstrap a module.
* Follow the repository-specific **CONTRIBUTING.md** or **Contributions** section if available, or see our [How to contribute](https://github.com/Summoner-Network/summoner-docs/blob/main/development/contribution/index.md) guidelines in `summoner-docs`.
* Open an issue on one of our public Github repos for design proposals or protocol questions.


## Contact

* Discord: [Join the server](https://discord.gg/9HMeXnMycE)
* Twitter: [@SummonerNetwork](https://twitter.com/SummonerNetwork)
* Email: [info@summoner.org](mailto:info@summoner.org)

