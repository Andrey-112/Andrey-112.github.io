# Andrey-112.github.io
from telegram.ext import Updater, CommandHandler


def hello(bot, update):
    update.message.reply_text(
        'Hello {}'.format(update.message.from_user.first_name))


updater = Updater('570423026:AAFusVvo108Nk0R6BoPN5EWEVvQqfey1U0Y')

updater.dispatcher.add_handler(CommandHandler('hello', hello))

updater.start_polling()
updater.idle()

import telegram
