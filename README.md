# CodeForge

**CodeForge** is an extensible WPF-based code editor prototype built with C# and .NET.

The project focuses on layered software architecture, separation of concerns, syntax highlighting and plugin-based extensibility.

---

## Overview

CodeForge was created as a study project to explore how a desktop application can be structured into multiple layers while keeping the editor extensible through plugin contracts.

The goal is not to replace professional IDEs such as Visual Studio or VS Code.  
Instead, CodeForge demonstrates the architecture of a modular editor application with a dedicated extension layer.

The project combines:

- a WPF desktop user interface
- a multi-project .NET solution
- separate presentation, application, domain, infrastructure and plugin-contract layers
- plugin contracts for extensibility
- editor-related functionality such as syntax highlighting
- StyleCop-based code quality rules

---

## Features

- WPF-based desktop editor shell
- layered project structure
- plugin contract separation
- syntax highlighting / editor-related functionality
- custom editor architecture
- StyleCop-based code style enforcement

---

## Tech Stack

- **C#**
- **.NET 9**
- **WPF**
- **XAML**
- **StyleCop.Analyzers**
- **Layered Architecture**
- **Plugin Contracts**

---

## Project Structure

```text
CodeForge
├── Editor.Presentation
│   └── WPF user interface and application entry point
│
├── Editor.Application
│   └── Application services and orchestration logic
│
├── Editor.Domain
│   └── Core domain models and editor concepts
│
├── Editor.Infrastructure
│   └── Infrastructure-related implementations
│
├── Editor.PluginContracts
│   └── Contracts used by extensions/plugins
│
└── Editor.sln
```

---

## Architecture

CodeForge follows a layered architecture approach.

The main idea is to avoid putting all logic directly into the WPF presentation layer.  
Instead, the application is split into multiple projects with clear responsibilities.

| Layer | Responsibility |
|---|---|
| `Editor.Presentation` | WPF UI, views, view models and application entry point |
| `Editor.Application` | Application services and orchestration logic |
| `Editor.Domain` | Core domain abstractions and editor concepts |
| `Editor.Infrastructure` | Infrastructure-specific implementations |
| `Editor.PluginContracts` | Shared contracts for plugin-based extensibility |

This structure makes the project easier to extend, reason about and maintain.

---

## Plugin Concept

One of the central ideas behind CodeForge is extensibility.

The project contains a dedicated `Editor.PluginContracts` project that defines the contracts used by plugins or extensions.  
This keeps plugin-facing abstractions separated from the concrete application implementation.

The goal is to make it possible to add editor functionality without tightly coupling every feature directly to the WPF presentation layer.

---

## Screenshots

### Editor Preview

![CodeForge Preview](Vorschau.png)

### Architecture

![CodeForge Architecture](Architektur.png)

---

## Demo

A short demo video is included in the repository:

[Watch demo video](Editor%20Video.mp4)

---

## Requirements

To build and run this project, you need:

- Windows
- .NET 9 SDK
- Visual Studio 2022 or newer
- .NET desktop development / WPF workload

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/Katharon/CodeForge.git
cd CodeForge
```

Restore dependencies:

```bash
dotnet restore
```

Build the solution:

```bash
dotnet build Editor.sln
```

Run the WPF project:

```bash
dotnet run --project Editor.Presentation/Editor.Presentation.csproj
```

Alternatively, open `Editor.sln` in Visual Studio and start the `Editor.Presentation` project.

---

## Project Status

CodeForge is currently a prototype / study project.

The main goal is to demonstrate software architecture, WPF development and extensibility through plugin contracts.  
Some parts may still be experimental and are not production-ready.

---

## What I Learned

This project helped me deepen my understanding of:

- WPF desktop application development
- structuring larger C# applications
- separating presentation, application and domain concerns
- designing plugin contracts
- working with multi-project .NET solutions
- applying code style rules with StyleCop
- thinking about extensibility and maintainability

---

## Repository Notes

The repository was originally created under the internal project name `Editor`.  
The public project name is now **CodeForge**.

---

## License

No license has been specified yet.
