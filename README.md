# AI Mind Map Generator (Force Layout)

This is a web application that allows you to create mind maps using a force-directed graph layout powered by D3.js. You can add nodes, connect them, edit their content, and export the mind map as a JSON file, a collection of notes in markdown, or an SVG image. The application also uses AI (via a Google Gemini API key which must be entered in the javascript) to generate topic suggestions and notes for the mind map.

## Features

*   **Interactive Force Layout:** Nodes are arranged using a physics simulation, preventing overlaps and creating a dynamic and visually appealing mind map.
*   **AI-Powered Generation:** Generate subtopics and notes for your mind map using AI.
*   **Node Editing:** Edit node titles, notes (with Markdown support), and colors.
*   **Multi-Node Editing:** Simultaneously change the colors of multiple selected nodes.
*   **Import/Export:** Save and load your mind maps as JSON files or export selected chain of notes as a markdown document.
*   **SVG Export:** Export the mind map as a scalable vector graphic (SVG) image.
*   **Drag and Drop:** Easily reposition nodes and connect them by dragging one node onto another.
*   **Keyboard Shortcuts:** Use keyboard shortcuts for common actions, improving efficiency.
*   **Zoom and Pan:** Use your mouse wheel or trackpad to zoom in and out, and click and drag the background to pan the view.
*   **Accessibility:** The application is designed with accessibility in mind, including keyboard navigation and ARIA attributes.
*   **Persistence:** Your mind maps are automatically saved to and loaded from your browser's IndexedDB storage.
*   **Toggleable Physics:** Toggle the physics simulation on and off for manual arrangement.
*   **Customizable Force Parameters:** Adjust the repulsion, link distance, and collision forces in the physics simulation to suit your needs.
*   **Multi-Select Mode:** Select multiple nodes for simultaneous editing or deletion.
*   **Child Layouts:** Arrange children of a selected node in various layouts (vertical, horizontal, arc, circle).

## Technologies Used

*   **HTML:** For the structure of the web page.
*   **CSS (Tailwind CSS):** For styling the application.
*   **JavaScript:** For the application logic and D3.js integration.
*   **D3.js:** A JavaScript library for manipulating documents based on data. Used for creating the force-directed graph.
*   **IndexedDB:** For storing mind map data in the browser.
*   **Marked.js:** A markdown parser and compiler. Used for rendering node notes.
*   **Google Gemini API:** Used to generate topics, summaries, and notes (requires a user-provided API key to be entered in the javascript).

## Getting Started

1.  Open the `index.html` file in your web browser.
2.  Enter a central topic in the prompt box that appears and click "Generate" to start your mind map.
3.  Alternatively, you can click "import a mind map" to load an existing mind map from a JSON file.

## Usage

*   **Adding Nodes:**
    *   Select a node and click the "+" button to add a child node manually.
    *   Select a node and shift-click the "+" button, or click the "Generate" button to create new sub-topics with AI.
    *   Click the "New Root" button to add a new, independent mind map tree.

*   **Editing Nodes:**
    *   Select a single node and press the "E" key or click the "Edit" button to edit its title, notes, and colors.
    *   Select multiple nodes and press "E" or click the "Edit" button to change their colors simultaneously.

*   **Deleting Nodes:**
    *   Select one or more nodes and press the "Delete" or "Backspace" key, or click the "Delete" button to delete them.

*   **Connecting Nodes:**
    *   Click and drag one node on top of another to make it a child of that node.

*   **Severing Links:**
    *   Hover over a link and click the red minus button to make a node independent.

*   **Moving Nodes:**
    *   Click and drag any node to reposition it.

*   **Zooming and Panning:**
    *   Use your mouse wheel or trackpad to zoom.
    *   Click and drag the background to pan the view.

*   **Toggle Physics:**
    *   Click the **Force** button to toggle the physics simulation on and off.

*   **Customize Force Parameters:**
    *   **Long-press** the Force button to open a modal where you can adjust the sensitivity of the repulsion, link distance, and collision forces.

*   **Using Child Layouts:**
    *   Select a single node, then select a child layout option above to arrange the child nodes automatically.

*   **Multi-Select Mode:**
    *   **Long-press** (click and hold for 500ms) on any node to toggle **Multi-Select Mode**.
    *   In Multi-Select Mode, simply click nodes to add or remove them from the selection.
    *   Press <kbd>Esc</kbd> to deselect all nodes and exit Multi-Select Mode.

## Keyboard Shortcuts

*   `Shift + N`: Start a new mind map.
*   `Shift + E`: Export the mind map as JSON.
*   `Shift + I`: Import a mind map from a JSON file.
*   `Delete` or `Backspace` or `D`: Delete selected node(s).
*   `E`: Edit selected node (single) or colors (multiple).
*   `Escape`: Deselect all nodes and exit Multi-Select Mode.
*   `Enter` when focused on a node: Add new child node to selected node (or generate child with shift).
*   `Spacebar` when focused on a node:  Add the focused node to selection.

## Known Issues

*   AI generation relies on a third-party API (Google Gemini) and requires a valid API key to be entered into the javascript.  AI generation may fail if the API key is invalid or if the API is unavailable.
*   Performance may degrade with very large mind maps.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues to report bugs or suggest new features.
