# Trabalho prático da matéria de lógica computacional 1 da UnB
1 Exercícios

1.1 Questão 1
A primeira questão consiste em demostrar que o conjunto de todos inteiros (denotado como fullset[int]) é um conjunto aberto, segundo a definição de Furstenberg.
int_is_open: CONJECTURE open_N_Z?(fullset[int])

1.2 Questão 2
A segunda questão consiste em demonstrar que o conjunto Na,b é um conjunto aberto, segundo a
definição topológica moderna.
Nab_open: CONJECTURE open?(N(a)(b))

1.3 Questão 3
A terceira questão consiste em provar que para todo n ∈ N, n 6= 1, existe um primo que o divide.
Aqui será necessário usar os lemmas da teoria “divides” do prelúdio de PVS.
Lembrete: para examinar o arquivo do prelúdio usa-se o comando de linha M-x view-preludefile (ou, M-x vpf). Também é possível pesquisar por uma teoria específica do prelúdio usando M-x
vpt + nomeTeoria ou M-x view-prelude-theory + nomeTeoria. Onde M-x é Alt+x no Linux e
Option+x no Mac.
open_prime_decomposition_ind: CONJECTURE
FORALL (n:nat) : n /= 1 IMPLIES EXISTS(p:(prime?)): divides(p, n)

1.4 Questão 4
Finalmente, a quarta e última questão deve-se provar, por meio da teoria inf prime topology, a
infinitude dos primos. Esta questão irá requerer as instanciação de lemmas dessa teoria (não
necessáriamente da mesma seção).
Dicas, há lemmas que serão instanciados com o conjunto ”{x:int| x = 1 OR x = -1}”e será
util usar o lemma ”closed complement”, durante a prova.
prime_set_is_infinite: CONJECTURE
is_infinite(fullset[(prime?)])
