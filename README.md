# google-apps-radius

This is a RADIUS server that authenticates against a Google Apps domain. The
authentication is done using a headless browser
as opposed to Google's deprecated [ClientLogin](https://developers.google.com/accounts/docs/AuthForInstalledApps).

## Installing

Installation can be done via [npm](https://www.npmjs.org/):

    npm install -g google-apps-radius

## Usage

    Usage: google-apps-radius --address <address> --port [port] --domain <domain> --secret <secret>

    Options:
      --domain   [required]
      --secret   [required]
      --port     [default: 1812]
      --address  [default: "0.0.0.0"]
      --otp      [default: disabled]

## Two Factor / OTP support

Passing the `--otp` flag enables two-factor authentication for all requests.  In this mode, it is expected that the password sent to the radius server will be a concatenation of the user's password and their one-time password (a 6 digit code), eg "my-password123456".

## Known limitations

- Only supports RADIUS PAP (password authentication protocol)

## Author

Tim Cooper <<tim.cooper@layeh.com>>

## License

GPLv3
