## Proposal Name: Password Manager

*TODO:* Needs a better name

## Summary:

A secure, decentralised, and beautiful password manager for Arweave.

## Motivation:

I think this bit is pretty self-explanitory :smile:

Storing your passwords for your applications in a manner where only you can see them, is truly amazing.

And a secure and simple way to share a password :heart_eyes:

## Specification:

| Dashboard | Modal |
| :-------: | :---: |
| <img width="1000" src="https://user-images.githubusercontent.com/62398724/101262721-a45a2700-3738-11eb-8b5b-e681286a2894.png"> | <img width="1000" src="https://user-images.githubusercontent.com/62398724/101262725-a623ea80-3738-11eb-9a19-d7f458183505.png"> |
| <img height="300" src="https://user-images.githubusercontent.com/62398724/101262748-d23f6b80-3738-11eb-9414-69acc543c493.PNG"> | <img height="300" src="https://user-images.githubusercontent.com/62398724/101262755-d4092f00-3738-11eb-93c7-3e4fc5871805.PNG"> |

> Ignore the error on mobile :sweat_smile:

When a user adds a new password entry, all data is encrypted using their JWK key.

A unique identifier is generated for this entry. This allows for easier tracking of changes.

A user can then edit, remove (different than delete as Arweave is permanent), and even share this password.

Here's how to transaction tags look:

```
App-Name: PasswordManager
ID: sVF9wNyvEWxRGbdHgFhJg
Action: Create | Edit | Remove | Share
```

The first MVP will be a web app, as can be seen above. Later on I'll look into a browser extension and mobile app :smile:

## Team:

John Letey ([@johnletey](https://github.com/johnletey)):

- CTO @ [th8ta](https://th8ta.org).
- Co-Founder of [Verto](https://verto.exchange).
- Development Lead & Co-Founder [ArVerify](https://github.com/ArVerify).

## Timeline:

~ 1 to 2 weeks

## Grant Requested (DAI):

2,000 DAI

## Ethereum Address:

`0x0f3F9D76D105E4F75171B3BA7f54094A4B2cc156`
