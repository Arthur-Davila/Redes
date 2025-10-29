Plano de controle cria a tabela e é utilizada pelo plano de dados

plano de repasse está dentro do plano de dados

De que forma as tabelas são calculadas:
algoritimos de rotiamento;
ele recebe um grafo e os nós são os roteadores;
ele vai procurar o melhor caminho:
o caminho de menor custo(quem atribui o custo é o adm da rede)

para fazdr a escolha de menor custo:
TRADICONAL
controle por roteador :(cada roteador executa uma parte do plano de controle) o roteador toma a decisão
CADA ROTEADOR TERIA QUE MANDAR UM BROADCAST PARA TODO MUNDO PARA VER TUDO
o roteador ele 
complexidade grande no head
n²

controle logicamento localizado:
Ele pega o numero entre 1 e n e distribui fisicamente
ele distribui em alguns nós ele troca informações entre controladores e os controladores pegam informações 
exemplo :(6 nós e 2 controladores 1 controlador pega informação de 3 e se comunica com outro controlador que pega dos outros 3 restantes )
TOMA MELHORES DECISÕES
função de controle ????

--------------------------

CA agente de controle -> responsavel por entregar  dados para a camada de controle
CADA ROTEADOR SDN tem que TER o CA

cada roteador sdn consegue instanciar funções de rede neles

openflow -> protocolo de gerencia os roteadores


rede tradicional vai ter só o menor caminho

tabela de repasse da um caminho só

repasse generalizado ao inves de só olhar o destino olha mais variaveis


south bound :
plano de dados -> executa o software do plano de controle

offbound:
plano de controle -> define as e repassa regras de software para a rede

Ncast -> mensagem para qualquer um de um grupo

----------------------------------------------------
Algoritmos de Roteamento:

1 - Realiza a descoberta de um bom caminho (menor custo)
2 - Passivel a intervenção politica (Regras de negocios)

Sempre menor custo
Custos:
-Largura de banda->quanto maior melhor(taxa para mandar dados)
-Latencia
-Saltos


Classificado:
quanto a execução:
    algoritimo de roteamento global:
        i-Algoritms de estado de enlase(Link-state: LS) -> Usa o broadcast global
            OSPF - LINK- STATE
    algoritimos desentralizados: 
        RIP
quanto a operação:
    algoritimos de roteamentos estaticos:
        o repasse não muda sem ser manualmente
    algoritimos de roteamentos dinamicos:
        o repasse muda dinamicamente 

quanto a sensibilidade:
    algoritimos sensiveis a carga:
        algoritmos sensiveis a carga olha o trafico da rede para fazer a tabela de repasse
    algoritimos insensiveis a carga:
        não verifica a carga para fazer a tabela de repasse

LS-> O(N²)
    Usado em rede pequenas 
    DYSKTRA -> algoritmo que usa uma busca em profundidade para achar o menor caminho

Algoritimo de vetor de distancia (DV) ou HEAP->
    Trata-se de um algoritimo 
    1-iterativo
    2-assincrono
    3-distribuido

    cada roteador faz a propagação de cada tabela 
    ele compara com os vizinhos
    é feito de 30 em 30 segundos
    faz a convergencia com os repasses e atualizam
    15 SALTOS é o limite
    custos de enlaces até seus vizinhos
    as informações desses vizinhos

DV x LS
    No DV cada nó conversa apensa com seus vizinhos

    No LS, informações são necessarios 

Na internet utiliza o BGP ->
    na internet não vale a pena mandar um brodcast para todo mundo,

roteamento hieraquico:
    -escala
    -autonomia administrativa
    sistema autonomo = designados pelo ICANN

roteamento intra AS: OSPF
    acronimo para open shortest path first
    -é um protocolo LS
    provedor de serviço contem um AS
    AS -> formados de um conjuntos de roteadirs