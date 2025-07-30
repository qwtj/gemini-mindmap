# AI Mind Map Generator (Force Layout)

This web application is an interactive mind map generator that leverages D3.js for visualization and can optionally utilize AI to suggest new topics and generate notes. It supports keyboard navigation, drag-and-drop node manipulation, and various export options.

## Features

*   **Interactive Mind Maps:** Create and manipulate mind maps with a force-directed layout.
*   **AI Integration:** Generate new child nodes and synthesize notes using an AI agent.
*   **Drag and Drop:** Organize nodes by dragging them to new parent nodes.
*   **Keyboard Navigation:** Navigate and manipulate the mind map using keyboard shortcuts for accessibility.
*   **Import/Export:** Import mind maps from JSON or Markdown files and export them in JSON, SVG, or Markdown formats.
*   **Customization:** Edit node titles, notes, colors, and text colors.
*   **Multiple Selection:** Edit the colors of several nodes simultaneously.
*   **Accessibility:** Designed with accessibility in mind, including keyboard navigation and ARIA attributes.
*   **Responsive Design:** Adapts to different screen sizes.
*   **Physics Control:** Turn the physics simulation on and off.
*   **Child Layout:** Arrange the children of a node in different layout styles: vertical, horizontal, arc, and circle.

## Technologies Used

*   **D3.js:** Data visualization library for creating interactive graphics.
*   **Tailwind CSS:** Utility-first CSS framework for styling the application.
*   **IndexedDB:** In-browser database for storing mind map data.
*   **JavaScript:** Core programming language for the application's logic.
*   **marked.js:** Markdown parser and compiler.

## Setup/Installation

To run this web application locally, you can simply open the `index.html` file in your web browser. No additional setup is required, as it is a client-side application with no server-side dependencies.

1.  Download or clone the repository containing the `index.html` file.
2.  Open `index.html` in your preferred web browser.

## Usage

### Creating a Mind Map

1.  **Initial Prompt:** Enter a central topic in the initial prompt dialog to start generating ideas.
2.  **Adding Nodes:**
    *   Click the **Add** button (+ icon) to manually add child nodes to a selected node.
    *   Click the **Generate** button (sparkles icon) to generate new sub-topics with AI.
    *   Click the **Add Root** button (document icon) to add a new root to the map.
3.  **Editing Nodes:**
    *   Select a single node and click the **Edit** button (pencil icon) to edit its content (title, notes, colors).
    *   Select multiple nodes and click the **Edit** button to change their colors simultaneously.
4.  **Drag and Drop:** Click and drag nodes to move them around and reorganize the mind map.
5.  **Deleting Nodes:** Select one or more nodes and click the **Delete** button (trash icon) to remove them.

### Keyboard Shortcuts

*   **`C`:** Open the command prompt.
*   **`Shift + N`:** Start a new mind map.
*   **`Shift + E`:** Export the mind map as JSON.
*   **`Shift + I`:** Import a mind map from a JSON or Markdown file.
*   **`U`:** Un-fix the currently selected node.
*   **`Delete` / `Backspace` / `D`:** Delete selected node(s).
*   **`E`:** Edit the currently selected node(s).
*   **`Escape`:** Deselect all nodes.

### UI Buttons

*   **Edit (Pencil Icon):** Edit selected node(s).
*   **Export (Arrow Icon):** Open export options (JSON, Notes, SVG, Markdown).
*   **Force (Physics Icon):** Toggle physics layout. Double-click to adjust repulsion, link distance, and collision forces.
*   **Delete (Trash Icon):** Delete selected node(s).
*   **Add Menu (Plus Icon):** Open add node menu (+: manual entry, Sparkles: Generate with AI, Document: add new root)
*   **Help (Question Mark Icon):** Open the help and instructions modal.

### Agent Command Prompt

Press the <kbd>C</kbd> key to open a command prompt. You can type commands using natural language to interact with the mind map. Some example commands include:

*   `create a new root node for [topic]`
*   `generate [number] ideas to [topic]`
*   `delete the node '[node name]'`
*   `arrange the children of '[node name]' in a circle`
*   `export the map as svg`
*   `export the map as markdown`
*   `export the map as json`

### Notes on AI Integration

1.  The quality of the AI-generated content is directly related to the input prompt.
2.  AI Integration requires an API key (if used externally from the Gemini App Sandbox). Please follow instructions in the code comments for usage.
3.  AI features are optional and the application functions fully without them.

## Known Issues

*   The performance of the force layout may degrade with a very large number of nodes.
*   AI-generated content may sometimes be inaccurate or nonsensical.

## Contributing

Contributions are welcome! Feel free to submit pull requests or open issues to suggest improvements or report bugs.

## License

This project is open source and available under the [MIT License](LICENSE).
