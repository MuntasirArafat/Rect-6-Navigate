# button-click-naviget



To navigate to another page on button click in React Router v6 using a class component, you can use the useNavigate hook to get access to the navigate function and then call it on button click.

Here's an example:


```javascript
import { useNavigate } from 'react-router-dom';

class MyComponent extends React.Component {
  render() {
    const navigate = useNavigate(); // use the useNavigate hook to get the navigate function

    return (
      <div>
        <button onClick={() => navigate('/other-page')}>Go to other page</button>
      </div>
    );
  }
}
