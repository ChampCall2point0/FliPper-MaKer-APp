# Flipper Maker - GitHub Copilot Instructions

## Project Overview

Flipper Maker is a web-based application that allows users to generate files for the Flipper Zero device. The generated files can be instantly installed from a mobile phone or downloaded for manual installation via qFlipper.

## Technology Stack

- **Frontend**: Vanilla JavaScript (ES5/ES6), HTML5, CSS3
- **UI Framework**: Bootstrap 5.1.3
- **Additional Libraries**: jQuery 3.6.0, Masonry Layout 4.2.2, Luxon (for date/time)
- **Hosting**: GitHub Pages (static site)
- **No Build System**: Direct browser execution, no transpilation or bundling

## Code Style and Conventions

- Use vanilla JavaScript - avoid introducing new frameworks or build systems
- Follow existing code patterns in the repository
- Use descriptive variable and function names
- Maintain compatibility with modern browsers (ES6+ features are acceptable)
- Keep code modular with separate files for different functionalities
- Use Bootstrap classes for styling to maintain consistency

## File Organization

- Main application entry point: `index.html`
- Module organization pattern: `general_*.js` for general features, `[protocol]_*.js` for protocol-specific code
- Protocol implementations: SubGHz, IR, NFC, RFID, BadUSB
- Tool files: Separate JavaScript files for specific tools (e.g., `nfc_tool_create.js`, `subghz_tool_OokToSub.js`)

## Flipper Zero File Formats

When working with Flipper Zero file generation:
- SubGHz files use `.sub` extension with specific format requirements
- IR files follow IRDB format conventions
- NFC files use `.nfc` extension
- RFID files use `.rfid` extension
- BadUSB files use `.txt` extension
- All files must include proper headers and formatting as per Flipper Zero specifications

## Key Features to Maintain

- Instant file installation on mobile devices via Flipper Zero app
- Support for multiple protocols: TouchTunes, IR, MegaCode, H10301, FireFly
- Tools: NFC URL Creator, File Sharing, OOK to .sub converter, BadUSB Alt Code converter
- File download functionality that automatically launches the Flipper Zero app on mobile

## Testing and Validation

- Test file generation output format manually
- Verify download functionality works on both mobile and desktop
- Ensure generated files are compatible with Flipper Zero devices
- Test across modern browsers (Chrome, Firefox, Safari, Edge)

## Dependencies

- Minimize new dependencies - prefer vanilla JavaScript solutions
- If adding libraries, use CDN links to maintain the static nature of the site
- Ensure any new dependencies are compatible with the existing Bootstrap/jQuery setup

## Community and Contributions

- Encourage community pull requests
- Maintain clear, helpful comments for complex logic
- Document new features in the README.md
- Credit external resources and libraries appropriately

## Special Considerations

- The application runs entirely client-side - no backend server
- All file generation happens in the browser
- Files must be properly formatted for Flipper Zero compatibility
- Support both mobile and desktop workflows
- Maintain the existing visual design and user experience
