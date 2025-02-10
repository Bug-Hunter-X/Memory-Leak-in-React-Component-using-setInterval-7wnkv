# React setInterval Memory Leak

This repository demonstrates a common React bug: a memory leak caused by the improper use of `setInterval` within the `useEffect` hook.

The `bug.js` file shows the faulty component. The `setInterval` function is called without a cleanup function to stop the interval, resulting in a memory leak. This is because the component keeps on incrementing the count even after it is unmounted.

The `bugSolution.js` file provides the corrected version with a proper cleanup function to address the memory leak.