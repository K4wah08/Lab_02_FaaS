# Lab_02_FaaS
from telegram import Update
from telegram.ext import Application, CommandHandler, MessageHandler, filters, ContextTypes
TOKEN = "YOUR_API_TOKEN"
async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text("Olá! Eu sou um bot. Me mande uma mensagem para queeu a responda.")
async def echo(update: Update, context: ContextTypes.DEFAULT_TYPE):
    received_text = update.message.text
    response = f"Você disse: {received_text}"
    await update.message.reply_text(response)
if __name__ == "__main__":
    main()
