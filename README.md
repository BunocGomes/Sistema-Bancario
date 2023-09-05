# Sistema-Bancario
menu = (''' 
     Digite a opcao desejada: 
     [s]Sacar
     [d]Deposito
     [e]Extrato
     [q]Sair   
     ''')
saldo = 0 
limite = 500
saques = 0 
LIMITE_SAQUES = 3
extrato = ''

while True:
    opcao = input(menu)
    
    if opcao == 'd': #deposito
        valor_deposito = int(input('Digite o valor do deposito: '))
        if valor_deposito > 0:
            saldo += valor_deposito
            extrato += f'valor do deposito: {valor_deposito}\n'
        else:
            print('Valor Invalido')
    elif opcao == 's':
        valor_saque= int(input( 'Digite o valor do saque: '))
        if valor_saque > 0 :
            if saldo >= valor_saque and saques < 3 and valor_saque <= 500:
                saldo -= valor_saque
                saques += 1
                extrato += f'valor do saque: {valor_saque}\n'
            
            elif saques >=3:
              print('ja usou todos os saques do dia')
            else:
                print('saldo insuficiente ')
        else:
          print('valor invalido')     
    elif opcao == 'e':
        print(f'{extrato}\nSeu saldo:{saldo}')
    elif opcao == 'q':
        break
    else:
        print('digite uma opcao valida ')            
