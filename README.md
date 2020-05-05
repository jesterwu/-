# homework
const { router, text } = require('bottender/router');
const SayHi = async context => {
    await context.sendText('hihi')
    return context.sendText('haha')
   }
   
module.exports = async context => {
    return router([
        // return the SayHi action when receiving case-insensitive "hi" or "hello" text messages
        text(/^(hi|hello)$/i, SayHi),
      ])
};
