This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Getting Started

See `src/App.js` and `src/App.css` for chatbot integration.

#### Prerequisites

You need to [add the Interactions category](https://docs.amplify.aws/lib/interactions/getting-started/q/platform/js#create-new-chatbot) to your app with Amplify CLI.

#### Customizing Header with Slots

If you wish to add more to the header than just text, you can use a [slot element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/slot) to replace the header content with your own markup. For example:

_App.js_

```javascript
import logo from './amplify-logo.svg';
// ...

function App() {
  // ...
  return (
    <div className="content">
      <AmplifyChatbot
        botTitle="Chatbot Lex"
        botName="BookTrip_dev"
        welcomeMessage="Hello, how can I help you?"
        voiceEnabled={true}
      >
        <div slot="header" className="header-slot">
          <img alt="" src={logo} height="40px" />
          Amplify Bot
        </div>
      </AmplifyChatbot>
      <br />
    </div>
  );
}
```
