# Copilot Instructions

## General Guidelines
- User's active document may differ from what assistant assumed; prefer calling `get_currentfile` to confirm the active document before acting.
- All code is X++; Microsoft Dynamics AX 2012 R3. When generating or editing code, follow coding standards present in the existing codebase and confirm the active document with `get_currentfile` before acting. Store these as user-level preferences (remembered for future sessions).
- Remember to apply the development-guidelines PDF rules when generating or editing X++ code for Microsoft Dynamics AX 2012 R3. User will provide the PDF file or paste its key sections; confirm before applying rules to the active document. Store key sections provided by the user as user-level memory.
- Always use the user's copilotinstructions.md file (user preference) for guidance when provided and apply it to future responses.
- Do not generate code with metadata markers like '#' from .xpo files; provide clean X++ only.
- Use Microsoft Learn archives for AX 2012 R3 if possible for standard code which is not customized, such as for standard processes etc.
- When generating code, usually do not generate full function code; generate only the changed parts along with mentioning where to change it.
- When fetching files, prefer the full file contents by default unless a partial range is explicitly requested by the user.

## Code Style
- Use specific formatting rules.
- Follow naming conventions, including WDH naming conventions and AOT object rules.
- Ensure adherence to X++ coding standards for Microsoft Dynamics AX 2012 R3.
- Method names should start with a lower-case letter, use `_param` style, camelCase, and tabs for indentation.
- Label file should be <COMPANY PREFIX> (EN-US).
- Always use all variable declarations at top and not inline in code below.
- Prefer `throw` over `ttsAbort` and avoid display methods.
- Use localization via CountryRegionCodes and <COMPANY PREFIX>BusinessContext.

## Project-Specific Rules
- Utilize X++ best practices and conventions specific to Microsoft Dynamics AX 2012 R3.
- Follow the services namespace and data contract rules.
- Adhere to the QA/code review checklist.
- Use TFS workflow.
- Remember the WDH datajob formatting/guidelines for future datajobs (not core logic) in X++ for AX 2012 R3.
