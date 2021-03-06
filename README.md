![SecureDrop](/docs/images/logo.png)

[![Build Status](https://travis-ci.org/freedomofpress/securedrop.png)](http://travis-ci.org/freedomofpress/securedrop)

SecureDrop is an open-source whistleblower submission system that media organizations can use to securely accept documents from and communicate with anonymous sources. It was originally created by the late Aaron Swartz and is currently managed by [Freedom of the Press Foundation](https://freedom.press).

## Technical Summary

SecureDrop is a tool for sources to communicate securely with journalists. The SecureDrop application environment consists of three dedicated computers:

* `Secure Viewing Station`: An air-gapped laptop running the [Tails operating system](https://tails.boum.org/) from a USB stick that journalists use to decrypt and view submitted documents. (If this laptop does not have a DVD drive, buy an external DVD drive you can use with it.)
* `Application Server`: Ubuntu server running two segmented Tor hidden services. The source connects to the first, public-facing Tor hidden service to send messages and documents to the journalist. The journalist connects to the second authenticated Tor hidden service to download encrypted documents and respond to sources.
* `Monitor server`: Ubuntu server that monitors the `Application Server` and sends email alerts.

In addition to these dedicated computers, the journalist will also use his or her normal workstation computer:

* `Journalist Workstation`: The every-day laptop that the journalist uses for his or her work. The journalist will use this computer to connect to the `Application Server` to download encrypted documents that he or she will transfer to the `Secure Viewing Station`. The `Journalist Workstation` is also used to respond to sources.

Depending on the news organizations's threat model, it is recommended that journalists always use the [Tails operating system](https://tails.boum.org/) on their `Journalist Workstation` when connecting to the `Application Server`. Alternatively, this can also be its own dedicated computer.

These computers should all physically be in your organization's office.

## How to Contribute

See the [Development Guide](/docs/develop.md).

## How to Install SecureDrop

See the [Installation Guide](/docs/install.md).

## How to Use SecureDrop

See [how to use SecureDrop as a source](/docs/source_user_manual.md) and [how to use SecureDrop as a journalist](/docs/journalist_user_manual.md).

## License

SecureDrop is open source and released under the [GNU Affero General Public License v3](/LICENSE).

The [wordlist](/securedrop/wordlist) we use to generate source passphrases comes from [Diceware](http://world.std.com/~reinhold/diceware.html), and is licensed under Creative Commons Attribution 3.0 Unported thanks to A G Reinhold.
