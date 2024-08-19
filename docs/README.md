# About Coder

Coder is an open-source platform for creating and managing developer workspaces in your preferred cloud or server environment.

<p align="center">
  <img src="./images/hero-image.png">
</p>

Built on top of tools like SSH, containers, and Terraform, Coder remote workspaces are accessible for teams of all sizes and approachable no matter where your organization is in its cloud-native journey.

Coder workspaces are defined and provisioned using Terraform, an infrastructure as code tool. If you don't know Terraform yet, Coder's library of preconfigured templates will get you running and productive without heavy configuration. If you've used Terraform in the past, you can put that knowledge to use right away to craft custom environments.

<blockquote class="warning">
  <p>
  If you are a Coder v1 customer, view <a href="https://coder.com/docs/coder">the docs</a> or <a href="https://coder.com/docs/coder/latest/guides/v2-faq">the sunset plans</a>.
  </p>
</blockquote>

## How it works

With Coder, individual development environments are represented as workspaces. Workspaces are created from templates that define environment configurations.

### Templates

Users with the [template admin role](./admin/users.md#roles) create [templates](./templates/index.md) to define developer environments using tools like Terraform and Docker. Choose the tools and resources your project needs, the platform you want to run on, and the people who can access it.

You can create templates from scratch or use a starter template to get started. All of your changes are versioned with the ability to promote changes, control when workspaces are started or stopped, and more.

<p align="center">
  <img src="./images/providers-compute.png">
</p>

Coder workspaces aren't limited to compute. Easily provision storage buckets, secrets, sidecars, or any other resources Terraform can represent.

[Learn more about managing infrastructure](./templates/index.md).

### Workspaces

Developers use these templates to provision [workspaces](./workspaces.md): individual development environments provisioned using identical configurations.

Connect seamlessly with your favorite IDE like [VS Code](./ides/vscode-extensions.md) or [JetBrains](./ides/gateway.md) or log in directly using [SSH](./ides.md#ssh-configuration). If a new version of the template is published, you'll have the option to upgrade your workspace immediately.

<p align="center">
  <img src="./images/ide-icons.svg" height=72>
</p>

You can use any Web IDE ([code-server](https://github.com/coder/code-server), [projector](https://github.com/JetBrains/projector-server), [Jupyter](https://jupyter.org/), etc.), [JetBrains Gateway](https://www.jetbrains.com/remote-development/gateway/), [VS Code Remote](https://code.visualstudio.com/docs/remote/ssh-tutorial) or even a file sync such as [mutagen](https://mutagen.io/).

## Using Coder

The following pages can help you get started using Coder.

- [Installation](./install/index.md): Install the Coder CLI or launch a local Coder server for testing
- [Quickstart](./quickstart.md): Learn how to get started with Coder and create your first development environments
- [Templates](./templates/index.md): Find out more about how to create and manage templates to create your ideal development environments
- [Workspace](./workspaces.md): Launch and manage workspaces to make the transition to remote development
- [IDEs](./ides.md): Connect to your workspaces with your favorite IDE
- [Dotfiles](./dotfiles.md): Customize your workspaces by bringing along your personal dotfiles

## Managing Coder

If you are setting up Coder for your organization, these pages can provide guidance:

- [Installation](./install/index.md): Install the Coder server on a variety of platforms and environments
- [Architecture](./architecture/architecture.md): Understand Coder's architecture, components, and dependencies, and learn more about how to implement a production-ready deployment
- [Platforms](./platforms/README.md): Guidance on how to get started with Coder on specific platforms
- [Networking](./networking/index.md): Learn about Coder's network topology and how workspaces, Coder servers, and users connect to one another
- [Secrets](./secrets.md): Configure access to secrets from your organization's workspaces
- [Administration](./administration/README.md): Find out more about user management, authentication, resource quotas, scaling, logs, and more.
- [Guides](./guides/index.md): Read more user guides to get more out of your Coder instance.
- [Enterprise features](./enterprise.md): Evaluate enterprise features to determine if you would benefit from a paid license.

## Why choose remote development?

Migrating from local developer machines to workspaces hosted by cloud services is a choice that is growing in popularity for both [individual developers](https://blog.alexellis.io/the-internet-is-my-computer/) and [organizations](https://slack.engineering/development-environments-at-slack) alike. Some of the benefits include:

- **Easier environment management:** Tools such as Terraform, nix, Docker, devcontainers make it easier to onboard developers and troubleshoot development environment issues
- **Increased speed:** Server-grade compute accelerates many areas of software development including IDE load times, code compilation and building, and running large workloads for both monolith or microservice applications
- **Increase security:** Centralize source code and other important data on company-managed servers or cloud services instead of local developer machines
- **Improved compatibility:** Remote workspaces share infrastructure configuration with other developers and across development, staging, and production environments, reducing configuration drift
- **Improved accessibility:** Connect to remote workspaces via browser-based IDEs, remote IDE extensions, or SSH to develop from low-powered devices like lightweight notebooks, Chromebooks, and iPads

## What makes Coder different?

The main difference between Coder and other remote IDE platforms is the level of infrastructure control. Coder allows admins to:

- Support ARM, Windows, Linux, and macOS workspaces
- Modify pod/container specs (e.g., adding disks, managing network policies, setting/updating environment variables)
- Use VM/dedicated workspaces, developing with Kernel features (no container knowledge required)
- Enable persistent workspaces, which are like local machines, but faster and hosted by a cloud service

Coder includes [production-ready templates](https://github.com/coder/coder/tree/c6b1daabc5a7aa67bfbb6c89966d728919ba7f80/examples/templates) for use with AWS EC2, Azure, Google Cloud, Kubernetes, and more.

## Common misconceptions: what Coder is _not_

Developer tools come in all shapes and sizes. Sometimes it's difficult to understand how they fit into other parts of the developer ecosystem.

Coder is not...

- an **infrastructure as code (IaC) platform:** Terraform is the first IaC _provisioner_ in Coder, allowing Coder admins to define Terraform resources as Coder workspaces.
- a **DevOps/CI platform:** Coder workspaces can follow best practices for cloud service-based workloads, but Coder is not responsible for how you define or deploy the software you write.
- an **online IDE:** Instead, Coder supports common editors, such as VS Code, vim, and JetBrains over HTTPS or SSH.
- a **collaboration platform:** You can use git and dedicated IDE extensions for pull requests, code reviews, and pair programming.
- a **SaaS/fully-managed offering:** You must host Coder on a cloud service (AWS, Azure, GCP) or your private data center.

## Up next

- Learn about [Templates](./templates/index.md)
- [Install Coder](./install/index.md#install-coder)
