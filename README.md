# react-otp-input

A fully customizable, one-time password input component for the web built with React.

![GIPHY](https://media.giphy.com/media/9JiszPVOX5FuPfJm39/giphy.gif)

[Live Demo](https://devfolioco.github.io/react-otp-input)

[CodeSandbox](https://codesandbox.io/s/0y849kwoqv)

## Installation

To install the latest stable version:

```
npm install --save react-otp-input
```

Basic usage:

```javascript
import React, { Component } from 'react';
import OtpInput from 'react-otp-input';

export default class App extends Component {
  state = {
    otp: '',
  };

  handleChange = otp => this.setState({ otp });

  render() {
    return (
      <div>
        <OtpInput
          onChange={this.handleChange}
          numInputs={6}
          separator={<span>-</span>}
        />
      </div>
    );
  }
}
```

## API

<table>
  <tr>
    <th>Name<br></th>
    <th>Type</th>
    <th>Required</th>
    <th>Default</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>numInputs</td>
    <td>number</td>
    <td><strong>true</strong></td>
    <td>4</td>
    <td>Number of OTP inputs to be rendered.</td>
  </tr>
  <tr>
    <td>onChange</td>
    <td>function</td>
    <td><strong>true</strong></td>
    <td>console.log</td>
    <td>Returns OTP code typed in inputs.</td>
  </tr>
  <tr>
    <td>value</td>
    <td>string / number</td>
    <td><strong>true</strong></td>
    <td>''</td>
    <td>The value of the otp passed into the component.</td>
  </tr>
  <tr>
    <td>separator</td>
    <td>component<br></td>
    <td>false</td>
    <td></td>
    <td>Provide a custom separator between inputs by passing a component. For instance, <code>&lt;span&gt;-&lt;/span&gt;</code> would add <code>-</code> between each input</td>
  </tr>
  <tr>
    <td>containerStyle</td>
    <td>style (object) / className (string)</td>
    <td>false</td>
    <td>none</td>
    <td>Style applied or class passed to container of inputs.</td>
  </tr>
  <tr>
    <td>inputStyle</td>
    <td>style (object) / className (string)</td>
    <td>false</td>
    <td>none</td>
    <td>Style applied or class passed to each input.</td>
  </tr>
  <tr>
    <td>focusStyle</td>
    <td>style (object) / className (string)</td>
    <td>false</td>
    <td>none</td>
    <td>Style applied or class passed to inputs on focus.</td>
  </tr>
  <tr>
    <td>isDisabled</td>
    <td>boolean</td>
    <td>false</td>
    <td>false</td>
    <td>Disables all the inputs.</td>
  </tr>
  <tr>
    <td>disabledStyle</td>
    <td>style (object) / className (string)</td>
    <td>false</td>
    <td>none</td>
    <td>Style applied or class passed to each input when disabled.</td>
  </tr>
  <tr>
    <td>hasErrored</td>
    <td>boolean</td>
    <td>false</td>
    <td>false</td>
    <td>Indicates there is an error in the inputs.</td>
  </tr>
  <tr>
    <td>errorStyle</td>
    <td>style (object) / className (string)</td>
    <td>false</td>
    <td>none</td>
    <td>Style applied or class passed to each input when errored.</td>
  </tr>
  <tr>
    <td>shouldAutoFocus</td>
    <td>boolean</td>
    <td>false</td>
    <td>false</td>
    <td>Auto focuses input on inital page load.</td>
  </tr>
  <tr>
    <td>isInputNum</td>
    <td>boolean</td>
    <td>false</td>
    <td>false</td>
    <td>Restrict input to only numbers.</td>
  </tr>
</table>

## Breaking changes when porting to v1.0.0

`react-otp-input` is now a controlled component to facilitate functionalities that weren't possible before from the application using it, such as clearing or pre-assigning values. For `v1.0.0` and above, a `value` prop needs to be passed in the component for it function as expected.

## Development

To run the development server:

```
npm run dev
```

To run the development server for example:

```
npm run docs
```

To make a production build of the example:

```
npm run docs:prod
```

## Checklist

- [x] Add flowtypes
- [x] Add ESLint, Prettier for code quality
- [x] Add styling support for states including focus/disabled
- [ ] Travis CI, Codecov
- [ ] Write tests

## Contributing

Feel free to open issues and pull requests!

## License

MIT



## My_changes

Description
react-native-otp-inputs is fully customizable, pure JavaScript package, that provides solution for One-time password feature with user friendly events like moving to previous input with backspace or going to next when filled in. It supports pasting and otp code into inputs

Installation
React-Native version	installation
>= 0.53.0 < 0.57.0	yarn add react-native-otp-inputs@1.1.0
<= 0.57.0	yarn add react-native-otp-inputs
It's because of onKeyPress event implementation on android.

Basic usage
import React, { Component } from 'react'
import { View } from 'react-native'
import OtpInputs from 'react-native-otp-inputs'
 
export default class App extends Component {
  render() {
    return (
      <View style={styles.container}>
        <OtpInputs
          handleChange={code => console.log(code)}
          numberOfInputs={6}
        />
      </View>
    )
  }
}
API
Method	Type	Required	Default	Description
autoCapitalize	string	false	'none'	Defines input auto capitalization (only use with keyboardType)
clearTextOnFocus	boolean	false	false	Defines if input text should be cleared on focus
containerStyles	style (object)	false	none	Styles applied to whole container
errorMessage	string	false	none	Error message that is displayed above inputs
errorMessageContainerStyles	style (object)	false	defaultStyles	Styles applied to error message container
errorMessageTextStyles	style (object)	false	none	Styles applied to error message text
focusedBorderColor	string	false	#0000ff	borderColor of input when focused
focusStyles	style (object)	false	none	Styles applied to the input when its focused
handleChange	function	true	console.log	Returns otp code which is typed in inputs
inputStyles	style(object)	false	defaultStyles	Styles applied to single input
inputContainerStyles	style (object)	false	defaultStyles	Styles applied to each input container
inputsContainerStyles	style (object)	false	defaultStyles	Styles applied to inputs container
inputTextErrorColor	string	false	#ff0000	Color of text inside input container when error is passed in
keyboardType	string	true	'phone-pad'	Keyboard type for inputs
numberOfInputs	number	true (1..6)	4	How many inputs should be rendered
secureTextEntry	boolean	false	false	Defines if input will hide text inside
selectTextOnFocus	boolean	false	true	Defines if input text should be selected on focus
unfocusedBorderColor	string	false	transparent	borderColor of input when not focused
testIDPrefix	string	false	otpInput-${inputIndex}	Prefix that will be applied as a testID for each input
isRTL	boolean	false	false	Defines if the app is currently in RTL (preferably pass {I18nManager.isRTL}). Keeps the OTP boxes in LTR alignment.
placeholder	string	false	none	Placeholder for the input boxes.
Methods
Those can be called on ref:

import React, { Component } from 'react'
import { View } from 'react-native'
import OtpInputs from 'react-native-otp-inputs'
 
export default class App extends Component {
  otpRef = React.createRef()
 
  clearOTP = () => {
    otpRef.current.clear()
  }
 
  render() {
    return (
      <View style={styles.container}>
        <Button title="Clear" onPress={this.clearOTP} />
        <OtpInputs
          ref={this.otpRef}
          handleChange={code => console.log(code)}
          numberOfInputs={6}
        />
      </View>
    )
  }
}
Method	Description
clear	Clears inputs and returns to handleChange method empty string
