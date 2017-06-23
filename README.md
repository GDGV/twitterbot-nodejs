# GDG Cloud Vancouver TwitterBot-NodeJS

[![Twitter Follow](https://img.shields.io/twitter/follow/gdgcvbot.svg?style=social)](https://twitter.com/gdgcvbot)

This code is a fork of the main repo [here](https://github.com/nisrulz/twitterbot-nodejs)

Yeah it pretty much does what it says in the title. Its a twitter bot which can post tweets, retweet other tweets and possibly fav tweets.

> It attempts to retweet once per hour

## Installation

- Install [Node.js](http://nodejs.org/)
- Clone this repo

```bash
  git clone https://github.com/nisrulz/twitterbot-nodejs.git
```

- Run

```bash
npm install
```

## Connecting to Twitter

- Register a Twitter account and also get its "app info".
> Twitter doesn't allow you to register multiple twitter accounts on the same email address. I recommend you create a brand new email address (perhaps using Gmail) for the Twitter account. Once you register the account to that email address, wait for the confirmation email.

- Now go [here](https://apps.twitter.com/app/new) and log in as the Twitter account for your bot:
- Fill up the form and submit.
- Next once the submission completes you will be taken to a page which has the
  - "Settings" tab : Update details here
  - "Permissons" tab :  Enable `Read and Write`
  - "Key and Access Token" tab : Click on `Create my access token`.
- Use the generated tokens in the "Key and Access Token" tab to fill the fields under the `config.js` file in your app directory. It should look like this:

```javascript
module.exports = {
  consumer_key:         'blah',
  consumer_secret:      'blah',
  access_token:         'blah',
  access_token_secret:  'blah'
}
```

- Update the code under `bot.js` , with the your values. Best of all modify the code, tinker with it.
- Now type the following in the command line in your project directory:

```bash
node bot.js
```

Hopefully at this point you see a message like "Success! Check your bot, it should have retweeted something."
Ok it won't say that, you have to code that in. Its as simple as

```javascript
console.log("Success! Check your bot, it should have retweeted something.");
```

Check the Twitter account for your bot, and it should have retweeted a tweet with the provided hashtag.

### Whats Next

You might want to push this app to a running server , probably [heroku](https://www.heroku.com/).

> Note : Heroku servers would go back to sleep if there is no activity after some time, so you can have a look at [Kaffeine](https://kaffeine.herokuapp.com/) , to keep your server active.

---

> Do not misuse the twitter api to spam or burden the server load for twitter api , as twitter follows a strict rule of closing down accounts that do that. Please read [here for the rules](https://support.twitter.com/articles/18311)
