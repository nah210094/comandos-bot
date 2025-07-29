import discord
from discord.ext import commands
from psw import gen_pass
import random
intents = discord.Intents.default()
intents.message_content = True
bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Hola, soy un bot {bot.user}!')

@bot.command()
async def heh(ctx, count_heh = 5):
    await ctx.send("he" * count_heh)

@bot.command()
async def IGN(ctx):
    await ctx.send(f'Hola, me llamo ignacio. soy el creador de este bot! Me gusta el basquet y la actividad fisica mas q nada!')

@bot.command()
async def psw(ctx, *, longitud:int):
    contra = gen_pass(longitud)
    await ctx.send (f'tu contraseña segura segurisima es!!!!---->  {contra}')

l_emojis = ['👍','💩','💨','😎','🛌','🏀','🔥','⭐','💠','💭','🇦🇷ℹ️','💸','💣','🥁','🏋️','⛹️','💆‍♂️','👩‍💻','👨‍🔬']
l_frases = ['El único lugar donde el éxito aparece antes que el trabajo es en el diccionario.',
         'No esperes el momento perfecto, toma el momento y hazlo perfecto.', 'Se tu mismo',
         'La gente dice que nada es imposible, pero yo hago nada todos los días',
         'El talento gana partidos, pero el trabajo en equipo y la inteligencia ganan campeonatos',
         'Aunarse es el principio. Mantenerse juntos, es el progreso. Trabajar juntos es el éxito']

@bot.command()
async def emoji(ctx):
    emo = random.choice(l_emojis)
    await ctx.send (f'mira esto bro----> {emo}')

@bot.command()
async def frase(ctx):
    fr = random.choice(l_frases)
    await ctx.send (f'aqui tienes tu frase---> {fr}')

@bot.command()
async def joined(ctx, member: discord.Member):
    """Dice cuando una miembro se unió"""
    await ctx.send(f'{member.name} joined {discord.utils.format_dt(member.joined_at)}')    

bot.run("ingrese su token aqui")
