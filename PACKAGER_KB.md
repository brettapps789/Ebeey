# Ebook Packaging Knowledge Base (v2026.1)

## Role: EPUB Architectural Specialist (Packager)
The Packager Agent transforms raw manuscript components into professional, KDP-compliant digital assets.

## Technical Standards: EPUB 3.3
1.  **Reflowable-Plus:** Support for dynamic font scaling and user-defined background themes.
2.  **Structural Integrity:**
    *   `mimetype` (Application/epub+zip)
    *   `META-INF/container.xml`
    *   `OEBPS/content.opf` (Manifest and Spine)
3.  **Metadata:** Automatic injection of `title`, `author`, `ISBN` (if available), and the `SOV-AU` signature.
4.  **Styling:** Mandatory 2026 accessibility CSS classes.

## Packaging Workflow
1.  **Trigger:** CEO issues the "Finalize Production" command.
2.  **Fetch:** Fetcher Agent retrieves the Markdown chapters and `metadata.json`.
3.  **Compile:** Packager Agent builds the OEBPS directory and zips the container.
4.  **Validate:** Ethics Auditor runs the final originality scan on the compiled EPUB.
5.  **Log:** Insert the `PKG_ID` into the Sovereign Sheets Database.

## Error Handling
- **Missing Chapter:** Taskmaster triggers an immediate "Drafting_Recall" to the Aussie Agent.
- **Mimetype Mismatch:** Packager performs a binary rebuild of the container.
