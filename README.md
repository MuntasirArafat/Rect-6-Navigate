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
```

To do some calculations and then navigate to a new page in React Router v6, you can use the useNavigate hook inside a function that does the calculation and then calls the navigate function with the path of the new page.

Here's an example:



```javascript
import { useNavigate } from 'react-router-dom';

function doCalculationAndNavigate(num1, num2) {
  const result = num1 + num2; // do some calculation

  const navigate = useNavigate(); // use the useNavigate hook to get the navigate function
  navigate(`/result-page/${result}`); // navigate to the result page with the result as a parameter
}

class MyComponent extends React.Component {
  render() {
    return (
      <div>
        <button onClick={() => doCalculationAndNavigate(3, 5)}>Calculate and go to result page</button>
      </div>
    );
  }
}
