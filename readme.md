Hello,

Welcome to my project, feel free to send me an email at nateKM1@protonmail.com.

Support for more exchanges coming soon!

Feel free to send me a Bitcoin Cash donation here (1NLkGPnNbT9iCJ35U9UfsURANtYgNREVtq)
or email me if you want to send me something else and I will respond with an address.


How to use:

  This monitors a users twitter stream (instant) and acts on every
  tweet that It sees. It is currently pointed at the correct one.

 How to Set Up:

    1. You must get your twitter API consumer_key, consumer_secret, access_token, and access_token_secret and enter them on lines 14 to 18. This allows you to connect to a users twitter stream.

  ```javascript
    const T = new Twit({
    consumer_key: '',
    consumer_secret: '',
    access_token: '',
    access_token_secret: ''
   });
  ```


  2. You must give this program your Poloniex API_Key, and Secret that goes along with it (on lines 5, 6)

  ```javascript
  const API_KEY = '';
  const SECRET = '';
  ```

  3. You must choose if you want to use safecheck or not (default is true). Safecheck makes sure that the given tweet has the string coin of the day inside of it and wont buy any match without it. With safeCheck as false it will purchase any coin it sees in the tweet stream.

  4. Setting up Poloniex Class

```javascript
  const polo = new Poloniex(API_KEY, SECRET, 0, 0);
  /*
  // const polo = new Poloniex(API_KEY, SECRET, buyAmount (default set), markup (default set as 0));
  API_KEY = the api key you recieve from the exchange poloniex; (Do not touch this..remember..you already set it on line 5-6)
  SECRET = the secret you recieve from the exchange poloniex; (Do not touch this..remember..you already set it on line 5-6)
  buyAmount = the amount of BTC you want to spend on the coin that was just tweeted about (min 0.000001); (you must set this)
  markup = incase another bot gets a request in faster and clears the book, this lets you send a buy with a markup. (and set this)   Recomended @ should be .01 - .05;
*/
```

 To Run, make sure to have node.js + npm installed https://nodejs.org/en/
  The first command changes your current directory
  The second command installs dependencies
  The third command starts the program

```bash
   1. cd /*directory*/
   2. npm install
   3. node index.js
```


 
