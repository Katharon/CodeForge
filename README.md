# CodeForge

**CodeForge** is an extensible WPF-based code editor prototype built with C# and .NET.  
The project focuses on clean architecture, separation of concerns, syntax highlighting and plugin-based extensibility.

It was created as a study project to explore how a desktop application can be structured into separate layers while keeping the editor extensible through plugin contracts.

---

## Overview

CodeForge is not intended to be a full replacement for professional IDEs such as Visual Studio or VS Code.  
Instead, it demonstrates the architecture of a modular editor application with a dedicated plugin layer.

The project combines:

- a WPF desktop user interface
- a layered solution structure
- separate application, domain, infrastructure and presentation projects
- plugin contracts for extensibility
- syntax highlighting / editor-related functionality
- StyleCop-based code quality rules

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
│   └── Contracts used by external extensions/plugins
│
├── Extensions
│   └── Extension/plugin-related components
│
└── Editor.sln
