# Firebase Asynchronous Operation Error
This repository demonstrates a common error in Firebase when dealing with asynchronous operations and document snapshots.  The `bug.js` file shows the problematic code, accessing a document's field before the data is fully loaded, leading to potential errors.  The solution, found in `bugSolution.js`, addresses this by properly checking for the existence of data before accessing it.

## How to reproduce
1. Clone the repository.
2. Install Firebase:
   ```bash
npm install firebase
```
3. Configure your Firebase project (add config details to `firebase.json`).
4. Run `bug.js` to see the error.
5. Run `bugSolution.js` to see the correct implementation.

## Solution
The solution uses a check (`doc.exists` and checks `doc.data()`) to ensure data has been loaded before accessing properties. Always handle asynchronous Firebase operations with proper error checks and data validation.