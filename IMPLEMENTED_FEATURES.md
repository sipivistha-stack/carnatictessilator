# EduTask Studio – requested changes

## 1. Teacher attendance
- Teacher dashboard retains the Attendance manager.
- Attendance is explicitly marked per student as Present, Absent, Late, or Excused.
- Batch Present/Absent actions remain available.
- The saved attendance session records the exact status and teacher-entered cumulative percentage.
- Students below the existing 75% threshold remain subject to the examination eligibility rule.

## 2. Strict AI/student submissions
- New tasks are marked `strictSubmission: true`.
- AI-generated/student-simulated submissions are never auto-graded or auto-corrected.
- Teacher correction data is only created through the teacher evaluation workflow.
- Seeded demo submissions are reset to `submitted` without pre-existing correction objects when starter data is seeded.

## 3. Level-based Carnatic singing + voice recorder
- Teachers can enable a singing activity while creating a Carnatic task.
- Teachers can enter separate lyrics for Beginner, Intermediate, and Advanced levels.
- The student's level is determined from the profile (`carnaticLevel`) or mapped from the existing performance tier.
- Students see only the lyrics assigned to their level.
- Browser microphone recording and audio upload are supported.
- Teacher can require a recording and set a maximum recording duration.
- The submitted recording is preserved as submitted; no automatic correction/rewrite is applied.

## 4. Word document fix
- Uploaded `.docx` files are now parsed from their actual `word/document.xml` content in the browser.
- The old fake/sample Word pages have been removed.
- Teacher Word-document task creation includes an `Import .docx Template` action that loads the actual document text into the structured template field.
- Invalid/unreadable Word files now show an error instead of silently replacing the file with fabricated sample content.
