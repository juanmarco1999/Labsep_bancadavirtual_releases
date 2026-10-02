# Simulador LABSEP

A bancada do **Laboratório de Sistemas de Energia Elétrica (ENE0073)** na sua
máquina: os mesmos equipamentos, os mesmos bornes, os mesmos instrumentos — e
os cabos você pluga um a um, como faz na aula.

![A Figura 2 do Experimento 4 — delta desbalanceado, energizado —, com os três amperímetros de linha um embaixo do outro, como a apostila desenha, os dois wattímetros no borne de 1 A e nenhum cabo por cima de instrumento](img/bancada.png)

**[⬇ Baixar a última versão](../../releases/latest)** · Windows 64 bits · não
pede administrador · funciona sem internet

**Novo na 1.19.4:** as montagens prontas do Experimento 6 ficaram mais fiéis
às figuras — no paralelismo (Figura 3), o V1, o A, o V e o reostato na linha
do T2, como o desenho; no método CA (Figura 2), o V3 com os dois fios pretos;
e o jumper do próprio transformador, no autotransformador e na Figura 2,
dando a volta por fora em vez de cortar o núcleo. A fiação e as leituras são
as mesmas. [O que mudou](../../releases/tag/v1.19.4). Na 1.19.3, o aviso de
falha ao passar o mouse num multímetro recém-chegado e o desfazer que trocava
o número dos multímetros foram corrigidos —
[o que mudou na 1.19.3](../../releases/tag/v1.19.3).

---

## Por que isso existe

A prova prática é numa bancada só, com o tempo contado e o roteiro na mão.
Quem chega sem ter montado antes gasta metade da aula descobrindo onde vai o
amperímetro — e a outra metade desconfiando do número que leu. Aqui dá para
errar à vontade, na véspera, de madrugada, quantas vezes precisar.

Foi feito por um aluno da disciplina, para a turma da disciplina.

## O que dá para fazer

**Montar.** Arraste de um borne a outro para ligar um cabo. Empilhe plugues na
traseira de outro plugue, que é como se faz um nó de três na bancada de
verdade. Escolha a cor do fio, a potência de cada lâmpada, a posição de cada
chave. Nada é "aproximadamente": o que não pode ser ligado não liga, e o que
pode dá exatamente o que daria na mesa. Passe o mouse num borne e tudo o que
está no mesmo nó elétrico acende junto; e «Arrumar a mesa como a figura», embaixo
do seletor, põe a sua montagem na disposição das prontas, com os mesmos cabos —
cada amperímetro de linha na linha dele, mesmo que você os tenha instalado fora
da ordem.

**Ou partir da figura pronta.** São **33 montagens** dos roteiros no seletor,
armadas cabo por cabo como o desenho manda — estrela, delta, equilibrado,
desequilibrado, neutro aterrado, correção de fator de potência, os
transformadores. Serve para estudar a figura e serve para conferir a sua
própria montagem contra ela. Cada instrumento fica no borne e no lugar em que a
figura o põe: os amperímetros de linha dos Experimentos 3 e 4 um embaixo do
outro, o T1 sobre o T2 no paralelismo do Experimento 6, o voltímetro sobre a
primeira lâmpada na Figura 2 do Experimento 1. Nenhum borne de instrumento
vira emenda — a linha se abre em ramos na carga, como na bancada —, e nenhum
cabo passa por cima de visor, mostrador, bocal ou de outro aparelho.

![A Figura 3 do Experimento 6 — dois transformadores em paralelo —, com o T1 sobre o T2 e o A1 sobre o A2, e o V1, o A, o V e o reostato na linha do T2, como o desenho](img/transformadores.png)

**Medir.** Os multímetros são ET-1110B com as faixas do manual: a leitura sai
com a resolução da faixa, mostra `OL` quando estoura e tem a incerteza
declarada. Os wattímetros ENGRO MOD.71 têm o ponteiro, o comutador e o
multiplicador — inclusive o ponteiro parado no batente quando a potência é
negativa, que é o que se vê antes de inverter a bobina. O borne de corrente
importa: no de 5 A o multiplicador é 5 e a leitura anda de 12,5 em 12,5 W, e as
montagens prontas usam o que a apostila manda, a menor escala que aguente a
corrente da bobina. E a chave manda no que
o visor mostra: em V⎓ numa bancada CA ele marca zero — a média de uma senoide
—, e em CC a ponta trocada lê negativo.

**Descobrir onde o instrumento entra.** Botão direito num cabo e o programa diz
qual corrente passa ali com o nome da coluna da tabela: *a corrente de linha da
fase V*, *a corrente de fase do ramo UV*, *a corrente de neutro*. Escolhida uma,
ele abre o cabo e põe o amperímetro em série — que é a manobra que todo mundo
erra na primeira vez —, e mostra o gesto inteiro: a ponta sai do borne, o
aparelho chega, o COM e o 10A encaixam. Voltímetro é pelo borne, e entra em
paralelo sem desfazer nada.

**Preencher as tabelas do relatório.** As **46 tabelas** dos roteiros dos
Experimentos 1 a 7 estão no programa, com dica, conferência célula a célula,
valor revelado quando você desistir e exportação em CSV, Markdown ou PDF.

![As tabelas guiadas, com conferência e exportação](img/tabela.png)

**Saber o que está errado antes de valer nota.** «Analisar montagem» percorre o
circuito e devolve o que fazer, por quê, e em que ordem consertar — são **62
achados** catalogados, cada um com código. O que cada amperímetro mede ele diz
pela ligação, e não pelo número: um amperímetro em série com só uma das lâmpadas
de um ramo sai como «só parte da corrente do ramo», mesmo quando o valor bate
com a corrente inteira de outro ramo. No exemplo abaixo faltava a ligação
do amperímetro: a fase U ficou sem carga (a lâmpada apagada, à esquerda) e o
wattímetro ficou com uma bobina só.

![A análise apontando dois erros, com o conserto e o porquê](img/analise.png)

**Treinar para a prova dos Experimentos 3 e 4.** A aba *Modos* traz **71
exercícios de bancada** em oito grupos — medições, identificação das fases,
montagens, wattímetros, fator de potência, diagnóstico, tabelas e um simulado
da P2. Treinar é montar: 35 deles começam com a bancada limpa e desligada —
varivolts no zero, nenhum cabo, lâmpadas na bandeja, os multímetros da mesa em
OFF —, e os instrumentos saem de uma prateleira no quadro do treino, por
clique ou arrastando até a mesa. Você monta a carga, instala o medidor, regula
a fonte e liga. Os outros começam com o circuito pronto, porque ali a montagem
é a pergunta: os ramos a identificar, o erro plantado, a leitura a
interpretar.

A correção vem quando você pede, e olha o que cada aparelho está medindo pela
ligação, e não pelo número do visor — um amperímetro antes da bifurcação do
delta recebe «isso é corrente de linha». Nada da resposta aparece antes da
tentativa. No guiado há dicas em degraus, até uma demonstração que depois se
desfaz, e as marcas na mesa dizem o que marcam por cor, traço e ícone; no
prático e no simulado — onze tarefas sorteadas, com a nota só na entrega —,
não há dica. As leituras vão para um caderno com o antes e o depois.

O progresso é cobertura de habilidades, não probabilidade de aprovação: cada
item do Exp 3 e do Exp 4 aparece como não iniciado, em treino, consistente ou
dominado, ao lado de onde você está errando e do próximo treino — com o botão
que abre exatamente a variante que falta. Depois de entregar, **Comparar com
referência** alterna a mesa entre a sua montagem e a do roteiro; e a última
categoria da lista abre na bancada a montagem de cada atividade (Exp 3 e Exp 4,
Atividades 1 a 3) só com os medidores do que se quer medir.

«Analisar montagem com IA», nos modos do zero e fora da prova, passa cada
conclusão por um validador que confere contra o que a bancada mede: «está tudo
correto» numa montagem errada não aparece. A consulta à Maritaca de verdade ainda não foi
conferida; sem chave — o caso de quem só instala —, quem responde é a
validação elétrica local, e a tela diz isso.

![A aba Modos: o modo pelo nome, o objetivo sorteado pela semente e, à direita, o progresso por item, onde se está errando e o próximo treino](img/modos.png)

**Treinar do jeito difícil.** A aba *Prova* sorteia uma prova prática e corrige
com nota; o *treino de diagnóstico* esconde um defeito na montagem e pede que
você o encontre medindo — sem olhar o painel, como na bancada.

**E ainda:** animação da tensão e da corrente circulando, diagrama fasorial,
osciloscópio, o ensaio que identifica as fases — tire uma lâmpada com a
bancada ligada e ele diz, pelas leituras, entre quais fases ela estava (na
bancada real, só com autorização do professor) —, uma bandeja para as
lâmpadas que saem do bocal, a lâmpada que se põe rosqueando — o contato só
fecha quando ela assenta —, montagem salva em arquivo `.juan` e relatório em
PDF.

## O que ele cobre

Os **Experimentos 1 a 7** — Blocos 1, 2 e 3:

| Bloco | Experimentos |
|---|---|
| 1 | 1 · cargas em série · 2 · paralelo e fator de potência |
| 2 | 3 · carga em estrela · 4 · carga em delta |
| 3 | 5, 6 e 7 · transformador monofásico, autotransformador e banco trifásico |

Os Experimentos 8 e 9 ainda não estão.

## De onde vêm os números

De um solver de circuitos, não de uma tabela. Cada leitura sai da solução da
malha por análise nodal em fasores — troque uma lâmpada, uma chave ou a tensão
da fonte e a conta é refeita. A lâmpada tem modelo térmico, então a resistência
dela muda com a tensão, e é por isso que três lâmpadas em série não dão um
terço do brilho: dão 15 %.

Os instrumentos entram no circuito como carga de verdade — a bobina de tensão
do wattímetro puxa 220 µA, o voltímetro tem 10 MΩ —, e é por isso que a
corrente de linha não é exatamente √3 vezes a de fase.

## Baixar e instalar

Vá em **[Releases](../../releases/latest)** e pegue um dos dois:

| arquivo | para quê |
|---|---|
| `SimuladorLABSEP_setup.exe` | instala, cria o atalho e associa os arquivos `.juan` |
| `SimuladorLABSEP-X.Y.Z-portatil.zip` | roda sem instalar — descompacte e abra o `.exe` |

A instalação é na pasta do usuário: **não pede administrador** e não mexe no
sistema. São cerca de 95 MB em disco. Instalar por cima de uma versão anterior
preserva ajustes, montagens salvas e calibração.

O programa **não precisa de internet** para nada do que faz — a única coisa que
usa rede é a procura por versão nova, e ela pode ser desligada.

## Ele avisa quando sai versão nova

A partir da 1.15.0 o simulador pergunta aqui, sozinho, no máximo uma vez por
dia, e mostra o que mudou antes de baixar qualquer coisa. Você decide: baixar,
deixar para depois, pular aquela versão ou desligar o aviso de vez. Também dá
para perguntar na hora, pelo menu **Bancada → Procurar atualizações…**

Antes de instalar o que baixou, ele **confere o SHA256** do arquivo contra o
`SHA256.txt` publicado na release. O que não bate é apagado e nada é executado.

## Conferir o download você mesmo

Cada release traz um `SHA256.txt`. No PowerShell:

```powershell
Get-FileHash .\SimuladorLABSEP_setup.exe -Algorithm SHA256
```

O valor tem de ser igual ao da linha correspondente do arquivo.

## O que ele não é

Não substitui a bancada nem a leitura do roteiro impresso: a mesa real tem
contato ruim, plugue solto, professor perguntando e o relógio andando, e nada
disso cabe numa tela. O simulador serve para você chegar à aula sabendo o que
vai fazer.

Também **não é material oficial** da UnB nem do departamento, e não tem vínculo
com eles. É trabalho de aluno, e pode conter erro — se achar um, abra uma
[issue](../../issues) dizendo o que você fez e o que esperava. Isso ajuda a
turma toda.

## Autoria

Feito por **Juan Marco Silva** ([@juanmarco1999](https://github.com/juanmarco1999)),
aluno de Engenharia Elétrica da UnB. Uso acadêmico.

Este repositório existe só para distribuir o programa — aqui ficam o
instalador, a versão portátil e os resumos SHA256 de cada versão. O
código-fonte é privado.
