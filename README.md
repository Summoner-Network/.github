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

**Begin with Prereqs, then follow your branch step by step.** Click the badges in order to reach your goal.

<div>
├── <a href="#install-essential-dependencies" title="Start here - install required tools"><img alt="① Prereqs - install Python, Rust, git, build tools" src="https://img.shields.io/badge/①-Prereqs-6f42c1"></a> <sup><b>&emsp; ☜ &emsp;<em>Start here!</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <a href="#i-want-to-start-my-own-project-with-the-sdk" title="Use the SDK: create a venv and fetch core modules"><img alt="② Use the SDK - create venv and fetch core modules" src="https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7"></a> <sup><b>&emsp; ☜ &emsp;<em>If you want to test the SDK</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ├── <a href="#i-want-to-directly-test-the-agent-examples-with-the-sdk" title="Run example agents quickly"><img alt="③ Run Agents - launch example agents quickly" src="https://img.shields.io/badge/③-Run%20Agents-4f9bff"></a> <sup><b>&emsp; ☜ &emsp;<em>Launch example agents in seconds</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <a href="#start-a-new-project-fresh" title="Scaffold a new project from the SDK template"><img alt="③ Start New Project - scaffold from SDK template" src="https://img.shields.io/badge/③-Start%20New%20Project-4f9bff"></a> <sup><b>&emsp; ☜ &emsp;<em>Scaffold your own app with the SDK</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <a href="#i-want-to-develop-a-module" title="Author a reusable SDK module"><img alt="② Develop a Module - author a reusable extension" src="https://img.shields.io/badge/②-Develop%20a%20Module-008f99"></a> <sup><b>&emsp;  ☜ &emsp;<em>If you want to author an SDK extension</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <a href="#merge-module-into-sdk" title="Include your module in an SDK recipe"><img alt="③ Merge into SDK - include your module in the SDK build" src="https://img.shields.io/badge/③-Merge%20into%20SDK-00bcd4"></a> <sup><b>&emsp; ☜ &emsp;<em>How to include your module in an SDK</em></b></sup><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <a href="#desktop-ui-optional" title="Optional: desktop GUI (requires npm)"><img alt="② Desktop UI - optional GUI (npm required)" src="https://img.shields.io/badge/②-Desktop%20UI-ff69b4"></a> <sup><b>&emsp;  ☜ &emsp;<em>Try the GUI to launch a local server and your agents</em></b></sup>
</div>

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
<summary><img alt="Ubuntu logo" width="16" src="https://cdn.simpleicons.org/ubuntu/6f42c1">
<img alt="Debian logo" width="16" src="https://cdn.simpleicons.org/debian/6f42c1">
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
Download and install from these pages. During Python setup, select “Add python.exe to PATH.”

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




### <img alt="Use the SDK" src="https://img.shields.io/badge/Use%20the%20SDK-0b5ed7"> Create your SDK and install it

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
<summary><img alt="Apple logo" width="16" src="https://cdn.simpleicons.org/apple/0b5ed7"> <b>Install on macOS</b></summary>
<br>

**Run the installer.** Choose **either** approach, both perform the same setup.

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
<summary><img alt="Ubuntu logo" width="16" src="https://cdn.simpleicons.org/ubuntu/0b5ed7"> <img alt="Debian logo" width="16" src="https://cdn.simpleicons.org/debian/0b5ed7"> <b>Install on Ubuntu or Debian</b></summary>
<br>

**Run the installer.** Choose **either** approach, both perform the same setup.

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

**Open a PowerShell terminal.** You can use Windows Terminal, PowerShell 7+, or VS Code’s integrated terminal (PowerShell profile).

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

**Run the installer.** Choose **either** approach.

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

