# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: missing dependencies in the dependency array.  The provided code shows a counter that is supposed to increment every second. However, due to the missing dependency, the interval is only set once, and the counter does not update correctly.

## Bug Description
The `useEffect` hook's dependency array is empty (`[]`). This means that the effect runs only once after the component mounts. The interval is set, but the counter doesn't update because `count` is not included in the dependency array. The fix involves adding `count` as a dependency.