# Python
# Projeto de automação de tarefas - Acadêmico 
#   Listando as etapas do processo
task 1: Open the site of the company - abrir o site da empresa

task 2: Sign in the site - fazer login

task 3: Import the base data of the products

task 4: Register 1 product - cadastrar um produto

task 5: Doing again until over the products

    # CÓDIGO NA LINGUAGEM PYTHON
    
    # import pandas
    
    # import pyautogui
    # import time
    task 1 - Abrindo o site da empresa
    
    pyautogui.PAUSE = 1.3
    # abrindo/apertando a tecla windowns
    pyautogui.press('win')
    # escrevendo a busca do navegador (chrome no caso)
    pyautogui.write('chrome')
    # apertar a tecla enter
    pyautogui.press('enter') 
    time. sleep(2)
    # https://dlp.hashtagtreinamentos.com/python/intensivao/login
    pyautogui.write('https://dlp.hashtagtreinamentos.com/python/intensivao/login')
    # apertar a tecla enter
    pyautogui.press('enter')
    
    # para fazer pausas especificas no meio do cod
    time.sleep(3)
    
    # task 2 - login
    pyautogui.click(x=680, y=512)
    pyautogui.write('albertof469@gmail.com')
    
    pyautogui.press('tab')  # foi para campo da senha
    pyautogui.write('Al041095')
    
    pyautogui.press('tab')  # campo 
    pyautogui.press('enter')  # fazer login 
    
    # Task 3 importar a base de dados dos produtos (pandas, openpyxl)
    tabela = pandas.read_csv('produtos.csv')
    print(tabela)

    # Task 4 - cadastrar um produto
    time.sleep(2)

    # task 5 Repetir até os produtos acabarem 
    for linha in tabela.index: # index são as linhas da tabela
    pyautogui.click(x=808, y=366)

    # codigo
    codigo = tabela.loc[linha, 'codigo']
    pyautogui.write(str(codigo))
    pyautogui.press('tab')

    # marca
    marca = tabela.loc[linha, 'marca']
    pyautogui.write(str(marca))
    pyautogui.press('tab')

    # tipo
    tipo = tabela.loc[linha, 'tipo']
    pyautogui.write(str(tipo))
    pyautogui.press('tab')

    # categoria
    categoria = tabela.loc[linha, 'categoria']
    pyautogui.write(str(categoria))
    pyautogui.press('tab')

    # preço unitario
    preco_unitario = tabela.loc[linha, 'preco_unitario']
    pyautogui.write(str(preco_unitario))
    pyautogui.press('tab')

    # custo
    custo = tabela.loc[linha, 'custo']
    pyautogui.write(str(custo))
    pyautogui.press('tab')

    # observação
    obs = str(tabela.loc[linha, 'obs'])
    if obs != 'nan':
        pyautogui.write(obs)
    pyautogui.press('tab')

    pyautogui.press('enter')

    pyautogui.scroll(1000) # + scroll para cima/ - sroll para baixo 
