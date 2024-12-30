# Incorrect useEffect Dependency Array in React

This example demonstrates a common error in React's `useEffect` hook: an incorrect dependency array. The `useEffect` hook is used to perform side effects after rendering, such as data fetching, setting timers, or manipulating the DOM. It takes two arguments: a function that contains the side effect, and an array of dependencies. The side effect function is executed only after the component renders, and only if the values in the dependency array have changed.

In this case, the `useEffect` hook is used to set up a timer that increments a counter every second. However, the dependency array is empty (`[]`), which means that the side effect will only run once, after the initial render.  Subsequently, the timer will continue to run, but the `setCount` function will not be called, resulting in the counter not updating.

The solution is to include `count` in the dependency array, so that the effect runs every time the `count` changes.