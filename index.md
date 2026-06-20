## General

- Everything should be clean, performant and adhering to modern coding standards.

- UI and UX should be based on modern standards.

- Always ask before removing or changing any major existing functionality that is out of the scope of the current request before working on it.

- After every fix generate a git commit message that can be used by the user(never add claude as the author or co-author). Also, do not commit for me, only generate the message(unless the claude session is running in a remote cloud environment).

- When not having any context and trying to understand a new project, start with the readme and architecture files, if they exist, and then move on to the other files(the readme and architecture files could also be stale, so keep that in mind).

- Always add detailed comments for important sections of the code and follow general good commenting etiquette.

- Ask for clarifications where necessary.
  
## Tech Choices

- Always use the context7 plugin for up-to-date, version-specific documentation and code examples where possible.

- Always use uv for any python or pip related projects.
  
## Architecture

- Understand the architecture of the project using the ARCHITECTURE.md file(if present).

- Create the ARCHITECTURE.md file if not present(update it in case of any architectural change).

- While making the file consider -

	- The "big picture" architecture that requires reading multiple files to understand - major components, service boundaries, data flows, and the "why" behind structural decisions.

	- Critical developer workflows (builds, tests, debugging) especially commands that aren't obvious from file inspection alone.

	- Project-specific conventions and patterns that differ from common practices.

	- Integration points, external dependencies, and cross-component communication patterns.

	- Avoid generic advice ("write tests", "handle errors") - focus on the project's specific approaches.

	- Document only discoverable patterns, not aspirational practices.

	- Reference key files/directories that exemplify important patterns.
  
## Files

- Make sure any changes that would warrant an update to the readme are documented accordingly in the readme file(make a README.md file if it does not exist).

- Generate a CLAUDE.md file if it does not exist(keep it empty initially).

- Append all the prompts to a PROMPT.md file(create if not present).

- Make sure to update the gitignore file if necessary(create one if it does not exist).

- Create/Append a summary of the work that's done after each change, for context, in the format - "memory/YYYY-MM-DD.md".

- When a new claude code session is started, read the last 2 files(date wise) from this memory folder to get a recent context of the work done.

- Any new or updated env vars should be appropriately updated in the .env.example file.

- If the codebase has a LEARNINGS.md file, it contains learnings we have learned while working with this codebase. For example, a particular code pattern that might produce bugs. Read this file and remember the learnings while dealing with this codebase.

- Always add an mit license by default for greenfield projects. Use 'digster' as the right holder name.
  
## Testing

- Always setup tests for a new project.

- Always add tests for new features and run after changes to test integrity.

- For ui related changes of web projects, test the changes using an actual browser instance.

- Make sure to remove any screenshot files after testing's done, if created by the testing lib/mcp(eg. playwright)

- Setup proper logging with appropriate log levels for the project.

- After you finish writing any code, list the edge cases and suggest test cases to cover them.

- When there’s a bug, start by writing a test that reproduces it, then fix it until the test passes.
  
## Remote Sessions

- When creating git branches for remote claude code sessions, give them a name relevant to the task.
