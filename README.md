<h1 align="center">Ring Cloud Deployment Guides</h1>

<p align="center">
  <strong>The definitive guide to deploying Ring applications.</strong>
  <br />
  From modern PaaS providers and cloud servers with Docker to traditional shared hosting, we provide clear, production-ready tutorials to get you live.
</p>

<p align="center">
    <a href="https://github.com/ysdragon/deploy-ring/blob/main/LICENSE">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT" />
    </a>
    <a href="https://github.com/ysdragon/deploy-ring/pulls">
        <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome" />
    </a>
</p>

---

Deploying web applications can be complex. This repository simplifies that process for the **Ring programming language** by providing a collection of comprehensive, step-by-step tutorials for various hosting environments.

## 🎯 Core Philosophy

Our goal is to make these guides:

*   ✅ **Production-Ready:** Go beyond "hello world" with robust setups that include security, SSL, and best practices ready for real traffic.
*   📘 **Clear & Step-by-Step:** Provide easy-to-follow instructions that explain both the "how" and the "why."
*   🔧 **Flexible & Comprehensive:** Cover multiple popular hosting scenarios and tools, so you can choose the best fit for your project.

## 🚀 Which Tutorial is Right for Me?

Use this table to quickly decide which guide best fits your needs.

| If your hosting environment is... | Then choose this tutorial... | Key Technologies You'll Use |
| :--- | :--- | :--- |
| A **Managed Cloud Platform (PaaS)** where infrastructure, networking, and SSL are handled for you, and you want the simplest deployment. | 🚀 **Deploying to Modern Cloud Platforms** | `Docker`, `Fly.io`, `Railway.app` |
| A **Cloud VM** (AWS, GCP, DigitalOcean, etc.) with `root` or `sudo` access, where you want full control over your server stack. | 🐳 **Deploying with Docker & Reverse Proxy** | `Docker`, `HTTPLib`, `Nginx`, `Traefik`, `Caddy`, `Let's Encrypt` |
| **Shared Hosting** (cPanel, Plesk, etc.) with limited permissions (no background processes) and FTP/SFTP access. | 📜 **Deploying with CGI** | `Apache`, `LiteSpeed`, `CGI`, `Nginx`, `FastCGI` |

---

## 📚 Available Tutorials

### 🚀 1. Modern PaaS Deployment on Fly.io & Railway.app

[**➡️ Read the Tutorial: Deploying to Modern Cloud Platforms**](tutorials/ring_cloud_platforms.md)

This is the fastest and most straightforward path to a live, secure application. It's designed for developers who want to focus on code, not infrastructure. These platforms automatically build your Docker container and handle all the networking, SSL, and scaling for you.

**What you will learn:**
*   The core concepts of deploying to a Platform-as-a-Service (PaaS).
*   Deploying a containerized Ring application from your command line in minutes.
*   Using the **`flyctl`** CLI to launch an application on Fly.io's global network.
*   Using the **`railway`** CLI to instantly deploy an application on Railway.app.
*   Why this is the ideal approach for rapid prototyping and hassle-free deployments.

### 🐳 2. Modern Cloud Deployment with Docker & a Reverse Proxy

[**➡️ Read the Tutorial: Deploying with Docker**](tutorials/ring_cloud.md)

This guide covers the modern, industry-standard method for deploying web applications on cloud servers where you have full control. It demonstrates how to containerize your Ring `HTTPLib` application using **Docker** and manage it with a powerful reverse proxy.

**What you will learn:**
*   Containerizing a Ring web application built with `HTTPLib`.
*   Setting up a local development environment with **Docker Compose**.
*   Deploying to production with automatic, free **SSL (HTTPS)** from Let's Encrypt.
*   How to implement three different battle-tested reverse proxy setups:
    *   **Nginx:** For a classic, high-performance, and stable configuration.
    *   **Traefik:** For a modern, dynamic edge router that automatically discovers services.
    *   **Caddy:** For the ultimate simplicity with fully automated HTTPS out of the box.

### 📜 3. Traditional Hosting Deployment with CGI

[**➡️ Read the Tutorial: Deploying with CGI**](tutorials/ring_cloud_cgi.md)

This guide is perfect for developers on traditional hosting environments (like **cPanel** or **Plesk**) where running a persistent server process isn't an option. It covers the classic and highly compatible **CGI (Common Gateway Interface)** model.

**What you will learn:**
*   Creating a CGI-compatible Ring script (which does not use `HTTPLib`).
*   Using a universal, secure CGI wrapper script to execute your `.ring` files.
*   **Path A:** Deploying on shared hosting with **Apache/LiteSpeed**.
*   **Path B:** Deploying on a cloud VM with **Nginx** and `fcgiwrap`.
*   Platform-specific tips for **cPanel, Plesk, DirectAdmin, and KeyHelp**.

## 💡 How to Use These Tutorials

1.  **Check the Prerequisites:** Before you begin, ensure you have:
    *   A basic understanding of the [Ring programming language](https://ring-lang.github.io/).
    *   Familiarity with your computer's command line or terminal.
    *   For the PaaS guide: A free **Fly.io** or **Railway.app** account and their respective CLIs.
    *   For the Docker guide: **Docker** and **Docker Compose** installed.
    *   For the CGI guide: Access to a shared hosting account or a cloud VM.

2.  **Choose Your Guide:** Use the table above to select the tutorial that matches your hosting environment.

3.  **Follow the Steps:** Each tutorial is designed to be followed from start to finish. Clone this repository or simply read the guide directly on GitHub.

## 🤝 Contributing

Contributions are the lifeblood of the open-source community. Any contributions you make are **greatly appreciated**.

*   **Find an error?** Found a typo or a step that could be clearer? Open an issue or submit a pull request!
*   **Have a new guide?** We would love to include tutorials for other environments (e.g., different cloud providers, serverless platforms).
*   **Have a suggestion?** Let's hear your ideas for improving the existing tutorials!

Please feel free to [open an issue](https://github.com/ysdragon/deploy-ring/issues) or [submit a pull request](https://github.com/ysdragon/deploy-ring/pulls).

## License

This project is distributed under the MIT License. See the [`LICENSE`](LICENSE) file for more information.