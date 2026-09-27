# EduTask Studio – fixes in this build

## Teacher instructions are authoritative
- Coding task simulation now detects simple teacher instructions such as “take input and print/display it” and generates the matching input/output program instead of substituting an unrelated canned example.
- Student workspaces display the teacher's exact task instructions.
- No automatic correction or grading is performed by the student/AI simulator.

## Word documents
- DOCX uploads are read through a single async file pipeline instead of nesting async work inside FileReader callbacks.
- Word template import uses the actual uploaded `.docx` text.
- The Word student workspace starts empty unless the teacher supplied a template; it no longer inserts unrelated sample Carnatic content.
- Upload submission no longer calls `.replace()` on an undefined filename.

## Blank-screen protection
- Added a React error boundary so an unexpected document/task parsing error shows a recovery screen instead of making the whole classroom appear blank.

## Dependency
- `package.json` uses esbuild `^0.28.2`, compatible with Vite 8.

## Crash fix
- Fixed the Word Document task creation crash by importing `CheckCircle2` in `TaskCreateModal.tsx`, which was referenced by the Word-document configuration panel without being imported.
