# AI Interaction Guide for "Ultra World" Project

This is the central context file for the "Ultra World" project. It contains high-level instructions and pointers to more detailed documentation about the project's structure, the underlying NVGT API, and the tools at your disposal.

**CRUCIAL DIRECTIVE:** If you are ever unsure about something, if a task is not succeeding, or if you lack context, your primary directive is to **proactively investigate the codebase.** Use your tools to list files in directories, read their contents, and search for keywords. **Do not assume; verify by reading the files directly.**

---

## 1. Project Structure and Logic

For a detailed breakdown of the main files and directories, refer to the project overview. This file explains the roles of the client, the server, and their respective include directories.

@project_overview.md

---

## 2. Discovering the NVGT Engine API

The game is built on the Nonvisual Gaming Toolkit (NVGT). To understand the engine's built-in capabilities (e.g., sound, networking, UI), you must follow a systematic process of analyzing its C++ source code. This is your definitive guide for that process.

@nvgt_api_discovery.md

---

## 3. Core Tool Instructions

Before performing any action, review the core instructions for interacting with the file system and managing tasks. This ensures you use the most efficient and accurate tools for reading, searching, and creating plans.

@tools.md

---

## 5. Git Commit Message Conventions

Writing clear and consistent commit messages is crucial for maintaining a healthy and understandable project history. Here are the conventions to follow for this project.

### Structure

A good commit message has two parts: a subject and an optional body.

-   **Subject:** A short, single line (less than 50 characters) that summarizes the change. It should be in the imperative mood (e.g., "Fix bug", not "Fixed bug" or "Fixes bug").
-   **Body (Optional):** If the change is complex, add a blank line after the subject and write a more detailed explanation. Explain the "what" and "why" of the change, not the "how".

### Examples

#### Example 1: Simple Fix

For a small change, a subject line is often enough.

**Command:**
```bash
git commit -m "Fix: Correct calculation for player damage"
```

#### Example 2: New Feature (with Body)

For a more significant change, use a body to provide context.

**Command:**
```bash
git commit -m "Feat: Add /ping command for self-checking

- Allows any player to type /ping to check their own latency.
- Restricts pinging other players to admins to prevent spam.
- Adds an admin notification when an admin pings another player."
```

#### Example 3: Bad Commit Messages (to avoid)

*   `git commit -m "fix"` (Too vague. What was fixed?)
*   `git commit -m "Made some changes to the server file"` (Not specific. The "what" is obvious from the diff, the "why" is missing.)
*   `git commit -m "WIP"` (Work in progress should not be committed to the main branch.)
*   `git commit -m "Feat: Implement background muting"` (Too brief for a complex feature. Lacks the "why" and "what" in detail, especially if no body is provided.)

By following these conventions, we ensure that a thorough review of commit messages helps understand the project's evolution. To effectively understand the project's commit message style, always review past commit messages, including their full details. For example, use `git log -n 10` to see the last 10 commits, or simply `git log` without any parameters to display *all* commit messages with their full information (subject, author, date, and full description).

---

## 6. Documentation & Changelog Guidelines

Maintaining accurate and consistent documentation is as important as writing clean code.

### 6.1 Changelog Updates

-   **Files:**
    -   Server changes: `server/changelogs/server.md`
    -   Client changes: `server/changelogs/client.md`
-   **When to Update:** Whenever a feature is added, a bug is fixed, or a significant change is made that affects the user or developer experience.
-   **Process:**
    1.  **Read the file first:** Always use `read_file` to check the current structure and the most recent entry.
    2.  **Style:**
        -   New entry header: `## Changes on <DayOfWeek>, <Month> <Day>, <Year>` (e.g., `## Changes on Sunday, November 30, 2025`) OR `## Changes in <Version>` (e.g. `## Changes in 2.49.1`).
        -   If an entry for the current date/release already exists, append to it.
        -   Items: Use a bulleted list `- Description`.
        -   Tone: User-friendly and professional. (e.g., "Fixed a bug where...", "Added support for...", not "Changed code in file X").
    3.  **Credits:** If a specific user contributed to the fix/feature, credit them (e.g., `Thanks "User".`).

### 6.2 Commands Documentation

-   **File:** `server/commands.md`
-   **When to Update:** Whenever a new chat command is implemented or an existing one is modified (arguments, behavior).
-   **Process:**
    1.  **Read the file first:** Use `read_file` to see where the new command fits (categories like "General Commands", "Team Related Commands").
    2.  **Style:**
        -   Format: `- `command <arg1> [optional_arg]`: Description.`
        -   Ensure arguments are clearly marked with `< >` or `[ ]`.

**CRITICAL:** Before writing to any documentation file, you MUST read it to ensure your additions match the existing style and placement.

---

## 7. Git History Analysis

Use these commands to analyze the project history, generate changelogs, or debug regressions.

### 7.1 Viewing Commit Ranges

To list commits from a starting point up to the current state (HEAD).

*   **Include the starting commit:**
    Use `^` after the hash to include it in the range (literally "from the parent of this commit").
    ```bash
    git log <HASH>^..HEAD --pretty=format:"%h - %s %b"
    ```

*   **Exclude the starting commit (show only what came after):**
    ```bash
    git log <HASH>..HEAD --pretty=format:"%h - %s %b"
    ```

*   **Limit the number of commits:**
    Add `-n <NUMBER>` to show only the last N commits.
    ```bash
    git log -n 5
    ```

### 7.2 Viewing Changes (Diffs)

To see *what* changed in the code.

*   **Full diffs for a range:**
    Shows the patch output for every commit in the range.
    ```bash
    git log -p <HASH>^..HEAD
    ```

*   **Diff for a specific file:**
    Shows changes only for a specific file history.
    ```bash
    git log -p <HASH>^..HEAD -- <file_path>
    ```

*   **Stat summary (files changed, insertions, deletions):**
    Useful for a high-level overview without reading code.
    ```bash
    git log --stat <HASH>^..HEAD
    ```

### 7.3 Searching History

*   **By Author:**
    ```bash
    git log --author="Name"
    ```

*   **By Date:**
    ```bash
    git log --since="2025-11-01" --until="2025-11-30"
    ```

*   **By Message Content (Grep):**
    Find commits that mention a specific keyword (e.g., "bug", "auction").
    ```bash
    git log --grep="auction"
    ```

*   **By Code Content (Pickaxe):**
    Find commits that added or removed a specific string in the code (e.g., a variable name).
    ```bash
    git log -S "variable_name"
    ```

### 7.4 Formatting

Use `--pretty=format:"..."` to customize the output for changelogs.
*   `%h`: Short hash
*   `%s`: Subject
*   `%b`: Body
*   `%an`: Author name
*   `%ad`: Author date (use `--date=short` for YYYY-MM-DD)

**Example for Changelog Generation:**
```bash
git log <LAST_RELEASE_HASH>..HEAD --pretty=format:"- %s"
```