# MCET Schedule Builder

A browser-based course schedule builder for creating editable semester schedules. Open `index.html` in a modern browser. No installation is required.

## Main features

- Edit the course title, dates, column headings, and card text directly on the page.
- Drag schedule cards between dates, weeks, and columns.
- Add or remove columns.
- Choose date-by-date columns or whole-week columns, such as Recitation.
- Add or remove rows within a week for courses that meet one, two, three, or more times per week.
- Auto-fill dates from a start date, end date, and selected meeting days.
- Import an existing schedule from CSV or pasted Excel cells.
- Download and reload backup files.
- Print or save a compact student-facing PDF.

## Quick start

1. Open `index.html` in Chrome, Edge, Firefox, or another modern browser.
2. Click the title at the top to rename the schedule for your course.
3. Click column headers to rename them.
4. Click inside cards to edit wording.
5. Drag cards to move items around.
6. Use **Download backup** to save your work.

## Starting fresh

Click **Reset everything** to clear the schedule and return to a blank reusable template. This is helpful before sharing the tool with another instructor or starting a new course.

## Auto-fill dates

1. Click **Auto-fill dates**.
2. Enter the semester start and end dates.
3. Select the days of the week the class meets.
4. Choose a date display format.
5. Click **Create date rows**.

You can still manually edit, add, or remove dates after auto-fill.

## Rows within each week

- Click **+ row** inside a week to add one more class meeting to that week.
- Click **+ Row to every week** to add another meeting row across the whole semester.
- Click **- row** to remove a meeting row.

If a removed row has cards, those cards are moved to another row in the same week so they are not lost.

## Columns

Use the column controls at the top of the page to add or remove columns.

Column types:

- **date-by-date column**: separate cells for each class meeting.
- **whole-week column**: one cell that spans the whole week, useful for recitations, labs, or weekly reminders.

To rename a column, click directly on the column title in the header row.

## Importing from Excel or CSV

The importer works with a CSV file or with cells copied directly from Excel.

Common headers include:

- Week
- Date or Dates
- Topic
- Homework Due
- myCourses Quiz Due
- Project
- Bonus Due
- Recitation

Two CSV files are included in this repository:

- `course_schedule_import_blank_template.csv` is a blank 15-week template with three class meeting rows per week.
- `course_schedule_import_example.csv` shows example entries, including multiple lines inside one cell.

To import a CSV file, save your Excel file as CSV UTF-8, then click **Import CSV / Excel paste** and choose the file.

To paste from Excel, copy the schedule range including headers, click **Import CSV / Excel paste**, paste into the text box, and click **Import pasted table**.

### CSV import template notes

Required structure:

- The first row must contain column headers.
- Use `Week` for the week number.
- Use `Dates` or `Date` for the class meeting date or label.
- Other headers become schedule columns.

Recommended headers:

```text
Week, Dates, Topic, Homework Due, myCourses Quiz Due, Project, Bonus Due, Recitation
```

Tips:

- Put the week number only on the first row of each week; blank cells below it will be filled down during import.
- Put Recitation information only once per week. The Schedule Builder treats a column with `Recitation` in the title as a whole-week column.
- Multiple lines inside one Excel cell become separate draggable cards after import.
- To import: save the completed Excel file as CSV UTF-8, then use **Import CSV / Excel paste** in the Schedule Builder.

Blank week cells are filled down automatically. Multiple lines inside one Excel cell become separate draggable cards.

## Saving and loading work

The tool auto-saves in the browser, but the safest method is to use **Download backup**. This creates a backup file that can be loaded later with **Load backup**.

Use backups to move a schedule between computers or to share a course schedule with another person.

## Printing or saving as PDF

1. Open the schedule in the browser.
2. Choose Print.
3. Select Save as PDF.
4. Use Landscape orientation.
5. Turn on Background graphics so the colors appear.
6. Adjust browser scale if needed.

The editing view stays spacious, while the print view is more compact for student handouts.

## Sharing with coworkers

Share the repository link or the `index.html` file. Coworkers can open it in a browser, click **Reset everything**, and build or import their own course schedule.
