const TelegramBot = require('node-telegram-bot-api');
// Твой токен из скриншота
const token = '8577027584:AAHA35xAEAiuvwXR7No25Dj6QIenix3Z4_8'; 
const bot = new TelegramBot(token, {polling: true});

bot.onText(/\/start/, (msg) => {
    bot.sendMessage(msg.chat.id, 'Привет! Жми кнопку ниже, чтобы запустить Crash TON!', {
        reply_markup: {
            inline_keyboard: [[
                { text: '🚀 Играть', web_app: { url: 'ТВОЯ_ССЫЛКА_С_GITHUB' } }
            ]]
        }
    });
});

