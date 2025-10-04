# Summoner Platform

<!-- <p align="center">
  <a href="https://summoner.org">
    <img src="https://summoner.org/static/images/summoner-logo.png" alt="Summoner Logo" width="160"/>
  </a>
</p> -->

<p align="center">
  <a href="https://summoner.org">
    <!-- <img src="../img/summoner_intro_rounded.png" alt="Summoner Logo" width="250"/> -->
    <img src="https://github.com/Summoner-Network/.github/blob/main/img/summoner_intro_rounded.png" alt="Summoner Logo" width="250"/>
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


## Pick your route: run now or learn first

Whether you want a quick demo or a production-ready setup, start where it fits.  
Each row is a complete route; follow the badges in order. Docs are one click away if you want background first.



| Path | What you’ll do |
|---|---|
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#-install-essential-dependencies) | Install Python, Rust, git, and build tools. |
| [![① Prereqs](https://img.shields.io/badge/①-%20-6f42c1)](#-install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Use the SDK](https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7)](#-install-your-summoner-sdk) | Set up a venv and fetch core modules for the SDK. |
| [![① Prereqs](https://img.shields.io/badge/①-%20-6f42c1)](#-install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Use the SDK](https://img.shields.io/badge/②-%20-0b5ed7)](#-install-your-summoner-sdk) <sup>&nbsp;➜&nbsp;</sup> [![③ Start New Project](https://img.shields.io/badge/③-Start%20New%20Project-4f9bff)](#start-a-new-project-fresh) | Scaffold a fresh project from the SDK template. |
| [![① Prereqs](https://img.shields.io/badge/①-%20-6f42c1)](#-install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Use the SDK](https://img.shields.io/badge/②-%20-0b5ed7)](#install-your-summoner-sdk) <sup>&nbsp;➜&nbsp;</sup> [![③ Run Agents](https://img.shields.io/badge/③-Run%20Agents-4f9bff)](#start-with-runnable-agent-examples) | Run example agents immediately. |
| [![① Prereqs](https://img.shields.io/badge/①-%20-6f42c1)](#-install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Develop a Module](https://img.shields.io/badge/②-Develop%20a%20Module-008f99)](#i-want-to-develop-a-module) | Author a reusable SDK module. |
| [![① Prereqs](https://img.shields.io/badge/①-%20-6f42c1)](#-install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Develop a Module](https://img.shields.io/badge/②-%20-008f99)](#i-want-to-develop-a-module) <sup>&nbsp;➜&nbsp;</sup> [![③ Merge into SDK](https://img.shields.io/badge/③-Merge%20into%20SDK-00bcd4)](#merge-module-into-sdk) | Merge your module into an SDK build/recipe. |
| [![① Prereqs](https://img.shields.io/badge/①-%20-6f42c1)](#-install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Desktop UI](https://img.shields.io/badge/②-Desktop%20UI-ff69b4)](#desktop-ui-optional) | Optional desktop GUI to launch a local server and agents. |
| [![① Read SDK Docs](https://img.shields.io/badge/②-Read%20SDK%20Docs-d6720f)](#summoner-docs) | Read the docs and learn about Summoner. |


<!-- Horizontally scrollable, first column never wraps -->
<div style="max-width:100%; overflow-x:auto;">
  <table style="border-collapse:collapse; width:auto; min-width:720px;">
    <thead>
      <tr>
        <th style="text-align:left; white-space:nowrap;">Path</th>
        <th style="text-align:left;">What you’ll do</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href=#-install-essential-dependencies title="Start here — install required tools"><img alt="① Prereqs" src="https://img.shields.io/badge/①-Prereqs-6f42c1"></a>
        </td>
        <td>Install Python, Rust, git, and build tools.</td>
      </tr>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href=#-install-essential-dependencies>
            <img alt="① Prereqs" src="https://img.shields.io/badge/①-Prereqs-6f42c1">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-install-your-summoner-sdk" title="Create a venv and fetch core modules">
            <img alt="② Use the SDK" src="https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7">
          </a>
        </td>
        <td>Set up a venv and fetch core modules for the SDK.</td>
      </tr>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href=#-install-essential-dependencies>
            <img alt="① Prereqs" src="https://img.shields.io/badge/①-Prereqs-6f42c1">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-install-your-summoner-sdk" title="Scaffold from SDK template">
            <img alt="② Use the SDK" src="https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-start-a-new-project-fresh" title="Scaffold from SDK template">
            <img alt="③ Start New Project" src="https://img.shields.io/badge/③-Start%20New%20Project-4f9bff">
          </a>
        </td>
        <td>Scaffold a fresh project from the SDK template.</td>
      </tr>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href=#-install-essential-dependencies>
            <img alt="① Prereqs" src="https://img.shields.io/badge/①-Prereqs-6f42c1">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-install-your-summoner-sdk" title="Launch example agents">
            <img alt="② Use the SDK" src="https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-start-with-runnable-agent-examples" title="Launch example agents">
            <img alt="③ Run Agents" src="https://img.shields.io/badge/③-Run%20Agents-4f9bff">
          </a>
        </td>
        <td>Run example agents immediately.</td>
      </tr>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href=#-install-essential-dependencies>
            <img alt="① Prereqs" src="https://img.shields.io/badge/①-Prereqs-6f42c1">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-i-want-to-develop-a-module" title="Author an SDK extension">
            <img alt="② Develop a Module" src="https://img.shields.io/badge/②-Develop%20a%20Module-008f99">
          </a>
        </td>
        <td>Author a reusable SDK module.</td>
      </tr>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href=#-install-essential-dependencies>
            <img alt="① Prereqs" src="https://img.shields.io/badge/①-Prereqs-6f42c1">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-i-want-to-develop-a-module">
            <img alt="② Develop a Module" src="https://img.shields.io/badge/②-Develop%20a%20Module-008f99">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-merge-module-into-sdk" title="Include your module in an SDK recipe">
            <img alt="③ Merge into SDK" src="https://img.shields.io/badge/③-Merge%20into%20SDK-00bcd4">
          </a>
        </td>
        <td>Merge your module into an SDK build/recipe.</td>
      </tr>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href=#-install-essential-dependencies>
            <img alt="① Prereqs" src="https://img.shields.io/badge/①-Prereqs-6f42c1">
          </a>
          <sup>&nbsp;➜&nbsp;</sup>
          <a href="#-desktop-ui-optional" title="Optional GUI">
            <img alt="② Desktop UI" src="https://img.shields.io/badge/②-Desktop%20UI-ff69b4">
          </a>
        </td>
        <td>Optional desktop GUI to launch a local server and agents.</td>
      </tr>
      <tr>
        <td style="white-space:nowrap; vertical-align:middle;">
          <a href="#-summoner-docs" title="Documentation">
            <img alt="① Read SDK Docs" src="https://img.shields.io/badge/②-Read%20SDK%20Docs-d6720f">
          </a>
        </td>
        <td>Read the docs and learn about Summoner.</td>
      </tr>
    </tbody>
  </table>
</div>


<!-- 
| Path | What you’ll do |
|---|---|
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#install-essential-dependencies "Start here — install required tools") | Install Python, Rust, git, and build tools. |
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Use the SDK](https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7)](#install-your-summoner-sdk "Create a venv and fetch core modules") | Set up a venv and fetch core modules for the SDK. |
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Use the SDK](https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7)](#install-your-summoner-sdk) <sup>&nbsp;➜&nbsp;</sup> [![③ Start New Project](https://img.shields.io/badge/③-Start%20New%20Project-4f9bff)](#start-a-new-project-fresh "Scaffold from SDK template") | Scaffold a fresh project from the SDK template. |
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Use the SDK](https://img.shields.io/badge/②-Use%20the%20SDK-0b5ed7)](#install-your-summoner-sdk) <sup>&nbsp;➜&nbsp;</sup> [![③ Run Agents](https://img.shields.io/badge/③-Run%20Agents-4f9bff)](#start-with-runnable-agent-examples "Launch example agents") | Run example agents immediately. |
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Develop a Module](https://img.shields.io/badge/②-Develop%20a%20Module-008f99)](#i-want-to-develop-a-module "Author an SDK extension") | Author a reusable SDK module. |
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Develop a Module](https://img.shields.io/badge/②-Develop%20a%20Module-008f99)](#i-want-to-develop-a-module) <sup>&nbsp;➜&nbsp;</sup> [![③ Merge into SDK](https://img.shields.io/badge/③-Merge%20into%20SDK-00bcd4)](#merge-module-into-sdk "Include your module in an SDK recipe") | Merge your module into an SDK build/recipe. |
| [![① Prereqs](https://img.shields.io/badge/①-Prereqs-6f42c1)](#install-essential-dependencies) <sup>&nbsp;➜&nbsp;</sup> [![② Desktop UI](https://img.shields.io/badge/②-Desktop%20UI-ff69b4)](#desktop-ui-optional "Optional GUI") | Optional desktop GUI to launch a local server and agents. |
| [![① Read SDK Docs](https://img.shields.io/badge/②-Read%20SDK%20Docs-d6720f)](#summoner-docs "Documentation") | Read the docs and learn about Summoner. | -->




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
<summary><img alt="Template icon" width="16" src="https://cdn.simpleicons.org/github/0b5ed7"> <b>Option A - Start from scratch with an SDK template</b></summary>
<br>

**Create your own SDK repo from the template.** Click **Use this template → Create a new repository** on the [**SDK template**](https://github.com/Summoner-Network/summoner-sdk#getting-started), then clone it and enter the folder.

```bash
git clone https://github.com/<your-account>/<your-sdk-repo>.git
cd <your-sdk-repo>
```

**Choose modules and packages in `build.txt`.** List the modules you want your SDK to include. This step is optional and you can keep the default `build.txt` as-is. For custom builds, see the [**`build.txt` format**](#start-a-new-project-built-text) instructions in **Create a clean SDK (no ready-made agents)** below.

**Use the installation procedure for your platform.** See the sections below for platform-specific commands.

</details>
<a id="use-an-sdk-with-agent-examples"></a>
<details>
<summary><img alt="Agents repo icon" width="16" src="https://cdn.simpleicons.org/github/0b5ed7"> <b>Option B - Run agent examples with a ready-made SDK</b></summary>
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

Read more: **[POSIX install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/installation.md)**

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

Read more: **[Windows install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/windows_install.md)** • **[SDK template](https://github.com/Summoner-Network/summoner-sdk)**

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

Read more: **[POSIX install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/installation.md)**

</details>








---








### <img alt="Start New Project" src="https://img.shields.io/badge/Start%20New%20Project-4f9bff"> Create a clean SDK (no ready-made agents)


You can create a clean SDK that you extend as you explore. First define a **composition recipe** in `build.txt`, then install for your platform, and set up self-contained agent folders so they stay compatible with the Desktop app.
<a id="start-a-new-project-built-text"></a>
<details>
<summary><img alt="List icon" width="16" src="https://cdn.simpleicons.org/textpattern/4f9bff"> <b>Define your SDK recipe</b> <code>build.txt</code> (and optional <code>test_build.txt</code>)</summary>
<br>

**To build your Summoner SDK**, you need to tell the installer which packages to include from each Summoner module. Modules are GitHub repositories created from the template repository [`starter-template`](https://github.com/Summoner-Network/starter-template). Each module provides one or more packages under its `tooling/` directory.

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

Read more: **[SDK template (`build.txt` format)](https://github.com/Summoner-Network/summoner-sdk#buildtxt--test_buildtxt-format)**
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

Read more: **[Windows install notes](https://github.com/Summoner-Network/summoner-docs/blob/main/guide_sdk/getting_started/windows_install.md)** • **[SDK template](https://github.com/Summoner-Network/summoner-sdk)**

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
- [ ] install the agent's requirements
- [ ] start the server
- [ ] then run the agent.

Think of it as three small switches you flip on, in order.



<details>
<summary><img alt="Package" width="16" src="https://cdn.simpleicons.org/pypi/4f9bff"> <b>Install agent dependencies</b></summary>
<br>

This section assumes you already installed the SDK for the [`summoner-agents`](https://github.com/Summoner-Network/summoner-agents) repo (see [**Run agent examples with a ready-made SDK**](#use-an-sdk-with-agent-examples) above).

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










### <img alt="Develop a Module" src="https://img.shields.io/badge/Develop%20a%20Module-008f99"> Contribute your own SDK module

A **module** is a repository created from the [`starter-template`](https://github.com/Summoner-Network/starter-template). Your code lives under [`tooling/`](https://github.com/Summoner-Network/starter-template/tree/main/tooling) as one or more Python packages. You develop against the core SDK, then merge your package(s) into an SDK build later.

<details>
<summary><img alt="GitHub" width="16" src="https://cdn.simpleicons.org/github/008f99"> <b>Create your module repo from the template</b></summary>
<br>

**Make your own repo.** Click **Use this template → Create a new repository** on the [`starter-template`](https://github.com/Summoner-Network/starter-template), then clone it and enter the folder.

```bash
git clone https://github.com/<your-account>/<your-module-repo>.git
cd <your-module-repo>
```

**What the template gives you.** A bootstrap script, a virtual environment, and a smoke test that launches a small server.

</details>

<details>
<summary>
<img alt="Apple" width="16" src="https://cdn.simpleicons.org/apple/008f99">
<img alt="Ubuntu" width="16" src="https://cdn.simpleicons.org/ubuntu/008f99">
<img alt="Debian" width="16" src="https://cdn.simpleicons.org/debian/008f99">
<b>Set up on macOS / Ubuntu / Debian</b></summary>
<br>

Once you have cloned your module repo, proceed as follows.

**Run the installer.** Choose **either** approach. Both complete the same setup.

* **Either** run in the current shell so `venv/` auto-activates:

  ```bash
  source install.sh setup
  ```

* **Or** run as a separate process, then activate manually:

  ```bash
  bash install.sh setup
  source venv/bin/activate
  ```

**Smoke test.** Verify the installation by launching the test server. The script generates `test_server.py` you can run on localhost.

```bash
bash install.sh test_server
```

This creates `test_server.py`, `test_server_config.json`, and starts a basic server using the installed `summoner` package.

**If VS Code does not resolve imports.** Select the `venv` interpreter once and reopen your files so `from summoner.server import SummonerServer` resolves.

</details>

<details>
<summary>
<img alt="Windows" width="16" src="https://img.icons8.com/?size=100&id=JSovFPeJN9IG&format=png&color=008f99">
<b>Set up on Windows (native)</b></summary>
<br>

Once you have cloned your module repo, proceed as follows.

**Run the installer.** Allow scripts **for this session only**, then build and test by launching a test server.

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\install_on_windows.ps1 setup
.\install_on_windows.ps1 test_server
```

**Activate the virtual environment.** The setup script activates `venv` for you. You can re-activate later with either command.

```powershell
# Using the script
.\install_on_windows.ps1 use_venv
# Direct command
.\venv\Scripts\Activate.ps1
```

This mirrors the POSIX setup and launches the test server with the installed `summoner` package.

</details>

<!-- 
<details>
<summary><img alt="Package icon" width="16" src="https://cdn.simpleicons.org/pypi/008f99"> <b>Create your package under <code>tooling/</code></b></summary>
<br>

**What goes where and why**

* Put your Python package folders inside `tooling/`. Each folder under `tooling/` is treated as a package during development and later becomes a peer of the native SDK packages during the merge step.
* Put a single `requirements.txt` at the **repo root**. The SDK builder looks for it there when composing environments. Keeping it at the top level avoids duplication and makes installs predictable.

**Folder shape (single package)**

```txt
tooling/
  your_package/
    __init__.py          # optional exports, e.g., "from .agent import Agent"
    agent.py             # your code
    utils.py             # optional helpers
requirements.txt         # at repo root (used during SDK composition)
```

**Folder shape (multiple packages from one repo)**
You may ship more than one package from the same module repo.

```txt
tooling/
  pkg_alpha/
    __init__.py
    alpha.py
  pkg_beta/
    __init__.py
    beta.py
requirements.txt
```

**Naming guidelines**

* Use lowercase names with underscores for package folders, for example `your_package`.
* Avoid hyphens in package names.
* Choose names that will not collide with other modules when merged into the SDK.

**How to import during development**

Write imports against `tooling.*` so your code runs **before** the merge:

```python
from tooling.your_package import Agent
from tooling.your_package.utils import helper
```

This matches the template convention and keeps your code runnable while it is still under `tooling/`.

In comparison, imports from the core SDK should use `summoner.*`:

```python
from summoner.client import SummonerClient
```

**Why the import shape changes later**

During the SDK build, the builder copies `tooling/your_package/` to `summoner/your_package/` and rewrites internal imports to place your package at the same level as native ones. After the merge, **code inside the SDK** uses:

```python
from your_package import Agent
from your_package.utils import helper
```

Likewise, imports that referenced the core SDK from within your module are rewritten to their internal, SDK-local form:

```python
from client import SummonerClient
```

Consumers of the **installed SDK** then import through the public namespace:

```python
from summoner.your_package import Agent
from summoner.your_package.utils import helper
from summoner.client import SummonerClient
```

**Optional shim for local development**

If you reference `tooling.*` from files that may later live under `summoner/`, add a minimal path shim so the same file works both before and after the merge:

```python
# place near the top of files that import from tooling.*
import os, sys
root = os.path.dirname(os.path.abspath(__file__))
repo_root = os.path.abspath(os.path.join(root, "..", ".."))
if repo_root not in sys.path:
    sys.path.insert(0, repo_root)
```

**About `requirements.txt`**

* Keep it at the **repo root**. The SDK builder installs this file when composing your SDK.
* Pin versions for repeatability when possible. Example:

```txt
# requirements.txt at repo root
aiohttp>=3.9,<4.0
pydantic>=2.6,<3.0
```

**Quick sanity check**

With your virtual environment active:

```bash
python -c "import tooling.your_package as yp; print('OK:', yp.__name__)"
```

If this passes, you are ready to iterate on your module and later merge it into an SDK build.

</details> -->











---








### <img alt="Merge into SDK" src="https://img.shields.io/badge/Merge%20into%20SDK-00bcd4"> Merge module into SDK

This section explains how to structure your module so that it merges accurately into an SDK build. The installer behavior is covered earlier. Here we focus on conventions, layout, imports, and dependency planning.

<details>
<summary><img alt="Map" width="16" src="https://cdn.simpleicons.org/textpattern/00bcd4"> <b>Plan your repository layout for merging</b></summary>
<br>

**What the builder expects**

* All exportable code lives under `tooling/` as package folders. Each folder becomes a top-level package in the SDK under `summoner/<pkg>/`. This is why names must be stable and conflict-free.
* A single `requirements.txt` sits at the **repo root**. The SDK builder reads it during composition. Keeping one place for dependencies avoids duplication and surprises.

**Canonical shapes**

Single package:

```txt
tooling/
  your_package/
    __init__.py          # optional exports, e.g., "from .agent import Agent"
    agent.py
    utils.py
requirements.txt         # at repo root (used during SDK composition)
```

Multiple packages from one repo:

```txt
tooling/
  pkg_alpha/
    __init__.py
    alpha.py
  pkg_beta/
    __init__.py
    beta.py
requirements.txt
```

If you need subpackages, mirror the same pattern with directories:

```txt
tooling/
  your_package/
    __init__.py
    subpkg/
      __init__.py
      feature.py
requirements.txt
```

**Naming guidelines**

* Use lowercase with underscores for package folders, for example `your_package`. This avoids import issues on case-sensitive filesystems.
* Avoid hyphens in folder names. Dashes are not valid in Python import paths.
* Choose names that will not collide with packages contributed by other modules. If you are unsure, prefix with a short, consistent stem, for example `acme_utils`.

A few minutes spent here prevents most merge conflicts later.

</details>

<details>
<summary><img alt="Arrows" width="16" src="https://cdn.simpleicons.org/python/00bcd4"> <b>Import strategy before and after merge</b></summary>
<br>

**During development in your module repo**

Write imports against `tooling.*` so the code runs before the merge:

```python
from tooling.your_package import Agent
from tooling.your_package.utils import helper
```

Core SDK imports should always use the public namespace:

```python
from summoner.client import SummonerClient
```

This separation is intentional. It lets your module run in isolation while still using the public APIs of the core SDK.

**What changes at merge time**

When you compose an SDK, the builder copies `tooling/your_package/` to `summoner/your_package/` and rewrites internal imports so your package becomes a peer of native SDK packages.

* Imports that referenced your package:

  ```python
  # before merge (in module repo)
  from tooling.your_package import Agent

  # after merge (inside the SDK source tree)
  from your_package import Agent
  ```

* Imports that referenced the core SDK from within your module:

  ```python
  # before merge (in module repo)
  from summoner.client import SummonerClient

  # after merge (inside the SDK source tree)
  from client import SummonerClient
  ```

The rewrite is mechanical. It expects clean, absolute imports. Avoid deep relative imports like `from . import something` across distant folders. Keep intra-package imports either absolute within your package or local, for example `from .utils import helper`.

**How consumers import after installation**

Users of the installed SDK import through the `summoner` namespace:

```python
from summoner.your_package import Agent
from summoner.your_package.utils import helper
from summoner.client import SummonerClient
```

If you expose a minimal public surface in `__init__.py` (using `__all__`), consumers get a simpler experience:

```python
# tooling/your_package/__init__.py
from .agent import Agent
__all__ = ["Agent"]
```

This keeps imports stable even if your internal files change.

**Optional local shim**

If a file might later live under `summoner/` but you run it from the module repo during development, you can add a small path shim so `tooling.*` imports resolve locally:

```python
# place near the top of files that import from tooling.*
import os, sys
root = os.path.dirname(os.path.abspath(__file__))
repo_root = os.path.abspath(os.path.join(root, "..", ".."))
if repo_root not in sys.path:
    sys.path.insert(0, repo_root)
```

Use the shim only in entry points or dev scripts. Avoid sprinkling it across library code.

</details>

<details>
<summary><img alt="Checklist" width="16" src="https://cdn.simpleicons.org/pypi/00bcd4"> <b>Dependencies and versioning</b></summary>
<br>

**One file per module repo**

* Put `requirements.txt` at the **repo root**. The SDK builder installs from this file during composition.
* Prefer compatible-range pins for libraries you do not control, and exact pins for tools that must match across modules.

Example:

```txt
# requirements.txt at repo root
aiohttp>=3.9,<4.0
pydantic>=2.6,<3.0
```

If you ship optional extras for local experiments, document them separately, for example `requirements.dev.txt`, and keep them out of the main build to avoid bloating the SDK.

**Agent-specific dependencies**

If your repo also ships runnable agents, keep their extra dependencies in the agent folders’ own `requirements.txt`. The SDK composition uses the repo-root `requirements.txt` only. Agents can install their own extras at run time.

**Non-code assets**

If your package needs data files at run time, place them inside your package and load them via package-relative paths, not absolute file paths. This keeps things working after the merge.

</details>

<details>
<summary><img alt="Magnifier" width="16" src="https://cdn.simpleicons.org/checkmarx/00bcd4"> <b>Pre-merge self checks</b></summary>
<br>

Run these checks inside your module repo with the virtual environment active. They catch most issues early.

**Package import check**

```bash
python -c "import tooling.your_package as yp; print('OK:', yp.__name__)"
```

**Core import check**

```bash
python -c "from summoner.client import SummonerClient; print('OK')"
```

**Name collision check**

* Verify that each folder directly under `tooling/` has a unique, descriptive name.
* If you plan to include multiple modules in the same SDK, list their package names and check for overlaps.

**Public surface check**

* Inspect `tooling/your_package/__init__.py`. Export only the symbols you want users to see. Keep internal helpers unexported.

If these pass, your module is ready to be composed into an SDK.

</details>

<details>
<summary><img alt="Magnifier" width="16" src="https://api.iconify.design/tabler/alert-triangle.svg?color=%2300bcd4&width=16"> <b>Common pitfalls</b></summary>
<br>

* Placing `requirements.txt` under `tooling/`. Keep it at the repo root or the builder will not find it.
* Using hyphens in package folder names. Use underscores to keep imports valid.
* Mixing relative and absolute import styles. Prefer clean absolute imports inside your package and the `summoner.*` namespace for core.
* Side effects in `__init__.py`. Keep it light. Heavy work in `__init__.py` can surprise users when they import.
* Hard-coded absolute paths to data files. Use package-relative reads so the same code works before and after merge.
* Exporting everything. Expose a minimal API with `__all__` to avoid breaking downstream code when internals change.

A quick sweep for these issues saves time during composition.

</details>





---

Docs
- server (beginner, quick, fundamentals, advanced)
- client
- receive/send
- routes and states
- hooks
- travel
- events







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

