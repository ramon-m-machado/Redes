# Redes

## OSI
AASTREF

7. Aplicação
6. Apresentação
5. Sessão
4. Transporte
3. Rede
2. Enlace
1. Física

## TCP/IP
4. Aplicação (5, 6 e 7)
3. Transporte (4)
2. Internet (3)
1. Acesso à rede (1 e 2)

# LISTA DE REDES

## 1) o que é atenuação
enfraquecimento do sinal devido à perda de energia.
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/563d24ef-85ba-486d-a077-f64b2859b0f8)

## 2) o que é distorção
mudança no formato devido aos atrasos diferentes em diferentes frequências
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/6ad3f922-46b8-4d9b-a927-678ecbe68b37)

## 3) O que é ruído?
sinais indesejados inseridos entre a transmissão e recepção.

relação sinal ruido = POTENCIA DO SINAL S/ POTENCIA DE RUIDO N

10log10(S/N)
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/95320da5-aec0-43da-a288-c0f43861b0df)

## 4) Quais fatores afetam a capacidade de um canal?
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

## 5) Que tipo de ruído é mais difícil de remover de um sinal digital? Porque?
O ruído impulsivo, porque ele adiciona distorções abruptas e imprevisíveis aos dados, sem seguir um padrão regular (se seguisse, facilitaria filtrá-lo).

## 6) Por que a camada física não tem mecanismos como controle de tráfego e detecção de 
erros?
O intuito da camada física é transmitir e receber bits. Pelo principio da independência das camadas superiores (seguindo o modelo OSI) essa tarefa fica para as camadas de enlace e rede.

## 7) Descreva os três tipos de perdas nas transmissões e os efeitos negativos que eles 
podem proporcionar.
* atenuação: sinal enfraquece à medida que se propaga ( por conta de perda eletrica nos cabos ou dispersão do sinal em fibras ópticas). Efeito negativo: diminuição da qualidade do sinal recebido, erros de transmissão e degradação do desempenho.
* propagação: sinal dispersa à medida que se propaga. comum em transmissões sem fio. Efeito negativo: diminuição da intensidade do sinal recebido e pode interferir na conectividade confiável dos dispositivos.
* interferência: outros sinais afetam a transmissão do sinal principal. Efeito negativo: corrompe e distorce o sinal, resultando em perda de pacote e degradação da qualidade do sinal. Perda na confiabilidade e desempenho.

## 8) Na utilização de um canal para a transmissão de mais de um sinal é utilizada a Banda 
Passante. Quais filtros seriam necessários para separar cada sinal adequadamente?
* Low-Pass Filter: permite passagem de frequências mais baixas que um limite X.
* High-Pass Filter: permite passagem de frequências mais altas  que um limite X.
* Band-Pass Filter: permite a passagem entre um intervalo de frequências.
* Band-Stop Filter: permite a passagem de frequências fora do intervalo.

## 9) Qual seria a taxa máxima de dados de um canal sem ruído de 4KHz utilizando 2 níveis 
de um sinal digital? Se passasse a ser considerado um ruído de 30dB qual seria a taxa 
máxima de dados deste canal
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
 
 ## 10) Os canais de TV têm 6MHz. Quantos bits/s poderiam ser enviados se fosse utilizado um 
sinal digital de 4 níveis sem ruído?
 Utilizando Nyquist:
 C = 2*6.000.000*Log2(4)
 C = 2*6.000.000*log2(4) = 24.000.000 bps

## 11) Quais serviços a Ethernet provê à camada de rede? O padrão 802.3 provê serviços 
diretamente a camada de rede?
Não prove serviços diretamente à camada de rede. Ela fornece serviços à camada de Enlace. Não, o padrão 802.3 não provê serviços diretamente à camada de rede. Ele é focado principalmente na camada de enlace de dados.

## 12) igual a 9

## 13) O Teorema de Nyquist (taxa máxima de dados em um canal sem ruído) também se 
aplica à fibra ótica de alta qualidade de modo único?
Sim. O teorema estabelece que a taxa máxima de transmissão de dados é limitada pela largura de banda, que depende das cracterísticas físicas da fibra ótica.

## 14) Defina espectro eletromagnético e como sua utilização é regulamentada. Identifique 
limitações das faixas liberadas para uso geral.
É o intervalo completo de todas as frequências possíveis de ondas eletromagnéticas. É regulamentado pelos orgãos governamentais responsáveis pelas comunicações, que estabelecem faixas de frequências específicas para diferentes tipos de aplicações.

## 15) Represente graficamente a transmissão da sequência de bits 1100101110111011 
utilizando as modulações digitais NRZ, NRZI e Manchester. Qual seria a sequência de 
bits a ser transmitida utilizando 4B/5B?

Contexto: transformar os dados digitais em analogicos para promover comunicação
(modulação)
## 16) Descreva as modulações digitais: ASK, FSK e PSK, e as alternativas para conseguir 
aumentar a taxa de transferência com base no uso destas técnicas
* ASK altera a amplitude para representar os bits
* FSK altera a frequência para representar os bits
* PSK altera as fases para representar os bits
Para tentar aumentar a taxa de transferência, existe, por exemplo op QPSK, que usa as fazes 0,90,180,270 para representar, respectivamente, 00, 01, 10, 11.
Existem também o QAM, que combina ASK e PSK (maix utilizada) que utiliza 4 fases e 2 amplitudes
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/4b3bc36a-df11-4dd2-8293-a97e6b1f8654)

Contexto: Multiplexação é a transmissão de dois ou mais sinais de informação utilizando o mesmo meio de trasmissão. Objetivo: Maximizar o número de conexões 
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/9983cff5-df0d-4e7b-9cd0-838199c20c4b)
## 17) Descreva as técnicas de multiplexação FDM, TDM e WDM
* FDM: multiplexação por divisão de frequência. Uma faixa de frequência pra cada canal
* ![image](https://github.com/ramon-m-machado/Redes/assets/86575893/16bb96ac-c87a-45eb-9477-bf8c253efff1)

* WDM: por comprimento de onda. Aplicado a fibras oticas. utiliza diferentes comprimentos de onda.
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/82f85115-cd78-46cf-81ef-7744e75173b9)
* TDM: por divisão de tempo. Cada um utiliza toda a largura de banda por um pequeno período.
![image](https://github.com/ramon-m-machado/Redes/assets/86575893/812e15aa-b0cf-4125-8628-a4f297e0cc8a)

*Não foi pedido*
* CDM: por divisão de código. Vetores ortogonais (??)

## 18) Cite alguns possíveis serviços que um protocolo de camada de enlace pode
oferecer à camada de rede?
* Entrega de quadros. Entregar os quadros aos destinos corretos na rede local.
* Endereçamento: usa MAC para identificar os dispositivos na rede local.
* Controle de acesso ao meio: regula o acesso concorrente dos dispositivos ao meio de transmisão compartilhado. Ex CSMA/CD
* Detecção e correção de erros.
* Fragmentação e reagrupamento de pacotes
* Controle de fluxo
* Priorização de tráfego


## 19) Um cabo com 100km de comprimento funciona na taxa de dados T1. A velocidade 
de propagação no cabo é igual a 2/3 da velocidade da luz no vácuo. Quantos bits 
o cabo pode conter?
v_luz =  300.000 km/s
v_t = 200.000 km/s
cabo = 100km

frequencia 
f = 200.000 / 100 = 2.000 Hz
Por Nyquist
C = 2*W*log2(L)
* usando L = 2 (0 ou 1)
C = 2 * 2.000 * log2(2) = 4.000 bps

## 20) Uma LAN CSMA/CD de 10Mbps (não 802.3) com a extensão de 1 km tem uma 
velocidade de propagação de 200m/µ. Não são permitidos repetidores nesse 
sistema. Os quadros de dados têm 256 bits, incluindo 32 bits de cabeçalho, totais 
de verificação e outras formas de overhead. O primeiro slot de bits depois de uma 
transmissão bem-sucedida é reservado para o receptor capturar o canal com o 
objetivo de enviar um quadro de confirmação de 32 bits. Qual será a taxa de 
dados efetiva, excluindo o overhead, se partirmos do princípio de que não há
colisões

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

## 21) Um pacote IP a ser transmitido por uma rede Ethernet tem 60 bytes de 
comprimento, incluindo todos os seus cabeçalhos. Se o LLC não estiver em uso, 
será necessário utilizar preenchimento no quadro Ethernet? Em caso afirmativo, 
de quantos bytes?




## dicionario
* Ethernet é um protocolo de conexão que gerencia como os dispositivos e computadores se comunicam em uma rede local (LAN)

* O padrão 802.3 é um padrão Ethernet que define as especificações físicas e de enlace de dados para redes locais.










