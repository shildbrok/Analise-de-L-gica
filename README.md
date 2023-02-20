# <h1>Analise de Lógica</h1>
Nesse texto, eu abordo com imagens e lógicas aplicadas para criação de um jogo simples, com movimentações básicas em 2D e marcação de pontuação.</br>
<a href="https://scratch.mit.edu/projects/806257361/">PROJETO REFERÊNCIA</a>

Urso Brocado

Este é um conteúdo sobre lógica de programação, a ideia inicial é fazer um mini-game onde a gente move o personagem principal
no eixo X, enquanto um objeto cai no eixo Y, e quando o personagem encostar na comida, iremos contar pontos e aumentar o
tamanho do personagem em 1.

Iremos utilizar uma ferramenta chamada Scratch, criada pelo MIT para ensinar programação para pessoas sem experiência.
Para acessar a ferramenta basta acessar o link https://scratch.mit.edu/.

<img src="https://github.com/shildbrok/Analise-de-L-gica/blob/main/image.png" alt="alternatetext">

Quando inicializar a ferramenta e logar, e ir a página de criação.

<img src="https://github.com/shildbrok/Analise-de-L-gica/blob/main/image1.png" alt="alternatetext">

Vamos COMEÇAR!

Primeiro vamos coletar o cenário no canto inferior direito. Clique no botão e selecione o cenário que deseja, eu acabei escolhendo
esse cenário. Porém caso você esteje testando em casa pode fazer com qualquer um desses cenários.

<img src="https://github.com/shildbrok/Analise-de-L-gica/blob/main/image3.png" alt="alternatetext">

<img src="https://github.com/shildbrok/Analise-de-L-gica/blob/main/image5.png" alt="alternatetext">

Logo após fazer isso, vamos deletar o personagem padrão(Gato), e vamos selecionar o urso.

<img src="https://github.com/shildbrok/Analise-de-L-gica/blob/main/image4.png" alt="alternatetext">

Pronto! Agora temos o personagem e a paisagem onde o jogo vai ocorrer. Vamos começar a montar a lógica do mini-game.

Montando a física : Vamos montar a física do chão e colocar a gravidade no urso.

Vamos clicar em 'Meus Blocos' vamos 'Criar novo Bloco' e vamos nomear ele como gravidade. Agora vamos em 'Movimento' e em 
seguida 'adicione __ a Y', no Scratch não temos alguns recursos, e um deles seriam retirar números, mas podemos burlar isso
colocando '-x' para poder fazer o 'mesmo efeito'. Mas entenda que apesar de ser identico, NÃO É A MESMA COISA.
Colocando -4 no Y o objeto que for aplicado esse efeito da gravidade, o sentido de direção dele sempre sera para baixo.

<img src="https://github.com/shildbrok/Analise-de-L-gica/blob/main/image8.png" alt="alternatetext">

Criando a física nos objetos : Criar física nos objetos é muito simples, basta usar um técnica de desenho.
Vamos fazer um desenho de uma reta. Após a reta ser desenhada, posicione no local desejado.

Então vamos a lógica :</br> 
Quando a Bandeira for clicada{</br>
	Sempre{</br>
		se *urso* não tocar na (Reta) então {</br>
		gravidade * Lembrando a gravidade está definida em -4*</br>
			  * forçando a decida no eixo Y do plano.*</br>
		}</br>
	}</br>
}</br>

Após esse primeiro script o urso deve ser forçado a ir para baixo.

Vamos faze o controle do Urso, ou seja se mover para um lado e para o outro, esse controle é simples de se fazer.

Quando a Bandeira for clicada{</br>
	Sempre{</br>
		se *urso* apertar a tecla A então {</br>
		adicione -7 a X *Isso faz com que o urso ande para o lado esquerdo*</br>
		}</br>
		se *urso* apertar a tecla D então {</br>
		adicione 7 a X *Isso faz com que o urso ande para o lado direito*</br>
		}</br>
	}</br>
}</br>

Agora o Urso deve se mover para o lado esquerdo e direito, esse é o script de movimento mais smples que deve ser feito.

Agora vamos criar a mecânica, do jogo desde o bolo cair sobre o solo, e quando tocar no Urso, contar os pontos, e aumentar
o tamanho to Urso.

Primeiro temos que criar uma Variavel chamada 'Pontos', ela vai ser responsavel por contar quantos bolos pegamos.
Essa é a parte mais complexa do script então reeleia muito, para conseguir entender.</br>

Quando a Bandeira for clicada{</br>
	mude Pontos para 0 *Isso fará com que resete todos os pontos ao iniciar o jogo*</br>
	vá para X: Numero Aleatório Entre -220 e 220 Y: 181 * -220 e 220 são as coordenadas que definem as bordas do layout
							    *ou seja se o bolo for alem desses numeros não ira aparecer na tela*</br>
	sempre{</br>
		se(*bolo* não tocando em reta) então{</br>
		adicione -1 a Y *Esse script fará com que o objeto desca devagar*</br>
		}</br>
		se(*bolo* tocar em urso) então{</br>
			adicione 1 a Ponto *Isso fará com que o ponto suba em 1 cada ve que o urso tocar o bolo*</br>
			vá para X: Numero Aleatório Entre -220 e 220 Y: 181 * esse código irá forçar cada vez que o urso tocar no bolo ir para cima novamente*</br>
		
		}</br>
	}</br>
}</br>
