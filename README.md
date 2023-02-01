# Trabalho-Automato
Neste repositório encontra-se meu trabalho sobre automatos finitos deterministico
Abaixo colocarei  encontra-se um dos meus 3 codigos 

def afd(Q, Sigma, delta, q0, F, cadeia):
    qA = q0
    for s in cadeia:
        qA = delta[(qA, s)]
    return qA in F


delta = {('q0', '0'): 'q0', ('q0', '1'): 'q1', ('q1', '0'): 'q0', ('q1', '1'): 'q1'}

Q = ['q0', 'q1']

F = ['q0']

Sigma = ['0', '1']

afd(Q, Sigma, delta, 'q0', F, '0000')

Automato que nao termina com o numeral 1
Este código recebe todas as informações a respeito de um automato finito deterministico e nos devolva uma linguagem reconhecida pelo automato.
Criou-se uma função afd que deve saber quais os estados o alberto a funçao de transiçao o estado inicial os estados finais e a cadeia.
O automato possui sempre um estado ativo e inicial, que vai ler a cadeia e passar por cada simbolo tomando uma decisão e passando para o próximo estado. O próximo estado ativo vai ser o delta que vai receber o estado ativo atual e o símbolo atual. Utilizando do return para verificar se qA vai estar entre o conjunto de estados finais determinado pelo automato.
Utilizei um automato que pede uma cadeia que termine necessariamente com zero .
-delta vai receber o estado e o simbolo
-F vai receber o estado final, que nesse teste é o q0 
-No ultimo algoritmo afd vai haver a checagem se o automato vai recenhecer ou nao esta linguagem
