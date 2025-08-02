### Recent Notification in Dashboard

My `recentNotificationSlice` Redux slice manages a `notifications` array containing notification summaries. When a user selects a notification, the slice fetches and stores its full details in `notificationDetails`. This structure enables displaying a concise list of notifications while supporting detailed views as needed.

[Related GPT discussion](https://chatgpt.com/share/6880fd42-a6ac-8007-9026-0da8a076e91f)

### What is PropTypes?
PropTypes helps you validate that the props passed to a component are of the expected type. If a prop doesn't match the expected type, React will show a warning in the browser console (only in development mode).

```javascript
import PropTypes from 'prop-types';
function Greeting({ name, age }) {
  return <p>Hello, {name}. You are {age} years old.</p>;
}

Greeting.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number,
};
```
### What is slice?
slice(start, end) lets you extract part of a string. It's zero-based and the end is optional and not included. It's commonly used to manipulate strings, like capitalizing the first letter or removing prefixes.

### Redux Toolkit – rejected Flow: With vs Without rejectWithValue
```vbnet
               ┌──────────────────────┐
               │   Thunk is called    │
               └──────────┬───────────┘
                          │
                   API Request
                          │
              ┌───────────┴───────────┐
              │                       │
           Success                 Error Occurs
              │                       │
              ▼                       ▼
      dispatch.fulfilled     dispatch.rejected
                                      │
        WITHOUT rejectWithValue       │       WITH rejectWithValue
      ┌────────────────────────────┐  │  ┌──────────────────────────────┐
      │ action.payload = undefined │  │  │ action.payload = custom data │
      │ action.error.message =     │  │  │ (e.g. server error, status)  │
      │   error.message            │  │  │ action.error is still filled │
      └────────────────────────────┘  │  └──────────────────────────────┘
                                      │
      Reducer:                        │     Reducer:
      state.error =                   │     state.error =
         action.error.message         │        action.payload

```

### Redux Toolkit – rejectWithValue Notes
#### What is rejectWithValue?
- A helper provided by createAsyncThunk.
- Lets you send a custom error payload when an async thunk fails.
- This payload will be available in action.payload for the rejected case.

#### Default Behavior (without rejectWithValue)
- If a thunk throws an error:
  - action.payload → undefined
  - action.error.message → error message (default from JS error or Axios)
- You must read errors from action.error.message in your reducer.
#### Example
```javascript
builder.addCase(myThunk.rejected, (state, action) => {
  state.error = action.error.message;
});
```
### When to Use
#### ✅ Use rejectWithValue when:
- You need detailed error messages from API (e.g., "Faculty not found for classId 12")
- You want consistent error object structure in reducers.
- You need to store extra error details (status, validation issues).
#### ❌ Skip it when:
- You only need a generic error message like "Something went wrong".
- You don’t care about shaping the error payload.
### Comparison Table
| Feature                    | Without `rejectWithValue` | With `rejectWithValue` |
| -------------------------- | ------------------------- | ---------------------- |
| **Where is error stored?** | `action.error.message`    | `action.payload`       |
| **Custom error shape?**    | ❌ No                      | ✅ Yes                  |
| **Ease of use**            | Simpler                   | Slightly more setup    |
| **Detailed API errors**    | ❌ Harder                  | ✅ Easy                 |

### Error Payload – Definition
- An error payload is the data you send along with a rejected action when an async thunk fails.
- It’s stored in action.payload in the reducer (only if you use rejectWithValue).
- It can contain anything you want:
    - A simple error string
    - An object with error details
    - Validation errors from the server
    - HTTP status code
### Without rejectWithValue
#### When your thunk throws an error:
```javascript
throw new Error("Network failed");
```
#### The rejected action looks like this:
```javascript
{
  type: 'myThunk/rejected',
  payload: undefined,          // ❌ No error payload
  error: {
    message: "Network failed"  // Default JS error message
  }
}
```
### With rejectWithValue
#### When to use
```javascript
return rejectWithValue({ message: "Faculty not found", code: 404 });
```
#### The rejected action looks like this:
```javascript
{
  type: 'myThunk/rejected',
  payload: {                   // ✅ Error payload
    message: "Faculty not found",
    code: 404
  },
  error: {
    message: "Rejected"        // Default message from Redux Toolkit
  }
}
```
You can now read the error directly from action.payload.
