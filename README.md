# calculadora-basica
calculadora basica rapida simples
# Função para somar dois números
def somar(a, b):
    return a + b

# Função para subtrair dois números
def subtrair(a, b):
    return a - b

# Função para multiplicar dois números
def multiplicar(a, b):
    return a * b

# Função para dividir dois números
def dividir(a, b):
    # Trata a divisão por zero para evitar erros
    if b == 0:
        return "Erro! Divisão por zero não é permitida."
    return a / b

# Início do programa
def calculadora():
    print("Selecione a operação:")
    print("1. Somar")
    print("2. Subtrair")
    print("3. Multiplicar")
    print("4. Dividir")
    print("0. Sair")

    while True:
        # Pede a escolha do usuário
        escolha = input("Digite sua escolha (1/2/3/4/0): ")

        # Verifica se a escolha é válida
        if escolha in ('1', '2', '3', '4'):
            try:
                num1 = float(input("Digite o primeiro número: "))
                num2 = float(input("Digite o segundo número: "))
            except ValueError:
                print("Entrada inválida. Por favor, digite um número.")
                continue

            if escolha == '1':
                print(f"Resultado: {somar(num1, num2)}")

            elif escolha == '2':
                print(f"Resultado: {subtrair(num1, num2)}")

            elif escolha == '3':
                print(f"Resultado: {multiplicar(num1, num2)}")

            elif escolha == '4':
                print(f"Resultado: {dividir(num1, num2)}")

        # Permite ao usuário sair do programa
        elif escolha == '0':
            print("Saindo da calculadora. Até mais!")
            break

        else:
            print("Escolha inválida. Por favor, tente novamente.")

# Executa a função principal da calculadora
if __name__ == "__main__":
    calculadora()
