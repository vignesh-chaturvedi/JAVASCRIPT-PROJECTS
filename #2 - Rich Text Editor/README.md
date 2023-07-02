# Script.js Explanation
Let's break it down into sections:

1.  Variable Declarations:

    -   `optionsButtons`: Stores a collection of elements with the class name "option-button".
    -   `advancedOptionButton`: Stores a collection of elements with the class name "adv-option-button".
    -   `fontName`: Represents an element with the ID "fontName".
    -   `fontSizeRef`: Represents an element with the ID "fontSize".
    -   `writingArea`: Represents an element with the ID "text-input".
    -   `linkButton`: Represents an element with the ID "createLink".
    -   `alignButtons`: Stores a collection of elements with the class name "align".
    -   `spacingButtons`: Stores a collection of elements with the class name "spacing".
    -   `formatButtons`: Stores a collection of elements with the class name "format".
    -   `scriptButtons`: Stores a collection of elements with the class name "script".
    -   `fontList`: An array that contains a list of font names.
2.  `intializer` function:

    -   This function is called when the window loads.
    -   It sets initial configurations by calling the `highlighter` function for different button groups.
    -   It populates the font select dropdown (`fontName`) and the font size select dropdown (`fontSizeRef`) with options.
3.  `modifyText` function:

    -   This function is responsible for modifying the text in the editor area based on the given command, default UI, and value.
    -   It uses the `document.execCommand` method to perform the text modification.
4.  Event Listeners:

    -   The code attaches event listeners to the `optionsButtons` and `advancedOptionButton` elements, listening for a click or change event, respectively. When triggered, they call the `modifyText` function with the corresponding button ID and value.
    -   The `linkButton` element has a click event listener. When clicked, it prompts the user to enter a URL and then modifies the text by adding a link using the `modifyText` function.
    -   The `alignButtons`, `spacingButtons`, `formatButtons`, and `scriptButtons` elements have event listeners attached through the `highlighter` function. These listeners toggle the "active" class on button elements.
5.  Helper Functions:

    -   `highlighter` function: Adds event listeners to elements within the provided class name collection. It adds or removes the "active" class based on the `needsRemoval` parameter.
    -   `highlighterRemover` function: Removes the "active" class from all elements within the provided class name collection.
6.  Initialization:

    -   The `window.onload` event is set to call the `intializer` function when the window finishes loading.

Overall, this code sets up event listeners for various buttons and handles the modification of text within the editor area based on the user's actions.