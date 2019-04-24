import discord
from discord.ext import commands
from gtts import gTTS
import os
client = discord.Client()
TOKEN = "tokenhere"
class MyClient(discord.Client):
    async def on_ready(self):
        print('ZALOGOWANO JAKO', self.user)  
    async def on_message(self, message):
        if(len(message.content) < 100):
        	print(message.guild.name + " | " + message.author.nick + " :" + message.content)
	        tekst = message.content
	        tts = gTTS(message.author.nick +" mówi " + tekst + " na " + message.guild.name,'pl')
	        tts.save('audio.mp3')
	        os.system('mpg321 -q audio.mp3')


        
        
client = MyClient()
client.run(TOKEN,bot=False)
