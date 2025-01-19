# React useEffect setInterval Memory Leak

This repository demonstrates a common React bug involving memory leaks caused by improper usage of the `setInterval` function within the `useEffect` hook.  The `bug.js` file showcases the faulty code, while `bugSolution.js` provides the corrected version.

**Problem:**
The original code uses `setInterval` to update a counter every second. However, it omits the essential cleanup function within the `useEffect`'s return statement. This results in the interval continuing indefinitely, even after the component unmounts, leading to a memory leak.

**Solution:**
The solution incorporates a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, thereby preventing memory leaks and ensuring proper resource management.