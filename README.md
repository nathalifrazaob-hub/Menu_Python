# ----- MENUS -----
estudantes = (
    "(1) Incluir.\n"
    "(2) Listar.\n"
    "(3) Atualizar.\n"
    "(4) Excluir.\n"
    "(5) Menu Principal."
)

professores = (
    "(1) Incluir.\n"
    "(2) Listar.\n"
    "(3) Atualizar.\n"
    "(4) Excluir.\n"
    "(5) Menu Principal."
)

disciplinas = (
    "(1) Incluir.\n"
    "(2) Listar.\n"
    "(3) Atualizar.\n"
    "(4) Excluir.\n"
    "(5) Menu Principal."
)

turmas = (
    "(1) Incluir.\n"
    "(2) Listar.\n"
    "(3) Atualizar.\n"
    "(4) Excluir.\n"
    "(5) Menu Principal."
)

matriculas = (
    "(1) Incluir.\n"
    "(2) Listar.\n"
    "(3) Atualizar.\n"
    "(4) Excluir.\n"
    "(5) Menu Principal."
)

menu = (
    "(1) Gerenciar estudantes.\n"
    "(2) Gerenciar professores.\n"
    "(3) Gerenciar disciplinas.\n"
    "(4) Gerenciar turmas.\n"
    "(5) Gerenciar matrículas.\n"
    "(0) Sair."
)

# ----- FUNÇÃO PARA MOSTRAR MENU DE OPERAÇÕES -----
def mostrar_menu_operacoes(titulo, opcao):
    print(f"*** [{titulo}] MENU DE OPERAÇÕES ***")
    print(opcao)
    print()
    input("Informe a ação desejada (pressione Enter para voltar ao menu): ")
    print()

# ----- LOOP PRINCIPAL -----
while True:
    print("----- MENU PRINCIPAL -----\n")
    print(menu)
    
    try:
        resp = int(input("\nInforme a ação desejada: "))
    except ValueError:
        print("\nPor favor, digite um número válido.\n")
        continue

    print()  # Pular linha

    if resp == 1:
        mostrar_menu_operacoes("ESTUDANTES", estudantes)
    elif resp == 2:
        mostrar_menu_operacoes("PROFESSORES", professores)
    elif resp == 3:
        mostrar_menu_operacoes("DISCIPLINAS", disciplinas)
    elif resp == 4:
        mostrar_menu_operacoes("TURMAS", turmas)
    elif resp == 5:
        mostrar_menu_operacoes("MATRÍCULAS", matriculas)
    elif resp == 0:
        print("Saindo do programa...")
        break
    else:
        print("Opção inválida. Tente novamente.\n")
