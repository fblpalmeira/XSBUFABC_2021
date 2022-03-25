# [X Semana da Biologia UFABC - 2021](https://sites.google.com/view/x-semana-da-biologia-ufabc/xsbioufabc)
<img src="https://github.com/fblpalmeira/XSBUFABC_2021/blob/main/img/UFABC_logos.png" align="right" width = "250px"/>

A X Semana da Biologia UFABC foi um evento realizado de 12 a 23 de Julho de 2021.

## [Minicurso: Análise e visualização de dados de biodiversidade no R (12 horas)](https://sites.google.com/view/x-semana-da-biologia-ufabc/minicursos?authuser=0#h.aobl38szjvvm)
### Francesca B. L. Palmeira
<img src="https://github.com/fblpalmeira/XSBUFABC_2021/blob/main/img/UFABC_minicurso.png" align="right" width = "500px"/>

EMENTA: Este curso tem como objetivo oferecer um treinamento prático no uso da linguagem de programação R com a finalidade de: i) analisar dados de biodiversidade; ii) gerar modelos ecológicos dentro de três níveis de organização biológica (organismos/indivíduos, populações e comunidades); iii) visualizar dados construindo figuras e gráficos de alto impacto visual; iv) interpretar os resultados; e, v) discutir as aplicações biológicas das análises e dos modelos. O conteúdo programático inclui a: i) realização de análises exploratórias, ii) introdução à diferentes famílias de modelos ecológicos aplicados a armadilhas de captura, armadilhamento fotográfico, transectos lineares, coleta de fezes, coleta de animais mortos (predados ou atropelados), telemetria, dados de museu, pontos de contagem, parcelas de amostragens, entre outros métodos de coleta; iii) preparação de dados (input) específica para cada análise e modelo; iv) seleção e o ajuste de cada modelo utilizando as inferências da Estimativa da Máxima Verossimilhança (MLE – Maximum Likelihood Estimation) e Bayesiana; e, v) visualização gráfica de dados, interpretação dos resultados (output) e suas aplicações biológicas. Para a realização dos exercícios práticos, é recomendável que cada participante utilize um computador (desktop ou laptop) ao invés de um celular. Não será necessário fazer a instalação do R no computador uma vez que utilizaremos o RStudio Cloud, uma versão online. Não é necessário ter conhecimento prévio de R ou estatística. Será oferecido um tutorial com o passo a passo de todos os exercícios realizados durante o curso.

PÚBLICO-ALVO: Estudantes de graduação, pós-graduação e profissionais com interesse em análise e visualização de dados de biodiversidade.

PRÉ-REQUISITOS: Sem pré-requisito

CRITÉRIOS DE SELEÇÃO: 1) Priorizar grupos subrepresentados no uso do R (ex. mulheres cis, mulheres trans, pessoas não-binárias, pessoas de baixa renda e/ou pessoas que se auto declarar como parte de grupos subrepresentados) - critérios utilizados pelas RLadies; 2) Ordem de inscrição.

JUSTIFICATIVA: O avanço tecnológico dos últimos anos facilitou o nosso acesso a equipamentos modernos de campo e a ferramentas gratuitas para a análise de dados. Aliado a este fato, existe uma quantidade enorme de dados de biodiversidade disponíveis em diversos repositórios online. Desta forma, o uso da linguagem R tem sido extremamente útil para analisar e visualizar toda essa quantidade de dados disponíveis, além de possibilitar maior transparência e reprodutibilidade no processo de análise.

## AULA 1 - DIA 20/07/2021

INTRODUÇÃO:

- [Apresentação do curso `.pdf`](https://github.com/fblpalmeira/XSBUFABC_2021/blob/main/doc/Aula1_Intro_Minicurso_XSemBio_UFABC_2021.pdf)

- [Introdução rápida ao R `.pdf`](https://github.com/fblpalmeira/XSBUFABC_2021/blob/main/doc/Aula1_Intro_R_for_Mac_Fran_UFABC_2021-compactado.pdf)

Exercício: A minha vida em um gráfico de waffle: Aprendendo a usar o RStudio Cloud fazendo um exercício para visualizar a sua vida em um gráfico de waffle. 

- [Tutorial do RStudio Cloud `.pdf`](https://github.com/fblpalmeira/XSBUFABC_2021/blob/main/doc/Exercicio1_Waffle_RStudioCloud_Fran_UFABC_2021.pdf)

AULA TEÓRICA: Introdução a estrutura e a dinâmica de redes de interações tróficas .

- [Aula teórica 1 - Modelos de comunidades `.pdf`](https://github.com/fblpalmeira/XSBUFABC_2021/blob/main/doc/Aula1_ModelosComunidades_Fran_XSemBio_UFABC_2021.pdf)

PRÁTICA 1 - Redes ecológicas multipartida: O objetivo desta prática é construir uma representação gráfica tridimensional (3D) da rede de interação trófica entre uma espécie de predador de topo com espécies de mesopredadores e de presas utilizado o pacote ‘foodweb’ [(Perdomo 2015)](https://cran.r-project.org/web/packages/foodweb/foodweb.pdf). Utilizaremos uma matriz binária simétrica de interação trófica entre a onça-pintada e outros mamíferos, carnívoros e herbívoros, utilizando dados da literatura compilados por [(Palmeira 2015)](https://www.teses.usp.br/teses/disponiveis/11/11150/tde-17092015-111206/publico/Francesca_Belem_Lopes_Palmeira_versao_revisada.pdf), onde 0 representa que o predador de topo não-consumiu a espécie de meso ou de presa e 1 consumiu (Tabela 1). Desta forma, é possível estimar a riqueza de espécies, a conectância, o número e a densidade de links, o número de níveis tróficos, o nível trófico de cada espécie, a fração de espécies de herbívoros, onívoros e de topo e a razão entre predador e presa. As espécies que consumiram aquelas espécies de nível trófico basal (herbívoros) foram classificadas no nível trófico 1. As que consumiram as espécies de nível 1 foram classificadas no nível 2, e assim sucessivamente até o nível do predador de topo, neste caso, formado pela espécie que não foi consumida por nenhuma outra (Figura 2). 

- [Código `.R`](https://github.com/fblpalmeira/foodweb/blob/main/jaguar_foodweb.R)

- [Planilha `.csv`](https://github.com/fblpalmeira/foodweb/blob/main/jaguar_foodweb.csv)

<img src="https://github.com/fblpalmeira/foodweb/blob/main/jaguar_foodweb.gif">

Rede trófica bipartida 2D: O objetivo deste exercício é construir uma rede de interação bipartida utilizado o pacote ‘bipartite’ [(Dormann et al 2021)](http://cran.r-project.org/web/packages/bipartite/bipartite.pdf). Também é possível estimar o padrão de conectividade entre predadores e presas (interações observadas e possíveis), o grau de conectância e a sua distribuição, o quanto as espécies interagem, qual a força desta interação, como as interações se sobrepõem e se agrupam, qual o papel das espécies (espécies hub da rede, hub do módulo, conectoras e/ou periféricas) e quais os aspectos ecológicos mais importantes para a estrutura e a dinâmica da rede. Para isto, criamos uma matriz binária assimétrica de interação trófica entre as espécies, onde 1 representou o consumo da espécie e 0 o não-consumo (Tabela 2). O número de interações foi 32, 28 e 23 para a onça-pintada, a onça-parda e a jaguatirica, respectivamente. O grau variou de 1 a 3, sendo que quatro espécies de grande porte apresentaram grau 1 porque foram consumidas apenas pelo predador de topo. As espécies de pequeno porte apresentaram grau 3 porque foram consumidas pelo predador de topo e também pelos mesopredadores. 

- [Código `.R`]()

- [Planilha `.csv`]()

## AULA 2 - DIA 21/07/2021

AULA TEÓRICA: Introdução aos modelos populacionais que incorporam o viés da detecção imperfeita (processos observacionais) para estimar a ocorrência, a abundância e a densidade de espécies da fauna.

- [Aula teórica 2 - Modelos populacionais `.pdf`](https://github.com/fblpalmeira/XSBUFABC_2021/blob/main/doc/Aula2_ModelosPopulacionais_Fran_XSemBio_UFABC_2021.pdf)

PRÁTICA 2 - Modelo de ocupação: O objetivo desta prática é estimar a ocorrência de espécies incorporando o viés da detecção imperfeita.

O objetivo deste esxercício é estimar a probabiliade de ocorrência de espécies utilizando o pacote ‘unmarked’ [(Fiske & Chandler 2011)](http://www.jstatsoft.org/v43/i10/paper). Este modelo incorpora a probabilidade de detecção (p) da espécie, minimizando o viés da detecção imperfeita em função de covariáveis do sítio e da observação. Utilizaremos os dados de armadilhamento de cateto na Amazônia como estudo de caso. Criamos um histórico binário de detecção para cada espécie (detectada = 1 e não-detectada = 0). A partir deste histórico, criamos um modelo de ocorrência (y) para descrever o efeito de covariáveis sobre a distribuição dos catetos nas áreas amostradas [(Mackenzie et al 2017)](https://books.google.com.br/books?hl=pt-BR&lr=&id=hs2cBAAAQBAJ&oi=fnd&pg=PP1&dq=ackenzie+DI,+Nichols+JD,+Royle+JA,+Pollock+KH,+Bailey+LL,+Hines+JE.+2006.&ots=-YchUeaAuX&sig=_kbFkM0CVDDrg8SU2rShw_g4JnM#v=onepage&q=ackenzie%20DI%2C%20Nichols%20JD%2C%20Royle%20JA%2C%20Pollock%20KH%2C%20Bailey%20LL%2C%20Hines%20JE.%202006.&f=false). As covariáveis selecionadas para estimar a ocorrência e a detecção de catetos foram as do sítio e as da observação (Tabela 2). A função de máxima verossimilhança indicou os modelos de melhor performance baseado no Critério de Informação Akaike (AIC) com delta menor que dois (D<2) e maior peso de evidência (w). Para dar suporte aos melhores modelos, os mesmos foram considerados dentro de um intervalo de confiança (IC) de 95% (Burnham e Anderson, 2002).  

- [Código `.R`]()

- [Planilha `.csv`]()

## AULA 3 - DIA 22/07/2021

AULA TEÓRICA: Introdução aos modelos de movimento animal utilizando dados de telemetria.

- [Aula teórica 3 - Movimento animal `.pdf`]()

PRÁTICA 3 - Visualização (GIF) do movimento animal: O objetivo desta prática é visualizar o movimento animal de indivíduos de onça-pintada (Panthera onca) monitorados no Pantanal utilizando os dados do "Jaguar Movement Database" [(Morato el al 2018)](http://doi.org/10.1002/ecy.2379). Para visualizar o deslocamento dos animais é utilizado o pacote ‘moveVis’ (Schwalb-Willmann 2019) que irá gerar o vídeo de animação do movimento espaço-temporal dos indivíduos (GIF).

- [Código `.R`](https://github.com/fblpalmeira/movevis/blob/main/jaguar_pantanal_saobento_2008.R)

- [Planilha `.csv`](https://github.com/fblpalmeira/movevis/blob/main/jaguar_pantanal_saobento_2008.txt)

<img src="https://github.com/fblpalmeira/movevis/blob/main/jaguar_pantanal_saobento_2008.gif">

REFERÊNCIAS:

[Dormann CF, Fruend J, Gruber B. 2021.](http://cran.r-project.org/web/packages/bipartite/bipartite.pdf) Package ‘bipartite’. 

[Fiske IJ & Chandler RB, 2011.](http://www.jstatsoft.org/v43/i10/paper) unmarked: An R package for fitting hierarchical models of wildlife occurrence and abundance. Journal of Statistical Software 43(1): 1-23.

[Mackenzie DI, Nichols JD, Royle JA, Pollock KH, Bailey LL, Hines JE. 2017.](https://books.google.com.br/books?hl=pt-BR&lr=&id=hs2cBAAAQBAJ&oi=fnd&pg=PP1&dq=ackenzie+DI,+Nichols+JD,+Royle+JA,+Pollock+KH,+Bailey+LL,+Hines+JE.+2006.&ots=-YchUeaAuX&sig=_kbFkM0CVDDrg8SU2rShw_g4JnM#v=onepage&q=ackenzie%20DI%2C%20Nichols%20JD%2C%20Royle%20JA%2C%20Pollock%20KH%2C%20Bailey%20LL%2C%20Hines%20JE.%202006.&f=false) Occupancy estimation and modeling: inferring patterns and dynamics of species occurrence. Elsevier, London.

[Morato, R. G. et al. 2018.](http://doi.org/10.1002/ecy.2379) Jaguar movement database: a GPS-based movement dataset of an apex predator in the Neotropics. Ecology.

[Palmeira FBL, 2015.](https://www.teses.usp.br/teses/disponiveis/11/11150/tde-17092015-111206/publico/Francesca_Belem_Lopes_Palmeira_versao_revisada.pdf) Coocorrência, interações tróficas e distribuição potencial da onça-pintada (Panthera onca) no bioma Amazônia. Tese de Doutorado, Universidade de São Paulo (USP).

[Perdomo G, 2015.](https://cran.r-project.org/web/packages/foodweb/foodweb.pdf) Package 'foodweb'.

[Schwalb-Willmann, J. 2020.](https://cran.r-project.org/web/packages/moveVis/moveVis.pdf) Package 'moveVis': Movement Data Visualization.
