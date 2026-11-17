# Awesome-Low-Code-Mobile-Test-Automation

# Awesome Low-Code Mobile Test Automation

> A curated list of top Low-Code Mobile Test Automation platforms — both SaaS/Hosted commercial solutions and open-source alternatives for recording, authoring, and executing mobile app tests with minimal coding.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [BrowserStack App Low-Code Automation](#browserstack-app-low-code-automation)
  - [Katalon Studio](#katalon-studio)
  - [Testim Mobile](#testim-mobile)
  - [Repeato](#repeato)
  - [Sofy.ai](#sofyai)
  - [Waldo (Tricentis)](#waldo-tricentis)
  - [Maestro Cloud](#maestro-cloud)
- [Open-Source Software](#-open-source-software)
  - [Appium](#appium)
  - [Maestro (Open Source)](#maestro-open-source)
  - [Hydra Lab](#hydra-lab)
  - [Dogu](#dogu)
  - [Pickleib](#pickleib)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Low-Code Mobile Test Automation platforms. These are not open-source but are included as reference points for feature comparison.

### BrowserStack App Low-Code Automation
**Type:** AI-driven recorder with zero-setup cloud execution
BrowserStack's App Low-Code Automation lets teams state test objectives in plain English and have AI generate automated mobile tests, with AI-assisted selectors that avoid XPaths and self-healing that adapts to UI changes [citation:1]. It supports manual DSL commands for fine-tuning, modules for reusable steps, variables, version history, and data-driven testing. Tests run instantly on **30,000+ real devices** with no setup, emulators, or simulators required [citation:1]. It covers functional, accessibility, local, and geolocation testing, with daily insights and logs delivered to your inbox [citation:1]. Reviewers highlight the recording aspect as intuitive for non-technical users and the module feature as valuable for reuse [citation:1].  
**Best for:** Teams wanting a polished, zero-setup mobile recorder with AI-assisted authoring and execution on BrowserStack's real device cloud.

### Katalon Studio
**Type:** Low-code IDE with cloud-based mobile recorder
Katalon Studio's **Mobile Recorder** allows recording objects on **cloud devices** starting from version 9.5.0, eliminating complex local setups and making mobile testing accessible to users with minimal coding experience [citation:2]. You upload your app to TestOps, select a device (e.g., Android 14 on Galaxy S24), and interact with the app in a mirrored Device View while Katalon captures objects in a tree structure [citation:2]. Recorded actions become test steps, with options to add, remove, or reorder actions before saving. Locator strategies can be changed and verified with a Highlight function [citation:2]. **Trade-off:** Cloud mobile recording requires a Test Execution - Cloud Mobile Native App testing subscription [citation:2].  
**Best for:** Teams wanting a mature IDE that supports both local and cloud-based mobile recording with granular control over locators and test steps.

### Testim Mobile
**Type:** AI-based low-code testing with Enhanced Mode for cross-platform apps
Testim Mobile provides low-code authoring for iOS and Android, with **Enhanced Mode** specifically designed for cross-platform and hybrid apps—React Native, Flutter, and apps with embedded web views—using proprietary technology that understands the application's internal structure for more stable tests [citation:14]. It supports test authoring and execution on a **Virtual Mobile Grid** in the cloud, as well as local physical devices, emulators, and simulators. Enhanced Mode enables test scenarios that were previously impossible with Appium [citation:14]. **Trade-off:** Native mobile support was in beta as of the preview announcement, with device lifecycle management handled via the Tricentis Mobile Agent [citation:3].  
**Best for:** Teams building React Native, Flutter, or hybrid apps who have struggled with Appium's limitations on cross-platform frameworks.

### Repeato
**Type:** Computer vision-based no-code testing with local-first execution
Repeato uses **computer vision and machine learning** to recognize UI elements from screen pixels, working without source code, element IDs, or reliable view hierarchies [citation:15]. It supports Flutter, React Native, Xamarin, Unreal Engine, and native iOS/Android apps, with execution on local devices, simulators, or in CI via the Repeato CLI [citation:4][citation:15]. Key characteristics include visual fingerprints for element matching, OCR and locator fallbacks, and a **local-first architecture** where Studio works offline and tests remain in a normal workspace directory [citation:15]. **Trade-off:** Visual fingerprints may need updating after meaningful design changes, and cloud features are optional rather than core [citation:15].  
**Best for:** Teams wanting no-code mobile automation that works without source code access, particularly for cross-platform frameworks where Appium struggles.

### Sofy.ai
**Type:** AI agents for no-code real-device mobile testing
Sofy provides **AI Mobile Testing Agents** that generate, execute, and maintain tests across real devices without writing scripts [citation:6]. It offers access to **2,000+ real device configurations**, performance profiling (CPU, memory, battery, network), app store compliance validation, and parallel testing. Native CI integrations include GitHub Actions, Azure DevOps, CircleCI, and GitLab [citation:6]. Pricing is pay-per-test with no monthly commitments [citation:6].  
**Best for:** Teams wanting AI-agent-driven mobile testing on real devices with per-test pricing and existing CI pipeline integration.

### Waldo (Tricentis)
**Type:** Cloud-based mobile testing with best-in-class view tree
Waldo (acquired by Tricentis) provides mobile testing with a focus on **simplicity** (no Appium install, no local configuration) and **universality** (same remote device environment every run) [citation:5]. Its standout claim is a **best-in-class view tree** that "sees" the structure of mobile views better than other tools—enabling test flows that are not possible on other platforms, particularly for hybrid apps (React Native, Flutter, Ionic) where Appium support is poor [citation:5]. Session Replays capture video, device logs, and network requests with synchronized interaction timelines, shareable via public links [citation:5].  
**Best for:** Teams with hybrid or cross-platform apps where element visibility is a persistent problem, and who value rich session replay artifacts for debugging.

### Maestro Cloud
**Type:** Managed cloud execution for Maestro flows
Maestro Cloud provides **enterprise-grade infrastructure** for parallel execution of Maestro test flows, eliminating local emulator/simulator configuration and reducing test execution time by up to **90%** through asynchronous parallel runs [citation:8]. It supports device isolation (every virtual device wiped between tests), flexible configuration (Android API levels, iOS models), global testing via `--device-locale`, and cross-platform support for Android (Views/Compose), iOS (UIKit/SwiftUI), React Native, Flutter, and Web [citation:8]. Native CI integrations include GitHub Actions, Bitrise, Bitbucket Pipelines, and CircleCI, with PR integration for GitHub that can block merges on test failures [citation:8].  
**Best for:** Teams already using Maestro's YAML-based flows who need parallel cloud execution without managing local emulators.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Low-Code Mobile Test Automation tools. The open-source ecosystem spans **full cross-platform automation frameworks**, **declarative YAML-based testers**, **distributed test execution platforms**, **older GUI-based tools**, and **BDD-style step libraries**.

### Appium
**Stack:** Node.js (core) with clients for Java, Python, JS, Ruby, C# | **License:** Apache-2.0
Appium is the foundational open-source mobile automation framework, using the **W3C WebDriver protocol** for native iOS and Android automation. It is not low-code in the visual recorder sense—tests are written in code—but it is the **engine underneath many commercial low-code tools**, and its ecosystem includes the **Appium Inspector** GUI for element inspection and locator generation. Performance studies show Appium has the **fastest average test execution time (10.50 sec)** and the most **linear scaling (1.92)** under parallel sessions among compared platforms [citation:7].  
**Best for:** Engineering teams wanting full code-level control and the broadest ecosystem support, accepting that low-code authoring requires additional tooling.

### Maestro (Open Source)
**Stack:** Java / YAML flows | **License:** Apache-2.0
Maestro is an open-source UI automation framework that uses **human-readable YAML flows** interpreted at runtime rather than compiled, with built-in tolerance that handles network delays and UI flakiness by waiting for the screen to settle [from previous context]. It supports Android, iOS (simulators), React Native, Flutter, and Web, with a single-script installation and no "setup hell." The open-source version runs locally; Maestro Cloud is the managed parallel execution layer [citation:8].  
**Best for:** Teams wanting a lightweight, declarative mobile testing framework with YAML-based flows that can run locally or scale to Maestro Cloud.

### Hydra Lab
**Stack:** Java / Spring Boot / React / Docker | **License:** MIT (Microsoft)
Hydra Lab is a framework from Microsoft for building a **self-hosted cloud testing platform** using devices in hand, with a center-agent architecture, test task management, and result visualization. It supports **Appium (Java), Espresso, XCTest, Maestro, and Python Runner** across Android, iOS, Windows, and Web. Performance studies show Hydra Lab has a **scalability coefficient of 1.88** (near-linear scaling) and an average execution time of **11.32 sec**—second only to Appium among compared platforms [citation:7]. An out-of-box Docker image runs both center and agent instances [from previous context].  
**Best for:** Teams wanting a proven, Microsoft-backed framework to build their own cloud testing platform with multi-framework support.

### Dogu
**Stack:** (Check repository) | **License:** Open Source
Dogu is an open-source mobile test automation tool with its own GUI, device viewing, and Appium as its WebDriver backend—positioned as an **overlay on Appium** that adds convenience features not present in Appium by default [citation:7]. **Important performance findings:** Dogu showed the **worst performance and stability** among compared platforms, with the highest average test execution time (**12.88 sec**) and a **scalability coefficient of 3.43** (meaning it loses significant performance under parallel load) [citation:7]. It also had **no significant updates since 2022** as of the study, raising concerns about long-term support [citation:7].  
**Best for:** Historical reference or small-scale use where its GUI conveniences outweigh performance concerns; not recommended for large parallel test suites.

### Pickleib
**Stack:** Java / Cucumber / Playwright & Appium | **License:** Open Source (GitHub)
Pickleib is a test automation library that provides **built-in Cucumber step definitions** for WebUI, MobileUI, Desktop UI, API, Email, Database, and Localisation, with a focus on **low-code BDD-style test authoring** [citation:11]. For mobile, it wraps Appium with human-readable steps like `Fill input {element} on the {Page} with text: {value}`, `Verify presence of element`, and `Scroll until listed {element} is found` [citation:11]. It auto-detects page repository JSON or scans for `@PageObject`/`@ScreenObject` classes, reducing boilerplate for teams writing Cucumber tests.  
**Best for:** Teams using Cucumber/BDD who want ready-made mobile step definitions on top of Appium without writing glue code.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Visual Recorder | Cloud Execution | Self-Hosted | Best For |
|----------|---------|-------|-----------------|-----------------|-------------|----------|
| **BrowserStack** | Proprietary | Cloud | ✅ | ✅ 30,000+ devices | ❌ | Zero-setup AI recording |
| **Katalon Studio** | Proprietary | Desktop + Cloud | ✅ Cloud Mobile Recorder | ✅ TestCloud | (Desktop) | Mature IDE + cloud recording |
| **Testim Mobile** | Proprietary | Cloud | ✅ Enhanced Mode | ✅ Virtual Mobile Grid | ❌ | React Native / Flutter / Hybrid |
| **Repeato** | Proprietary | Desktop + CI | ✅ Computer vision | ✅ CLI headless | ✅ (Local) | No source code needed |
| **Sofy.ai** | Proprietary | Cloud | ✅ AI agents | ✅ 2,000+ devices | ❌ | AI agents + pay-per-test |
| **Waldo** | Proprietary | Cloud | ✅ | ✅ | ❌ | Best-in-class view tree for hybrid |
| **Maestro Cloud** | Proprietary | Cloud | (YAML flows) | ✅ Parallel | ❌ | Maestro flows at scale |
| **Appium** | Apache-2.0 | Node.js + clients | (Inspector GUI) | (Via grids) | ✅ | Full control + ecosystem |
| **Maestro OSS** | Apache-2.0 | Java / YAML | (YAML flows) | (Local only) | ✅ | Declarative YAML testing |
| **Hydra Lab** | MIT | Java/Spring/Docker | (Check) | ✅ Center-agent | ✅ | Multi-framework cloud platform |
| **Dogu** | Open Source | (Check) | ✅ GUI | (Check) | ✅ | Small-scale GUI use (perf caution) |
| **Pickleib** | Open Source | Java/Cucumber | (BDD steps) | (Via Appium) | ✅ | BDD mobile step definitions |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Low-Code Mobile Test Automation tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The open-source landscape for **low-code mobile test automation** is **led by Appium** as the foundational engine, with **Maestro** providing the most accessible declarative YAML-based alternative and **Hydra Lab** offering the strongest self-hosted cloud platform with proven near-linear scaling [citation:7]. **Dogu** provides GUI conveniences over Appium but has significant performance and maintenance concerns—it showed the worst scalability and has not had significant updates since 2022 [citation:7]. **Pickleib** fills a niche for BDD/Cucumber teams wanting pre-built mobile step definitions. No open-source project fully replicates BrowserStack's AI-driven zero-setup authoring or Waldo's best-in-class view tree for hybrid apps, but these tools cover the core low-code and declarative mobile testing workflows for self-hosted deployments.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
