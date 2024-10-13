def calcular(op, a, b):
    if op == '+':
        return a + b
    elif op == '-':
        return a - b
    elif op == '*':
        return a * b
    elif op == '/':
        if b != 0:
            return a / b
        else:
            return "Erro: Divisão por zero"
    else:
        return "Operação inválida"

# Loop para realizar várias operações
while True:
    print("Selecione a operação:")
    print("1. Adição (+)")
    print("2. Subtração (-)")
    print("3. Multiplicação (*)")
    print("4. Divisão (/)")

    escolha = input("Digite o número da operação (ou 'sair' para encerrar): ")

    if escolha == 'sair':
        break

    if escolha in ['1', '2', '3', '4']:
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
        
        if escolha == '1':
            resultado = calcular('+', num1, num2)
        elif escolha == '2':
            resultado = calcular('-', num1, num2)
        elif escolha == '3':
            resultado = calcular('*', num1, num2)
        elif escolha == '4':
            resultado = calcular('/', num1, num2)

        print("Resultado:", resultado)
    else:
        print("Escolha inválida.")
