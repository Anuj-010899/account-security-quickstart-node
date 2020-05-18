![Twilio Logo](./twilio_logo_red.png)
# Twilio Account Security Quickstart - Twilio Authy and Twilio Verify

![](https://github.com/TwilioDevEd/account-security-quickstart-node/workflows/Node.js/badge.svg)

> We are currently in the process of updating this sample template. If you are encountering any issues with the sample, please open an issue at [github.com/twilio-labs/code-exchange/issues](https://github.com/twilio-labs/code-exchange/issues) and we'll try to help you.

## About

A simple NodeJS implementation of a website that uses Twilio Account Security services to protect all assets within a folder with Two-factor authentication. Additionally, it shows a Verify Phone Verification implementation.

It uses four channels for two-factor authentication delivery, SMS, Voice, Soft Tokens, and Push Notifications. You should have the [Authy App](https://authy.com/download/) installed to try Soft Token and Push Authentication support.

Learn more about Account Security and when to use the Authy API vs the Verify API in the [Account Security documentation](https://www.twilio.com/docs/verify/authy-vs-verify).

Implementations in other languages:

| .NET | Java | Python | PHP | Ruby |
| :--- | :--- | :----- | :-- | :--- |
| TBD | [Done](https://github.com/TwilioDevEd/account-security-quickstart-spring)  | [Done](https://github.com/TwilioDevEd/account-security-quickstart-django)  | [Done](https://github.com/TwilioDevEd/account-security-quickstart-php) | [Done](https://github.com/TwilioDevEd/account-security-quickstart-rails)  |

## Features

#### Authy Two-Factor Authentication Demo
- URL path "/protected" is protected with both user session and Twilio Authy Two-Factor Authentication
- One Time Passwords (SMS and Voice)
- SoftTokens
- Push Notifications (via polling)

#### Verify Phone Verification
- Phone Verification
- SMS or Voice Call

## Set up

### Requirements

- [Nodejs](https://nodejs.org/) v10 or v12
- [Mongo](https://docs.mongodb.com/manual/installation/)

### Twilio Account Settings

This application should give you a ready-made starting point for writing your own application.
Before we begin, we need to collect all the config values we need to run the application:

| Config Value | Description |
| :----------  | :---------- |
| ACCOUNT_SECURITY_API_KEY  | Create a new Authy application in the [console](https://www.twilio.com/console/authy/). After you give it a name you can view the generated Account Security production API key. This is the string you will later need to set up in your environmental variables.|

![Get Authy API Key](api_key.png)

### Local Development

1. Clone this repo and `cd` into it.

   ```bash
   git clone https://github.com/TwilioDevEd/account-security-quickstart-node.git
   cd account-security-quickstart-node
   ```

1. Install the dependencies.

   ```bash
   npm install
   ```

1. Set your environment variables. Copy the `env.example` file and edit it.

   ```bash
   cp .env.example .env
   ```

   See [Twilio Account Settings](#twilio-account-settings) to locate the necessary environment variables.

1. Check and make sure MongoDB is up and running.

1. Start the server (will run on port 3000).

   ```bash
   npm start
   ```

1.  Navigate to `http://localhost:3000`

That's it!

### Tests

You can run the tests locally by typing:

```bash
npm test
```


### Cloud deployment

Additionally to trying out this application locally, you can deploy it to a variety of host services. Here is a small selection of them.

Please be aware that some of these might charge you for the usage or might make the source code for this application visible to the public. When in doubt research the respective hosting service first.

| Service                           |                                                                                                                                                                                                                           |
| :-------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Heroku](https://www.heroku.com/) | [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)                                                                                                                                       |

## Resources

- The CodeExchange repository can be found [here](https://github.com/twilio-labs/code-exchange/).

## Contributing

This template is open source and welcomes contributions. All contributions are subject to our [Code of Conduct](https://github.com/twilio-labs/.github/blob/master/CODE_OF_CONDUCT.md).

## License

[MIT](http://www.opensource.org/licenses/mit-license.html)

## Disclaimer

No warranty expressed or implied. Software is as is.

[twilio]: https://www.twilio.com
