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

