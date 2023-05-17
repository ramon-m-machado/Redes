## Link do gitHub (para ver as imagens)
https://github.com/ramon-m-machado/Redes


# LISTA DE REDES

### 1) o que é atenuação
enfraquecimento do sinal devido à perda de energia.

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/66280d9a-d8ab-4e26-9bf3-b135344aeb5f)


### 2) o que é distorção
mudança no formato devido aos atrasos diferentes em diferentes frequências

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/ac68482a-3a9f-4661-83c2-e2ba9b1cd670)


### 3) O que é ruído?
sinais indesejados inseridos entre a transmissão e recepção.

relação sinal ruido = POTENCIA DO SINAL S/ POTENCIA DE RUIDO N

10log10(S/N)

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/07397213-a63c-4571-997b-c81a5da2b775)


### 4) Quais fatores afetam a capacidade de um canal?
* largura de banda;
* ruído;
* atenuação;
* interferência;
* protocolos de comunicação;
* qualidade de equipamentos;

Obs.:
* largura de banda: diferença entre maior e menor frequência que pode ser utilizada para transmissão de um sinal em um meio físico
* interferência: A interferência é causada pela presença de outros dispositivos ou sinais que compartilham o mesmo meio de transmissão.
* protocolos de comunicação: alguns são mais eficientes e aproveitam melhor a largura de banda.
* qualidade de equipamentos: qualidade de roteadores, switches, cabos, etc.


### 5) Que tipo de ruído é mais difícil de remover de um sinal digital? Porque?O ruído impulsivo, porque ele adiciona distorções abruptas e imprevisíveis aos dados, sem seguir um padrão regular (se seguisse, facilitaria filtrá-lo).


### 6) Por que a camada física não tem mecanismos como controle de tráfego e detecção de erros?
O intuito da camada física é transmitir e receber bits. Pelo principio da independência das camadas superiores (seguindo o modelo OSI) essa tarefa fica para as camadas de enlace e rede.


### 7) Descreva os três tipos de perdas nas transmissões e os efeitos negativos que eles podem proporcionar.
* atenuação: sinal enfraquece à medida que se propaga ( por conta de perda eletrica nos cabos ou dispersão do sinal em fibras ópticas). Efeito negativo: diminuição da qualidade do sinal recebido, erros de transmissão e degradação do desempenho.
* propagação: sinal dispersa à medida que se propaga. comum em transmissões sem fio. Efeito negativo: diminuição da intensidade do sinal recebido e pode interferir na conectividade confiável dos dispositivos.
* interferência: outros sinais afetam a transmissão do sinal principal. Efeito negativo: corrompe e distorce o sinal, resultando em perda de pacote e degradação da qualidade do sinal. Perda na confiabilidade e desempenho.


### 8) Na utilização de um canal para a transmissão de mais de um sinal é utilizada a Banda Passante. Quais filtros seriam necessários para separar cada sinal adequadamente?
* Low-Pass Filter: permite passagem de frequências mais baixas que um limite X.
* High-Pass Filter: permite passagem de frequências mais altas  que um limite X.
* Band-Pass Filter: permite a passagem entre um intervalo de frequências.
* Band-Stop Filter: permite a passagem de frequências fora do intervalo.


### 9) Qual seria a taxa máxima de dados de um canal sem ruído de 4KHz utilizando 2 níveis de um sinal digital? Se passasse a ser considerado um ruído de 30dB qual seria a taxa máxima de dados deste canal
 Utilizando Nyquist:
 C = 2*W*Log2(L)
 C = 2*4000*log2(2) = 8000 bps
 
 Com ruído:
 30db => 10*log10(S/N) = 30
 => Log10(S/N) = 3
 => S/N = 1000
 
 Por Shannon: (independe do numero discreto de níveis)
  C = Wlog2(1+S/N) bps
  C = 4000* log2(1001)
  C = 4000* 9,967 bps ~= 40000 bps
 
 
### 10) Os canais de TV têm 6MHz. Quantos bits/s poderiam ser enviados se fosse utilizado um sinal digital de 4 níveis sem ruído?
 Utilizando Nyquist:
 C = 2*6.000.000*Log2(4)
 C = 2*6.000.000*log2(4) = 24.000.000 bps


### 11) Quais serviços a Ethernet provê à camada de rede? O padrão 802.3 provê serviços diretamente a camada de rede?
Não prove serviços diretamente à camada de rede. Ela fornece serviços à camada de Enlace. Não, o padrão 802.3 não provê serviços diretamente à camada de rede. Ele é focado principalmente na camada de enlace de dados.


### 12) igual a 9


### 13) O Teorema de Nyquist (taxa máxima de dados em um canal sem ruído) também se aplica à fibra ótica de alta qualidade de modo único?
Sim. O teorema estabelece que a taxa máxima de transmissão de dados é limitada pela largura de banda, que depende das cracterísticas físicas da fibra ótica.


### 14) Defina espectro eletromagnético e como sua utilização é regulamentada. Identifique limitações das faixas liberadas para uso geral.
É o intervalo completo de todas as frequências possíveis de ondas eletromagnéticas. É regulamentado pelos orgãos governamentais responsáveis pelas comunicações, que estabelecem faixas de frequências específicas para diferentes tipos de aplicações.


### 15) Represente graficamente a transmissão da sequência de bits 1100101110111011 utilizando as modulações digitais NRZ, NRZI e Manchester. Qual seria a sequência de bits a ser transmitida utilizando 4B/5B?

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/fa30ecd5-ed23-49c7-b514-4f599270a544)


Contexto: transformar os dados digitais em analogicos para promover comunicação
(modulação)

## 16) Descreva as modulações digitais: ASK, FSK e PSK, e as alternativas para conseguir aumentar a taxa de transferência com base no uso destas técnicas
* ASK altera a amplitude para representar os bits
* FSK altera a frequência para representar os bits
* PSK altera as fases para representar os bits
Para tentar aumentar a taxa de transferência, existe, por exemplo op QPSK, que usa as fazes 0,90,180,270 para representar, respectivamente, 00, 01, 10, 11.
Existem também o QAM, que combina ASK e PSK (maix utilizada) que utiliza 4 fases e 2 amplitudes

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/8cdb286e-b8b2-4422-a962-22559bc579c4)


Contexto: Multiplexação é a transmissão de dois ou mais sinais de informação utilizando o mesmo meio de trasmissão. Objetivo: Maximizar o número de conexões 
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/07b2b8ca-7a90-46ed-a9b8-99ad1cf9bcd0)

### 17) Descreva as técnicas de multiplexação FDM, TDM e WDM
* FDM: multiplexação por divisão de frequência. Uma faixa de frequência pra cada canal

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/470c8c21-2ce1-4af0-affd-4028b084f005)

* WDM: por comprimento de onda. Aplicado a fibras oticas. utiliza diferentes comprimentos de onda.

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/a59e3219-516d-416f-aa86-13da1e2f53f0)

* TDM: por divisão de tempo. Cada um utiliza toda a largura de banda por um pequeno período.

![image](https://github.com/ramon-m-machado/Redes/assets/86575893/c7ae6663-e08a-46c4-9cca-608cbf04bed3)

*Não foi pedido*
* CDM: por divisão de código. Vetores ortogonais (??)


### 18) Cite alguns possíveis serviços que um protocolo de camada de enlace pode oferecer à camada de rede?
* Entrega de quadros. Entregar os quadros aos destinos corretos na rede local.
* Endereçamento: usa MAC para identificar os dispositivos na rede local.
* Controle de acesso ao meio: regula o acesso concorrente dos dispositivos ao meio de transmisão compartilhado. Ex CSMA/CD
* Detecção e correção de erros.
* Fragmentação e reagrupamento de pacotes
* Controle de fluxo
* Priorização de tráfego


### 19) Um cabo com 100km de comprimento funciona na taxa de dados T1. A velocidade de propagação no cabo é igual a 2/3 da velocidade da luz no vácuo. Quantos bits o cabo pode conter?
v_luz =  300.000 km/s
v_t = 200.000 km/s
cabo = 100km

frequencia 
f = 200.000 / 100 = 2.000 Hz
Por Nyquist
C = 2*W*log2(L)
* usando L = 2 (0 ou 1)
C = 2 * 2.000 * log2(2) = 4.000 bps

### 20) Uma LAN CSMA/CD de 10Mbps (não 802.3) com a extensão de 1 km tem uma velocidade de propagação de 200m/µ. Não são permitidos repetidores nesse sistema. Os quadros de dados têm 256 bits, incluindo 32 bits de cabeçalho, totais de verificação e outras formas de overhead. O primeiro slot de bits depois de uma transmissão bem sucedida é reservado para o receptor capturar o canal com o objetivo de enviar um quadro de confirmação de 32 bits. Qual será a taxa de dados efetiva, excluindo o overhead, se partirmos do princípio de que não há colisões

* LAN CSMA/CD é uma rede de broadcast implementada através de hardware
* F = 10Mbps
* tamanho = 1km
* v = 200m/s
* quadros: 256 bits, sendo 32 de cabeçalho, então são 224 de informação
* quadro de confirmação 32 bits

Por Nyquist
C = 2*W*log2(L)
C = 2 * 10.000 * log2(256) = 160.000 bps

porém, como a cada transmissão bem sucedida ele envia um quadro de verificação, a frequência deve cair pela metade, sendo 80.000 bps


### 21) Um pacote IP a ser transmitido por uma rede Ethernet tem 60 bytes de comprimento, incluindo todos os seus cabeçalhos. Se o LLC não estiver em uso, será necessário utilizar preenchimento no quadro Ethernet? Em caso afirmativo, de quantos bytes?
Sim, será necessário utilizar preenchimento no quadro Ethernet. Serão necessários 4 bytes de preenchimento para atingir o tamanho mínimo de 64 bytes.


### 22) Os quadros Ethernet devem ter pelo menos 64 bytes para garantir que o transmissor ainda estará ativo na eventualidade de ocorrer uma colisão na extremidade remota do cabo. O tamanho mínimo de quadro nas redes com cabeamento Fast Ethernet também é de 64 bytes, mas esse cabeamento é capaz de transportar o mesmo número de bits com uma velocidade 10 vezes maior. Como é possível manter o tamanho mínimo de quadro?
O tamanho mínimo de quadro de 64 bytes é mantido em redes com cabeamento Fast Ethernet através da adição do preâmbulo e sincronização no início de cada quadro. Isso permite que o transmissor ainda esteja ativo na eventualidade de ocorrer uma colisão na extremidade remota do cabo.


### 23) Lembre-se de que, com o protocolo CSMA/CD, o adaptador espera Kx512 tempos de bits após uma colisão, onde K é escolhido aleatoriamente. Para K=100, quanto tempo o adaptador espera até voltar a etapa 2 para uma rede Ethernet 10Mbps? E para uma rede Ethernet de 100Mbps?
Para uma rede Ethernet de 10Mbps, em que K=100, o adaptador espera 100x512 = 51,200 tempos de bits após uma colisão antes de voltar à etapa 2.

Para uma rede Ethernet de 100Mbps, a velocidade é 10 vezes maior. Portanto, o adaptador ainda espera Kx512 tempos de bits após uma colisão. Nesse caso, seria 100x512 = 51,200 tempos de bits também.

Em ambos os casos, o adaptador espera 51,200 tempos de bits antes de voltar à etapa 2 após uma colisão.


### 24) Suponha que os nós A e B estejam no mesmo segmento de uma Ethernet de 10 Mbps e que o atraso de propagação entre dois nós seja de 225 tempos de bit. Suponha também que A e B enviem quadros ao mesmo tempo, que os quadros colidam e que, então, A e B escolham valores diferentes de K no algoritmo CSMA/CD. Admitindo que nenhum outro nós estejam ativos, as retransmissões de A e B podem colidir? Para nossa finalidade, é suficiente resolver o seguinte exemplo. Suponha que A e B comecem a transmitir em t=0 tempo de bit. Ambos detectam colisões em t=225 tempos de bit. Eles terminam de transmitir um sinal de reforço de colisão em t=225+48 = 273 tempos de bit. Suponha que KA=0 e KB=1. Em que tempo B programa sua retransmissão? Em que tempo A começa a transmissão? (nota: os nós devem esperar por um canal ocioso após retornar à etapa 2). Em que tempo o sinal de A chega a B? B se abstém de transmitir em seu tempo programado
No exemplo dado, após a colisão entre os nós A e B em uma Ethernet de 10 Mbps, B programa sua retransmissão para ocorrer em t=785 tempos de bit, enquanto A começa a transmitir em t=1010 tempos de bit, levando em consideração o tempo de propagação de 225 tempos de bit entre os nós.


#### 25) Considere uma Ethernet 100BaseT de 100Mbps. Considerando que a velocidade de transmissão do meio é 1,8.108 m/se, e o comprimento dos quadros é de 64 octetos e que não há repetidores, para se ter uma eficiência de 0,50, qual deve ser a distância máxima entre um nó e o hub? Essa distância máxima também garante que um nó transmissor A poderá detectar se outro nó transmitiu enquanto A estava transmitindo? Justifique sua resposta. Como se compara sua distância máxima com a estabelecida pelo próprio padrão de 100Mbps.
Para alcançar uma eficiência de 0,50 em uma Ethernet 100BaseT de 100 Mbps, não é necessário tempo de bits de controle. A distância máxima entre um nó e o hub é de até 100 metros, conforme o padrão Ethernet. Essa distância garante a detecção de colisões, pois os nós transmissores podem monitorar o meio durante a transmissão.






