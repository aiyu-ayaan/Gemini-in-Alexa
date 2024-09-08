# Custom Alexa Command with Gemini Integration

This project demonstrates how to create a custom Alexa command that integrates with the Gemini API. The setup includes building an Alexa skill, adding an invocation name, and configuring an intent strategy, with a `config.js` file for API key management.

## Features
- Custom Alexa skill with invocation name
- Integration with the Gemini API
- JavaScript configuration for easy setup

## Prerequisites
Before you begin, ensure you have:
- An Amazon Developer account
- AWS Lambda setup (for hosting your Alexa skill backend)
- Gemini API key

## Setup

### Step 1: Create `modelconfig.json` (Optional)
If you prefer to skip the manual configuration of the invocation name and intent strategy (Steps 2 and 3), you can use the provided `modelconfig.json` file.

1. Place the `modelconfig.json` file in the root of your project. This file contains predefined configurations that will automatically set up the invocation name and intent strategy.

### Step 2: Create `config.js`
To securely integrate the Gemini API, you'll need a configuration file for the API key.

1. Create a `config.js` file in the root of your project.
2. Add the following content to the file:

   ```javascript
   const API_KEY = "your_gemini_api_key_here";

   module.exports = { API_KEY };
   ```

   Replace `"your_gemini_api_key_here"` with your actual Gemini API key.

### Step 3: Install Dependencies
Run the following command to install the necessary dependencies:

```bash
npm install
```

### Step 4: Deploy the Alexa Skill
Deploy the skill using [Alexa Developer Console](https://developer.amazon.com/alexa), ensuring that it correctly invokes the Gemini API based on your custom logic.

## Usage
Once your skill is set up, you can invoke it using the defined invocation name. For example:

> "Alexa, open _your_invocation_name_"

## Contributing
Feel free to submit issues or pull requests to improve this project.

## License
```MIT License

Copyright (c) 2024 Ayaan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```