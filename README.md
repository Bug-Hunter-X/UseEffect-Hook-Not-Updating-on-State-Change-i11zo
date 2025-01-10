# React useEffect Hook Not Updating on State Change

This repository demonstrates a common error when using the `useEffect` hook in React. The provided code intends to log the count to the console whenever the count state variable changes. However, due to an incorrect implementation, the log only occurs once when the component mounts.

## Bug Description

The issue is that the useEffect hook is missing the dependency array.  Without it, the effect only runs once after the initial render.  The solution is to include the `count` variable in the dependency array so that the effect runs whenever `count` changes.

## Solution

The solution involves adding the `count` variable to the dependency array in the `useEffect` hook to ensure the effect runs whenever the state variable changes.  This ensures the console.log runs on every click of the increment button.