# lista-3


# 4
vendas_diarias = [10, 15, 20, 5, 0, 8, 12, 30]
analise = {}

analise['total_vendas'] = sum(vendas_diarias)

analise['dia_mais_vendas'] = vendas_diarias.index(max(vendas_diarias)) + 1
analise['dia_menos_vendas'] = vendas_diarias.index(min(vendas_diarias)) + 1

analise['media_vendas'] = analise['total_vendas'] / len(vendas_diarias)


analise['dias_acima_da_media'] = [dia + 1 for dia, vendas in enumerate(vendas_diarias) if vendas > analise['media_vendas']]


for chave, valor in analise.items():
    print(f"{chave}: {valor}")



# 6
emprestimos = [
    {"titulo": "Dom Casmurro", "usuario": "Ana", "dias_emprestado": 5},
    {"titulo": "1984", "usuario": "Carlos", "dias_emprestado": 12},
    {"titulo": "O Hobbit", "usuario": "Marina", "dias_emprestado": 3},
    {"titulo": "Capitães da Areia", "usuario": "Beatriz", "dias_emprestado": 15},
    {"titulo": "A Revolução dos Bichos", "usuario": "Lucas", "dias_emprestado": 9}]

relatorio = {}

relatorio["livros_mais_de_7_dias"] = [livro["titulo"] for livro in emprestimos if livro["dias_emprestado"] > 7]


livro_mais_tempo = max(emprestimos, key=lambda x: x["dias_emprestado"])
relatorio["livro_mais_tempo"] = livro_mais_tempo["titulo"]

relatorio["usuarios_com_emprestimos"] = list({livro["usuario"] for livro in emprestimos})

total_dias = sum(livro["dias_emprestado"] for livro in emprestimos)

relatorio["media_dias_emprestimo"] = total_dias / len(emprestimos)

for chave, valor in relatorio.items():
    print(f"{chave}: {valor}")
