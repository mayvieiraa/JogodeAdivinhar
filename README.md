# JogodeAdivinhar

import random

def jogo_adivinhacao():
    numero_secreto = random.randint(1, 100)
    tentativas = 0
    max_tentativas = 10
    
    print("Bem-vindo ao jogo de adivinhação!")
    print("Estou pensando em um número entre 1 e 100.")
    print("Você tem que adivinhar qual é esse número em até", max_tentativas, "tentativas.")
    
    while tentativas < max_tentativas:
        palpite = int(input("\nDigite seu palpite: "))
        tentativas += 1
        
        if palpite < numero_secreto:
            print("Seu palpite foi baixo. Tente um número maior.")
        elif palpite > numero_secreto:
            print("Seu palpite foi alto. Tente um número menor.")
        else:
            print("Parabéns! Você acertou o número em", tentativas, "tentativas!")
            break
    
    if tentativas == max_tentativas:
        print("\nSuas tentativas acabaram. O número secreto era", numero_secreto)

jogo_adivinhacao()
