# Text Expander

Text Expander is a React component that allows you to create expandable and collapsible text sections. It's useful for displaying long blocks of text that can be condensed to a specific number of words and expanded when needed.

## Installation

To use the Text Expander component in your React project, follow these steps:

1. Install the required dependencies by running the following command:

   ```shell
   npm install react
   ```

2. Create a new file called `TextExpander.js` and copy the code for the `TextExpander` component into it.

3. Import the `TextExpander` component in your React component where you want to use it:

   ```javascript
   import TextExpander from "./TextExpander";
   ```

4. You can now use the `TextExpander` component in your JSX code. Here's an example of how to use it:

   ```javascript
   function App() {
     return (
       <div>
         <TextExpander>{/* Your text content goes here */}</TextExpander>
       </div>
     );
   }
   ```

## Usage

The `TextExpander` component accepts several props that allow you to customize its behavior and appearance. Here are the available props:

- `children`: The text content to be displayed within the `TextExpander` component.

- `collapsedNumWords` (optional): The number of words to display when the text is collapsed. Defaults to 10.

- `expandButtonText` (optional): The text to display on the expand button. Defaults to "Show more".

- `collapseButtonText` (optional): The text to display on the collapse button. Defaults to "Show less".

- `buttonColor` (optional): The color of the expand/collapse button. Defaults to "blue".

- `expanded` (optional): Whether the text should be initially expanded or collapsed. Defaults to `false`.

- `className` (optional): Additional CSS class name(s) to apply to the `TextExpander` component.

To use these props, pass them to the `TextExpander` component as shown in the example below:

```javascript
<TextExpander
  collapsedNumWords={20}
  expandButtonText="Show text"
  collapseButtonText="Collapse text"
  buttonColor="#ff6622"
>
  {/* Your text content goes here */}
</TextExpander>
```

When the component is rendered, it will display the text content collapsed to the specified number of words. Clicking the expand button will reveal the full text, and clicking the collapse button will hide the excess text again.

## Example

Here's an example of how to use the `TextExpander` component:

```javascript
import { useState } from "react";
import "./index.css";
import TextExpander from "./TextExpander";

export default function App() {
  return (
    <div>
      <TextExpander>{/* Your text content goes here */}</TextExpander>

      <TextExpander
        collapsedNumWords={20}
        expandButtonText="Show text"
        collapseButtonText="Collapse text"
        buttonColor="#ff6622"
      >
        {/* Your text content goes here */}
      </TextExpander>

      <TextExpander expanded={true} className="box">
        {/* Your text content goes here */}
      </TextExpander>
    </div>
  );
}
```

In this example, three `TextExpander` components are used to display different blocks of text with different configurations.

Feel free to customize the component's props and the text content to fit your specific needs.

That's it! You can now use the `TextExpander` component in your React project to create expandable and collapsible text sections.
