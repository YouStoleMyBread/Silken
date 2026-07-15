# Silken

> A modern visual IDE for interactive fiction and large branching stories.

Silken is a private, early-stage project focused on making large Twine-style stories easier to create, organize, edit, test, import, and export.

The project is currently in the **concept and foundation phase**. The interface is interactive and several core systems already work, but Silken is not yet ready for production use.

Silken is being designed as a spiritual successor to Twine's visual editor, with a stronger focus on scalability, organization, built-in code editing, and large projects containing thousands of passages.

---

## Project Status

**Current phase:** Concept / functional foundation

The original UI mockup has grown into a working application foundation. Some systems are already functional, while many buttons, menus, dialogs, and backend features are still placeholders or incomplete.

A real SugarCube story containing roughly **2,000 passages** has been imported successfully with:

- Passage names
- Passage content
- Tags
- Node positions generated in the workspace
- Story connections
- Smooth canvas performance
- No noticeable lag during testing

This is encouraging, but performance testing is still ongoing and should not yet be treated as a final benchmark.

---

## Current Features

### Story Format Support

- SugarCube support
- Harlowe support
- Twee support
- Ability to switch between supported formats
- SugarCube project import tested with a large real-world story
- Passage and tag data preserved during import

### Visual Story Workspace

- Large node-based story canvas
- Passage nodes
- Live connection lines between passages
- Zoom and canvas navigation
- Passage selection
- Node movement
- Large-story rendering tested with approximately 2,000 passages
- Blueprint-style visual grid

Traditional directional arrows were replaced with simpler connection lines for clarity, reliability, and performance.

### Organization

- Full-color passage nodes
- Custom color selection
- Passage tags
- Tag colors
- Folder UI foundation
- Panel UI foundation
- Explorer sidebar
- Passage list
- Connection tree
- Search interface

Folders are intended to become collapsible, resizable containers that automatically arrange passages placed inside them.

Panels are intended to provide non-collapsible visual grouping without forcing passages into a structured layout.

### Passage Editing

- Monaco Editor integration
- Passage editing
- Story JavaScript editing
- Story stylesheet editing
- Editor switching between passage content, JavaScript, and stylesheet
- Floating passage editor window design
- Foundation for opening multiple passage editors at once

### Application Interface

- Story library interface
- Story workspace interface
- Menus and toolbars
- Build controls
- Story controls
- View controls
- Preferences interface
- About Silken interface
- Dark theme foundation
- Custom Silken branding and application icon

---

## Planned Core Systems

The following systems are considered part of Silken's core implementation rather than optional future extras.

### Project and File Management

- Create, open, rename, duplicate, and delete stories
- Save and load Silken project files
- Autosave
- Crash recovery
- Backup files
- Story library indexing
- Story-level tags
- Story sorting and filtering
- Custom story library folder
- IFID generation and preservation

### Import and Export

- Import published Twine HTML stories
- Preserve existing IFIDs when present
- Generate IFIDs when missing
- Export playable HTML
- Export Twee
- Import Twee
- Preserve story format and version
- Support full project round-tripping without losing story data

### Story Building and Testing

- Test story
- Play story
- Test from selected passage
- Start story from selected passage
- Proofing output
- Publish to file
- Runtime error reporting
- Temporary preview builds

### Passage and Graph Systems

- Create, rename, duplicate, delete, copy, cut, and paste passages
- Multi-selection
- Select all and deselect all
- Set start passage
- Automatic graph updates when passage links change
- Incoming and outgoing connection indexing
- Broken-link detection
- Unreachable-passage detection
- Selected-node connection filtering
- Toggle all connection lines on or off
- Show only connections related to the selected passage

### Folders and Panels

- Resizable folders
- Resizable panels
- Collapsible folders
- Dynamic folder layout
- Passage snapping inside folders
- Responsive rows and columns
- Internal folder scrolling
- Folder colors
- Panel colors
- External connection visibility
- Collapsed-folder connection summaries

### Search and Navigation

- Passage search
- Passage-content search
- Tag search
- Tag filtering
- Folder search
- Explorer navigation
- Recursive connection tree
- Click-to-focus passage
- Find and replace
- Search results that can filter and highlight nodes

### Diagnose

A floating diagnostic window is planned with clickable, live-updating results for:

- Broken links
- Passages with no incoming links
- Passages with no outgoing links
- Unreachable passages
- Duplicate passage names
- Unused tags
- Missing start passage
- Average words per passage
- Other story statistics and structural warnings

Selecting a diagnostic result should filter or highlight the related passages directly on the canvas.

### Preferences

- Light, dark, and system themes
- Passage editor font
- Passage editor font size
- Writing aid toggle
- Hardware acceleration toggle
- Language selection
- Grid options
- Connection-line display options
- Autosave settings

### Writing Aid

- Optional local proofreading
- Monaco diagnostics integration
- Suggestions and corrections
- Personal dictionary
- Per-story disable option
- Privacy-focused design

---

## Known Bugs and Limitations

- Connection lines may still require further refinement in dense stories
- Large graphs can become visually overwhelming when all connections are visible
- Folder behavior is not fully implemented
- Panel behavior is not fully implemented
- Many toolbar and menu actions are placeholders
- Story library actions are incomplete
- Floating editor window behavior is incomplete
- Multiple passage editor windows are not fully implemented
- Diagnose is not yet implemented
- Preferences are not fully functional
- Story building and runtime testing are incomplete
- Import and export need broader compatibility testing
- Save, autosave, recovery, and migration systems are incomplete
- Performance has not yet been tested across a wide range of hardware
- Large-story performance has been tested informally, not through repeatable benchmarks
- Harlowe, SugarCube, and Twee support still need broader edge-case testing
- The application is not ready for creating and shipping complete games yet

---

## IFID Rules

Silken should follow these rules:

- A new story receives an IFID when it is created
- Renaming a story preserves its IFID
- Moving or saving a story preserves its IFID
- Duplicating a story generates a new IFID
- Importing a story preserves its existing IFID when present
- Importing a story without an IFID generates one
- Exporting a story preserves its IFID

---

## Performance Goals

Silken is being designed around very large stories.

Target test sizes include:

- 1,000 passages
- 5,000 passages
- 10,000 passages
- 20,000 passages as a stress test

Performance work will focus on:

- Rendering only visible nodes
- Lazy loading and viewport virtualization
- Efficient connection rendering
- Fast search indexing
- Incremental parsing
- Efficient save and load operations
- Avoiding unnecessary DOM updates
- Keeping the full graph in lightweight application data rather than relying on rendered elements

---

## Development Priorities

The current priority is to complete a full vertical workflow:

1. Create or import a story
2. Edit passages
3. Parse passage links
4. Display and update connections
5. Save the project
6. Reopen the project without data loss
7. Build playable output
8. Test the story
9. Export the story
10. Import the exported result successfully

Once that workflow is stable, development can move toward folders, panels, diagnostics, proofreading, deeper editor tooling, and performance refinement.

---

## Definition of Finished

For Silken, **finished does not mean perfect**.

The project will be considered ready for its first complete release when:

- All core features work as intended
- Games can be created
- Games can be played
- Stories can be imported
- Stories can be exported
- The complete workflow is usable
- Known bugs may still exist
- Optional quality-of-life features may still be unfinished
- Future versions can continue improving stability, polish, and functionality

---

## Open-Source Plan

Silken is currently being developed privately.

The project is intended to become open source once it reaches a complete, usable state where the core workflow functions end to end.

The planned license is:

**GNU General Public License, version 3.0**

> Silken is free and open-source software released under the GNU General Public License, version 3.0. Stories and other works created with Silken are not covered by Silken's license and may be released under any terms, including commercial terms.

---

## Creator

Created by **YouStoleMyBread**

Silken is currently an independent project in active development.

---

## Disclaimer

Silken is not affiliated with or endorsed by Twine, the Interactive Fiction Technology Foundation, SugarCube, Harlowe, or their respective maintainers.

Silken is an independent project inspired by visual interactive-fiction tools and modern software-development environments.
