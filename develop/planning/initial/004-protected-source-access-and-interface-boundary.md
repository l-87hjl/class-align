# Protected Source Access and Interface Boundary

## Clarification

Full-text source material should not be publicly accessible through the user interface.

The system may still need to make that material available to the processing agent so the agent can answer questions, analyze assignments, generate rubrics, assess alignment, and apply the teacher clarity or visual learning procedures.

This creates an important boundary:

- The interface may be reachable through the web
- The source texts must remain protected from public access
- The processing agent must be able to read the texts when authorized
- Generated outputs may be handled differently from the source texts

A publicly reachable website does not require the uploaded full texts themselves to be public.

## Desired experience

The teacher should be able to use the system from a professional account without repeatedly copying files between machines, chats, or tools.

An ideal workflow would allow the teacher to:

1. Access an interface from the professional environment
2. Upload or select the relevant assignment and source files
3. Authorize processing for a particular task or batch
4. Allow the agent to use the protected source material during processing
5. Receive and review the resulting alignment, rubric, clarity, or visual-learning artifacts
6. Avoid exposing the original full text through public links or repository paths

## Possible boundary models

The final implementation method remains open, but several broad models could satisfy this requirement.

### Web interface with protected backend storage

The interface could be internet-accessible while uploaded full texts are stored behind authentication or otherwise inaccessible to the public.

The processing service would receive authorized access to the files without publishing them.

### Web interface with temporary processing

Source files could be uploaded for a particular job, made available to the agent only during processing, and deleted after a defined retention period.

This could reduce the need to maintain a permanent library of full texts.

### Web interface backed by the Mac Mini

A browser-accessible interface could submit work to a service running on the Mac Mini, allowing the local machine to hold or process protected source material.

This may reduce cloud storage of full texts, though it could introduce networking, availability, authentication, and maintenance concerns.

### Fully local Mac Mini workflow

The Mac Mini could remain the complete working environment for source files and agent processing.

This offers a clearer local-control boundary but risks preserving the current friction of manually moving files between the professional environment and the local machine unless a better transfer or remote-access mechanism is added.

## Design principle

The project should separate these concerns rather than treating them as the same decision:

- Whether the interface is reachable from the web
- Whether a user must authenticate
- Where source files are stored
- How long source files are retained
- Which processing agent can access them
- Whether generated outputs are safe to expose or share
- Whether the repository stores source texts, references to them, or only derived metadata

## Current preference

The preferred outcome is to preserve browser-based professional access while preventing public access to full texts.

The Mac Mini remains a viable processing or hosting component, especially if it can reduce exposure of source material without forcing repetitive copying and pasting.

The website option should not be rejected merely because full texts must remain private. The deciding question is whether the eventual system can enforce a protected path from upload or storage to authorized agent processing.

## Open questions

- Will the interface require individual authentication?
- Can the professional account access external authenticated services?
- Should full texts be stored permanently, temporarily, or only on the Mac Mini?
- Should the repository contain only metadata and derived artifacts rather than the full texts?
- How should the agent receive authorized access to protected files?
- What retention and deletion controls are needed?
- Which outputs may be shared publicly, and which should remain private?
- Would remote access to the Mac Mini remove enough file-transfer friction to make a local-first design practical?
