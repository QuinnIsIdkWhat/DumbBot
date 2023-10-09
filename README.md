# DumbBot
import discord
import random

client = discord.Client()

@client.event
async def on_ready():
    print("Bot is ready.")

@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content.startswith("!test1"):
        random_number = random.randint(1, 100)
        await message.channel.send(f"Random number: {random_number}")
        \
