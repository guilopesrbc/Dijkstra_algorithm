## Contexto do problema
O contexto do problema se baseia em encontrar o menor caminho dentro de um grafo, baseado em uma API, tomando um vértice como “raiz” da operação. A base utilizada foi uma lista de páginas presentes no Facebook as quais ligam a outros sites fora da página. A base de dados consiste previamente em um determinado “webgraph”, o qual contém ligações entre páginas. Tais páginas são conectadas por Id’s e possuem 4 tipos (Governmental organizations, politicians, Television shows and Companies). 

## Implementação
## Algoritmo utilizado
O algoritmo utilizado foi o de Dijkstra
## Desenvolvimento
Primeiramente optamos por realizar a construção de dois dataframes, responsáveis por mostrar os Id’s que tinham conexões, e as informações presentes no Database, respectivamente. Após a observação dos mesmos, passamos para a etapa da criação dos dicionários que seriam implementados na construção do algoritmo geral. Para a implementação criamos primeiro um algoritmo de Heap de Mínimo, uma vez que seria necessário para a criação do Dijkstra que viria posteriormente. Após o Heap, implementamos o Dijkstra e Networkx para a plotagem do output do programa em um  visualizador de grafo.
## Bibliotecas utilizadas
Em relação às bibliotecas utilizadas, destacamos duas: Sys e Pandas. Utilizamos a biblioteca “pandas” com o objetivo de criar os Dataframes, enquanto a utilização da biblioteca “Sys” se deu a fim de definirmos o número infinito para funcionamento do algoritmo de Dijkstra e . 
## Conclusão
Feito o set dos dicionários: um correspondente aos pesos de acordo com a relação que cada página tem, ps: os pesos foram definidos por nossa opnião indo de 1 a 4, ex: categoria governo tem um custo 4 em uma conexão com tvshow e custo 1 com conexão com a mesma categoria governo. Outro dicionário correspondente ao ID/nome (que busca o nome da página de acordo com o ID que for solicitado) e o último dicionário corresponde às conexões que cada id possui junto com o custo dessa conexão de acordo com o dicionário de pesos ex: { IDx : { IDy :CUSTOy, IDz : CUSTOz}} IDx possui conexão com IDy com um custo inteiro de CUSTOy. Partindo então para o algoritmo de dijkstra, a função é chamada com o vértice inicial e o vértice final, a função cria um novo dicionário com todos os vértices que salva o caminho que foi feito até ele e o custo desse caminho ex:  { IDx : { pred :[IDy, IDz], Cost: CUSTOy + CUSTOz}}. Com isso o Dijkstra vai percorrendo os caminhos dos vértices e adjacentes de acordo com o menor custo, utilizando o heap de mínimo e atualizando os caminhos e custos. No final imprime qual foi o melhor custo e seu caminho em uma lista, após isso executa a função visualize(g)  que plota um gráfico com o caminho que foi feito.
	

## Referências. https://www.youtube.com/watch?v=OrJ004Wid4o ( video referência de implementação do algoritmo.)
