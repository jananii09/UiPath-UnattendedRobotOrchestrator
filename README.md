# UiPath - Unattended Robot Automation with Orchestrator

This repository contains a **UiPath automation project** demonstrating how to run a workflow using an **Unattended Robot** connected through **UiPath Orchestrator**.  
The project covers everything from workflow creation to publishing, robot setup, and job execution via Orchestrator.

---

## Project Overview
- **Built using**: UiPath Studio (Modern Design Experience)
- **Goal**: Automate a workflow using an **Unattended Robot** managed entirely through **UiPath Orchestrator**
- **Focus Areas**:
  - Orchestrator setup (Machines, Robots, Folders, Processes)
  - Publishing projects from Studio to Orchestrator
  - Executing jobs without human intervention  
  - Scheduling triggers for automation

---

## Technologies & Components Used
- **UiPath Orchestrator**  
  For managing Machines, Robots, Assets, Jobs, and Triggers

- **Unattended Robot**  
  Service-mode execution on a target machine

- **UiPath Assistant**  
  Connects the machine to Orchestrator via Machine Key

- **Publishing Package**  
  Uploading workflow from Studio to Orchestrator

- **Job Scheduling**  
  Triggering unattended execution (time-based or manual)

---

## Project Files
- `Main.xaml` → Main workflow executed by the robot  
- `project.json` → Project metadata & package dependencies  
- Supporting Dependencies → Added via Manage Packages (UiPath.System.Activities, UiPath.UIAutomation.Activities, etc.)

---

## Workflow Logic

### 1 **Workflow Execution**
This project contains a simple workflow that:
- Performs automated steps without requiring human input  
- Ensures compatibility with unattended execution (no Message Boxes/Input Dialogs)

### 2️**Publish to Orchestrator**
- Workflow is published directly from UiPath Studio  
- Visible under **Orchestrator → Automations → Processes**

### 3️ **Unattended Robot Configuration**
- Machine Template created in Orchestrator  
- Machine Key added to UiPath Assistant  
- Robot provisioned with valid Windows credentials  
- Robot appears as **Connected (Licensed)** in Orchestrator

### 4️ **Triggering the Job**
- Job can be started manually from Orchestrator  
- Or set to run automatically using **Time Triggers**

---

## Execution Flow (Step-by-Step)

1. Create UiPath process  
2. Define Machine Template in Orchestrator  
3. Connect UiPath Assistant using Machine Key  
4. Configure **Unattended Robot** with Windows credentials  
5. Publish project from Studio  
6. Create a **Process** in Orchestrator  
7. Run Job manually or schedule trigger  
8. Monitor Logs, Output, and Job Status from Orchestrator

---

## Output Example
After execution, Orchestrator logs display:

- **Job Status**: Successful  
- **Robot Name**: UnattendedRobot01  
- **Start Time**: 2025-11-20 10:30:15  
- **End Time**: 2025-11-20 10:30:28  
- **Execution Logs**:  
  - Workflow Started  
  - Step 1 Completed  
  - Step 2 Completed  
  - Workflow Finished  

---

## Screenshots

<img width="1399" height="777" alt="image" src="https://github.com/user-attachments/assets/2ffbc8ce-e672-4d8d-8685-67d2e952c83c" />

---
