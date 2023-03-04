# Passwordless concepts for future authenticaion methods

## FIDO

Fast Identity Online

## FIDO2

Two different specifications for Fast Identity Online 

W3C - Web Auth
Internet website (relying parties) can requestion strong authentication from an end user computering platform.

FIDO Alliance - Computing platforms negotiate with users and 'authenticators' to unlock publick key-based credentials.
USB, NFC, BLE

## Typical Interaction

The cloud will ask for account authentication. Back end requests Username and Password.

## Requesting FIDO credentials 

Simple JAVASCRIPT API <WebAuthn-formatted request> sent to the Browser.

## FIDO Stochastic key

A new and unique key hash is generated for each service eg. Microsoft, Google, Yahoo

## API & Gesture

The back end API requests a 'Gesture' from the browser. A gesture is a local activation of a credential mechanism eg. face biometrics, fingerprint, Simple button. 

## The credential

FIDO uses public key cryptography. The token generates a keypair on first registration with a service. The private key portion is stored on the server of the service, while the public key is on the token.