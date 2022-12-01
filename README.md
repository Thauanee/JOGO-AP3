# JOGO-AP3from random import randint 
print("""Seja bem vindo ao jogo da soma.
      """)
print('''Regras:
      ''')
print("""Nesse jogo Você deve responder as operações corretamente!
Se voce acertar a questão você ira receber 5 pontos.
Caso contrario você ira perder 2 pontos.
Se voce com saldo negativo voce perde o jogo!
Se voce conseguir passar de 100 pontos você ganha o jogo!

Você irá começar com 10 pontos!

Boa sorte!""")
pontos = 10
while pontos >= 0 and pontos <= 100:
    numeros1 = randint(0, 99)
    numeros2 = randint(0, 99)
    resultado = numeros1 + numeros2
    print('-=-'*15)
    sua_vez = int(input('Qual a soma entre {} e {}? '.format(numeros1, numeros2)))
    if sua_vez != resultado:
        pontos = pontos - 2
        print(' ')    
        print('Você errou!!')
        print('Você perdeu 2 pontos')
        print('Pontuação atual: {}'.format(pontos))
        print('')
    else:
        pontos = pontos +5
        print(' ')    
        print('Você Acertou!!')
        print('Você ganhou 5 pontos')
        print('Pontuação atual: {}'.format(pontos))
        print('')
if pontos < 0:
    print('GAME OVER')
else:
    print('Meus parabens!!!')
    print('Voce Venceu!!!')
