# BApp Store Acceptance Criteria

**CRITICAL**: To submit your extension to the BApp Store, your extension MUST meet ALL of the following criteria:

## 1. Unique Function
- Extension must perform a unique function
- Should not duplicate existing BApp Store extensions
- Consider modifying existing extensions if idea isn't entirely new

## 2. Clear Name
- Name must clearly describe extension's purpose
- Provide a one-line summary and detailed description

## 3. Security
- Treat HTTP message content as untrusted
- Operate securely during expected usage
- Be cautious with auto-filled data from untrusted sources

## 4. Dependencies
- Include all dependencies for one-click installation
- Avoid version mismatches with underlying tools

## 5. Threading
- Perform slow operations in background threads
- Avoid blocking Swing Event Dispatch Thread
- Protect shared data structures with locks
- Catch and report background thread exceptions

## 6. Clean Unloading
- Release all resources when unloading
- Register unload handler
- Terminate background threads during unloading

## 7. Burp Networking
- Use `Http.issueHttpRequest()` for HTTP requests
- Respect upstream proxy and session handling settings
- Avoid target communication in `ScanCheck.passiveAudit()`

## 8. Offline Support
- Include recent definitions for online services
- Support high-security networks without internet

## 9. Large Project Handling
- Avoid long-term references to transient objects
- Use `Persistence.temporaryFileContext()` for message references
- Be cautious with large result sets

## 10. GUI Parenting
- Create GUI elements as children of main Burp Frame
- Use `SwingUtils.suiteFrame()` to get parent frame

## 11. Montoya API
- Reference `montoya-api` artifact using build tools
- Recommended to use Gradle for new projects

## 12. AI Functionality
- Use dedicated Montoya API methods for AI features
- Follow AI extension best practices
- Handle AI-related traffic through Burp's AI platform