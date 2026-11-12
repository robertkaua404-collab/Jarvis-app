# jarvis.py
import datetime
import random

def responder(texto):
    t = texto.lower()

    if "oi" in t or "olá" in t or "ola" in t:
        return "Olá! Eu sou o Jarvis. Como posso ajudar?"

    if "hora" in t:
        return f"Agora são {datetime.datetime.now().strftime('%H:%M')}."

    if "data" in t:
        return f"Hoje é {datetime.datetime.now().strftime('%d/%m/%Y')}."

    if "piada" in t:
        piadas = [
            "Por que o programador foi ao médico? Porque estava com um bug!",
            "O que o zero disse pro oito? Bonito cinto!",
        ]
        return random.choice(piadas)

    return "Ainda não sei responder isso, mas vou aprender!"

print("Jarvis iniciado. Digite 'sair' para encerrar.")
while True:
    entrada = input("Você: ")
    if entrada.lower() == "sair":
        print("Jarvis: Até logo!")
        break
    print("Jarvis:", responder(entrada))# Jarvis-app
Assistente pessoal Jarvis 
