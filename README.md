# React Native FlatList KeyExtractor Bug

This repository demonstrates a common yet subtle bug in React Native's FlatList and SectionList components: incorrect usage of the `keyExtractor` prop.  Using a non-unique key for items can lead to unpredictable behavior, including incorrect rendering, stale data, and performance issues.  This example shows the bug and its correction.

## Bug
The `BuggyFlatList.js` file shows how using a non-unique key (e.g., relying on the index) can cause problems.  The `keyExtractor` function incorrectly uses the item index as the key.  This breaks when items are added, removed, or re-ordered.

## Solution
The `FixedFlatList.js` file provides the correct implementation.  A unique identifier (like a UUID or the item's unique ID from the data source) should always be used as the key.  This ensures proper rendering and optimal performance.

## How to run
1. Clone the repo
2. `npm install` or `yarn install`
3. `npx react-native run-android` or `npx react-native run-ios`