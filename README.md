# vivo-desafio

# Módulo 're' que fornece operações com expressões regulares.
import re

def validate_numero_telefone(phone_number):
    # Padrão de expressão regular para validar números de telefone no formato (XX) 9XXXX-XXXX
    pattern = r'^\(\d{2}\) 9\d{4}-\d{4}$'
    
    # Verifica se o padrão definido corresponde ao número de telefone fornecido.
    # O 're.match()' retorna um objeto 'match' se houver correspondência no início da string, caso contrário, retorna 'None'.
    if re.match(pattern, phone_number):  
        return "Número de telefone válido."
    else:
        return "Número de telefone inválido."

# Solicita ao usuário que insira um número de telefone e armazena o valor fornecido na variável 'phone_number'.
phone_number = input("Digite o número de telefone no formato (XX) 9XXXX-XXXX: ")  

# Chama a função 'validate_numero_telefone()' com o número de telefone fornecido como argumento e armazena o resultado retornado na variável 'result'.
result = validate_numero_telefone(phone_number)

# Imprime o resultado:
print(result)
