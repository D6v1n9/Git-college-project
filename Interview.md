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

