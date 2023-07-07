# _Index.js Explanation_

This JavaScript code creates a simple coin flip game. Here's an explanation of each part:

1.  The variables `heads` and `tails` are initialized to keep track of the number of times the coin has landed on heads and tails, respectively.
2.  The variables `coin`, `flipBtn`, and `resetBtn` are used to select elements from the HTML document using their corresponding CSS selectors.
3.  The `flipBtn` button has an event listener attached to it. When clicked, it triggers the following actions:
    -   Generates a random number (`i`) between 0 and 1 using `Math.random()`.
    -   Sets the `animation` property of the `coin` element to "none" to reset any previous animations.
    -   If `i` is truthy (evaluates to `true`), it means heads is chosen:
        -   After a delay of 100 milliseconds, sets the `animation` property of the `coin` element to "spin-heads 3s forwards". This starts the animation where the coin spins and lands on heads.
        -   Increments the `heads` count.
    -   If `i` is falsy (evaluates to `false`), it means tails is chosen:
        -   After a delay of 100 milliseconds, sets the `animation` property of the `coin` element to "spin-tails 3s forwards". This starts the animation where the coin spins and lands on tails.
        -   Increments the `tails` count.
    -   Calls the `updateStats()` function after a delay of 3000 milliseconds to update the displayed count of heads and tails.
    -   Calls the `disableButton()` function to disable the flip button for 3 seconds.
4.  The `updateStats()` function updates the text content of the elements with IDs "heads-count" and "tails-count" to reflect the current counts of heads and tails.
5.  The `disableButton()` function disables the flip button by setting its `disabled` property to `true`. After a delay of 3000 milliseconds, it enables the button again by setting the `disabled` property to `false`.
6.  The `resetBtn` button has an event listener attached to it. When clicked, it resets the game by performing the following actions:
    -   Sets the `animation` property of the `coin` element to "none" to reset any animations.
    -   Resets the `heads` and `tails` counts to 0.
    -   Calls the `updateStats()` function to update the displayed counts of heads and tails.

Overall, this code allows the user to flip a virtual coin by clicking a button, keeps track of the number of heads and tails, and provides a reset button to start the game again.