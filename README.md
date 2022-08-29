# introducao-git
Material para introdução e adaptação ao Git e Github.
## O que é GIT? 

É um sistema open source de controle de versionamento, ou seja, versões. Pode ser utilizado para registro de histórico de edições de qualquer tipo de arquivos. 

Para esse curso é necessário ter instalado em sua máquina o Git Bash. Vamos manipular os arquivos através de linhas de comandos no Git bash, vale lembrar que para isso precisaremos realizar uma configuração em seu Git conectando-o com o Github, mas antes disso vamos entender/ relembrar o que é Github. 

## O que é Github? 

GitHub é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git. Ele permite que programadores, utilitários ou qualquer usuário cadastrado na plataforma contribuam em projetos privados e/ou Open Source de qualquer lugar do mundo.  

Para acessar esse serviço acesse o link:  https://github.com/ 

É necessário fazer o cadastro na plataforma. Acesse o link e clique em **Sign Up**, caso já tenha um cadastro clique em **sign in**.<br>
Se faz necessário reforçar que, quando instalamos o Git em uma máquina, ainda se faz necessário ter essa conta na plataforma para ter acesso a mesma e ter condições de desfrutar das vantagens que a plataforma oferece, já que a partir do momento que os seus arquivos estão salvos em seu Git, podemos transferi-los ao Github e com isso teremos a segurança de ter os arquivos salvos em nuvem(servidor do Github), com isso caso tenha problemas em seu computador, ou precisarmos fazer uso desses arquivos em outro computador com acesso a internet, poderemos ter acesso a estes através de nosso acesso a plataforma, ainda é possível compartilhar com sua equipe ou colegas estes arquivos.
<img src="https://files.fm/thumb_show.php?i=adnu5qafx">

## Configurações do Git

A primeira coisa a se fazer é ter o nome de usuário do Git e e-mail, para isso vamos fazer o seguinte passo a passo, mas lembre-se que esse processo de 
configuração do usuário e e-mail deve ser feito no primeiro uso da ferramenta e após isso não será necessário reconfigurar. Salvo o caso de ter sua máquina formatada.
Para esta configuração, tenha os dados usuario que estará na url ao logar no seu githut opção perfil, veja a imagem abaixo onde essa informação pode ser localizada.
<img src="https://files.fm/thumb_show.php?i=ds437mrpj">
Já temos as informações então vamos iniciar o nosso Git bash já dentro de uma pasta para conseguirmos já realizar também os primeiros testes mais tarde.
### Iniciar o Git Bash dentro de um diretório
1. Na área de trabalho foi criada a pasta **git-testes**.
2. Vou clicar dentro da pasta com botão direito do mouse
3. Clicar na opção Git Bash do menu suspenso.
<img src="https://files.fm/thumb_show.php?i=5xs93xnby">
O resultado esperado é ter a tela de Git Bash aberta, ver imagem do Git Bash:
<img src="https://files.fm/thumb_show.php?i=cnfs5ry2y">
*Vale destacar que ao abrir o Git bash, da forma indicada nos passo-a-passo acima, faz com que o mesmo já venha predefinido a operar dentro da pasta git-testes*
<img src="https://files.fm/thumb_show.php?i=8z3x2vnxs">

Agora sim, podemos configurar o Git conectando-o ao Github
### Configurar e-mail e usuário no Git
1. Para informar o usuário vamos executar o comando: git config --global user.name SEU-USUARIO-DO-GITHUB pressione o ENTER do teclado<br>
2. Para informar o e-mail da conta Github executar o comando: git config --global user. email email_utilizado_na_conta_github@email.com pressione o ENTER do teclado
<img src="https://files.fm/thumb_show.php?i=cyjpwg36t">

### exibir os dados de configuração do Git
Para verificar os dados de configuração do seu Git execute o seguinte comando:<br>
1. git config --list <br>
2. pressione o Enter do teclado para o comando ser executado.<br>
<img src="https://files.fm/thumb_show.php?i=dcs47yyn3">
*note que a imagem anterior, podemos ver que as ultimas duas linhas teremos os nossos dados, mas ATENÇÃO NÃO UTILIZE OS DADOS DA IMAGEM EM SUA CONFIGURAÇÃO, UTILIZE OS SEUS DADOS DE USUÁRIO CADASTRADO NO GITHUB E E-MAIL*

## Preparando um repositório no Github
<br>Vamos então criar nosso primeiro repósito remoto, no Github para podemos iniciar nosso processo de guardar arquivos em nuvem, ou seja, no servidor do Github.<br>
Dica: leia o passo a passo e depois siga os passos com calma atentando-se de não pular nenhuma das etapas, siga exatamente como esta sendo conduzido esse manual para um melhor aproveitamento do material e depois se desafie em fazer outros repositórios sozinhe.<br>
1. No seu painel do Github vamos e no menu do canto direito superior vamos escolher a opção YOUR REPOSITORIES<br>
<img src="https://files.fm/thumb_show.php?i=kawfvfvn9">
2. Ao acessarmos a tela de repositórios vamos localizar e clicar no botão NEW<br>
<img src="https://files.fm/thumb_show.php?i=kj87vtyxx">
3. Agora vamos nomear esse novo repositório como Git-testes mesmo nome do diretório em nossa máquina. Para isso basta preencher o campo **Repository name**<br>
4. Em Description (optional) vamos descrever essa ação como "Primeiros testes em Git"<br>
5. Mantenha selecionado a opção Public, que indica que esse diretório será publico, quando você estiver tratando projetos que não podem/devem ser visualizados por todes, poderá selecionar a opção Private.<br>
<img src="https://files.fm/thumb_show.php?i=3j88q83at">
6. Em Initialize this repository with: deixar a opção Add a README file DESMARCADA.<br>
7. Clique no botão **Create Repository**<br>
<img src="https://files.fm/thumb_show.php?i=b2xhawug7">
Após criar o repositório vamos ter a visualização do mesmo, note que a primeira tela após a criação do repositório já nos trás algumas instruções e linhas de códigos que vamos melhor entender nos próximos passos<br>
<img src="https://files.fm/thumb_show.php?i=ph8x9vaeg">
<br>

## Conectar o repositório do Github com o seu diretório local
<br>Vale destacar que poderemos ter diversos repositórios em nosso GitHub e desta forma organizar nossos projetos/serviços, crie quantos repositórios forem necessários.<br>

1. Confirme se vc iniciou o seu Gitbash no diretório correto, acima sugerimos criar o diretório git-testes, vamos utilizar esse diretório
  <img src="https://files.fm/thumb_show.php?i=cnfs5ry2y">

2. Vamos tornar esse diretório um diretório inicial para o Git com o comando <code>git init</code> pressione o <code>Enter</code> do seu teclado após digitar o comando.<br>

3. Agora vamos criar algum arquivo dentro desse diretório para termos alguma alteração a ser detectada pelo Git

   3.1 Abra o bloco de notas e escreva o texto: *primeiro arquivo dentro do repositório*

   3.2 Salve o arquivo dentro do diretório **git-testes** com o nome **arquivo1.txt** 

   <img src="https://files.fm/thumb_show.php?i=sgj66qk75">

4. Agora vamos executar o segundo comando só que com algumas alterações <code> git add .</code> após pressione o <code>Enter</code> do seu teclado 

   4.1 Basicamente esse comando adiciona os arquivos que o Git vai trabalhar, ou seja, o que ele precisa se preocupar em acompanhar mudanças de estado para o versionamento. Quando utilizamos o ponto após a palavra add estamos indicando que todos os arquivos alterados/ adicionados devem ser adicionados 

5. O comando seguinte será o commit digite: <code>git commit -m "primeiro commint"</code> após isso pressione o <code>Enter</code> do seu teclado.

   5.1 Esse comando faz uma ação que podemos entender como etiquetar a mudança que nosso repositório teve, esse passo é importante para sinalizar por exemplo que a alteração foi feita e assim ter maior controle sobre os status do seu repositório.

6. Feito vamos para a próxima linha que é alinhar e garantir que estamos trabalhando na branch correta, mais tarde vamos entender melhor o que essa banch significa e como manipular as branch, por hora entendemos que branch é uma forma de controlar qual versão do repositório vamos afetar nesse momento. Então execute o comando: <code>git branch -M main</code> e pressione o <code>Enter</code> do seu teclado.

   6.1 Note a alteração no nosso gitbash após a execução desse comando<br>
   <img src="https://files.fm/thumb_show.php?i=8785pfhy7">
  Lembre-se que a cada novo arquivo adicionado ou incluído nesse diretório para essa alteração seguir no seu Github é necessário seguir esses últimos passas de:

   <pre>
       <code>
       	git add.
       	git commit -m "mensagem explicando o que foi alterado resumidamente"
           git push -u origin main
       </code>
   </pre>

   <img src="https://files.fm/thumb_show.php?i=ekj9m3cns">

   Ainda podemos ver as alterações, para isso clique sobre o arquivo dentro do Github e confira também a quanto tempo foi feita a ultima atualização.

   <img src="https://files.fm/thumb_show.php?i=q6k4p3dda">

   <img src="https://files.fm/thumb_show.php?i=ukvezb8sw">

   Experimente adicionar novos arquivos dentro do diretório em seu computador 

   <img src="https://files.fm/thumb_show.php?i=5674ku6hx">

   ## Baixar atualização do Remoto(Github) para o diretório local
   Lembrando que o Git pode ser utilizado entre equipes, devemos também nos atentar a como podemos atualizar em nossa máquina uma alteração que esta no Github
   1. Primeira coisa a se fazer quando estamos trabalhando em equipe é usar o comando <code>git pull</code><br>
    1.1 Esse comando acima garante que as atualizações que já estão no servidor sejam baixadas para sua máquina. **Lembre-se sempre de conversar com sua equipe antes de subir seus arquivos na nuvem**. 
    
   ### testar o git pull
 1. Acesse seu repositório no Github e abra o arquivo pelo navegador, conforme a imagem abaixo<br>
  <img src="https://files.fm/thumb_show.php?i=ceregk5e3">
  2. Clique em editar arquivo<br>
  3. Adicione as alterações no conteúdo do arquivo, basta adicionar mais texto ao arquivo.<br>
  <img src="https://files.fm/thumb_show.php?i=eragvbugx">
  5. Descer até o final da página e dar um nome ao seu Commit e também comentário. <br>
  6. Clicar no botão **Commit Changes**<br>
 <img src="https://files.fm/thumb_show.php?i=j8v8nv2uh">
  7. Execute no Git Bash o comando <code>git pull</code>

<img src="https://files.fm/thumb_show.php?i=sgunmjnn5">
<br>
*Faça o teste, abra novamente em seu computador o arquivo que foi alterado diretamente no Github e veja se as linhas adicionadas então ali.*
<br>
*Lembre-se que programar exige calma, atenção aos detalhes e persistência. Leia a faça com calma os passos aqui sugeridos.*
<br>
*Em caso de erros você pode copiar a mensagem de erro e fazer uma pesquisa no Google ou chamar seus instrutores.*
<br> 
Bons códigos e sucesso!
