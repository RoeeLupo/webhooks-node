# Laffey
> :office: **| Webhook handler for [discord.boats](https://discord.boats)**

## Example
```js
const { Server } = require('laffey');

const handler = new Server(7700, '/webhook', {
  token: 'youshallnotpass'
});

handler
  .on('vote', (voter, bot) => console.log(`${voter.username} has voted ${bot.name}`))
  .on('listen', () => console.log(`Listening on port ${handler.port}`))
  .listen(); // It listens and emits the listen event /\
```

## License
**laffey** is released under the MIT License. Read [here](/LICENSE) for more information.