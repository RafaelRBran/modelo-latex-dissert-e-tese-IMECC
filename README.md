Introdução
========

Este projeto é uma adaptação do template de dissertações e teses do IMECC-Unicamp. 

A ideia para este repositório surgiu quando eu comecei a trabalhar na minha própria dissertação de mestrado. Me lembro que na época tive bastante trabalho para entender o modelo original e passei algum tempo organizando-o de uma forma que fosse conveniente para as minhas necessidades. Conversando com os meus colegas, percebi que haviam algumas dificuldades comuns associadas a esse template.
Por isso, achei que poderia ser útil compartilhar uma versão "limpa" dos meus arquivos, para servir de apoio a trabalhos futuros.

No entanto, é importante destacar que este repositório **não é oficial**, **não tem qualquer garantia** e **não pretende substituir os arquivos originais**. A ideia aqui é simplesmente fornecer uma *sugestão* de como organizar os diversos arquivos necessários para a compilação de uma dissertação ou tese. Se eu encontrasse este repositório antes de escrever a minha dissertação (em uma estranha linha do tempo alternativa), eu tentaria entender o trabalho que foi feito aqui e partiria da versão original para fazer uma terceira versão adequada para as minhas necessidades.

Quero ser bem claro aqui. Este repositório não é, de forma alguma, uma tentativa de diminuir o template original, [disponível no site do IMECC](https://www.ime.unicamp.br/pos-graduacao/procedimentos-formularios/defesa-tese-dissertacao) (acessado pela última vez no dia 21/05/2023). Aqui só estou tentando organizar uma estrutura de arquivos que me pareceu um tanto confusa à primeira vista, *mas que abriga um projeto que me foi de enorme ajuda quando precisei dele*. A maior parte do crédito pelo conteúdo deste repositório se deve ao autor original do template.

Como esses arquivos estão organizados?
--------------------------------------
A estrutura proposta aqui é bastante simples.

1. O arquivo `nome_do_pdf.tex` é o arquivo principal deste template e é o único arquivo que deve ser compilado.
    * Mude o título como quiser, sabendo que esse também será o nome do pdf final.
    * Sugiro que você comece por esse arquivo e leia todas as sugestões que deixei. Isso já deve dar alguma ideia da estrutura geral do projeto (que continuo descrevendo a seguir).

2. A pasta `00-configs`  é onde as configurações do template ficam armazenadas.
    * Comece pelo arquivo `dados.tex`. Esse arquivo serve para você inserir informações da sua dissertação como seu nome, o nome do seu orientador e o título do trabalho.
    * Em seguida, vá para o arquivo `configglobal.tex`. Se você já entende um pouco de LaTeX, divirta-se. É aqui que você vai definir as macros e comandos personalizados que preferir (só tome cuidado para não apagar ou sobrescrever configurações "obrigatórias" do template). Se você não se sente seguro editando esse arquivo, ignore-o.
    * Por fim, o arquivo `pacotes.tex` contém as chamadas de bibliotecas do LaTeX. Edições aqui devem ser simples, adicionando ou removendo o que você precisar (lembre-se de usar o arquivo `configglobal` para as configurações). Deixei algumas sugestões indicadas, mas tome muito cuidado para não apagar as bibliotecas "básicas".
    * O arquivo `imecc-unicamp.cls` **deve continuar como está**. Leia se quiser, mas não mude nada aqui.

3. As pastas `01-pretextuais`, `02-textuais` e `03-pós_textuais` é onde você trabalhará efetivamente.
    * Deixei alguns arquivos como exemplo, mas você pode alterá-los como achar melhor.
    * Para, por exemplo, adicionar um novo capítulo, você deve (i) criar um arquivo `.tex` na pasta `02-textuais` com o conteúdo do capítulo, (ii) abrir o arquivo `nome_do_pdf.tex` e fazer uma cópia das linhas que começam com "`\chapter`" e "`\input`" na área do desenvolvimento (acredito que sejam as linhas 143 e 144) e (iii) substituir os campos entre {} conforme a necessidade.

4. As pastas `figuras` e `tabelas` são uma sugestão para a sua organização.
    * Acho mais fácil separar esses arquivos para evitar a bagunça, mas no seu trabalho é você quem decide (como todo o resto).
    * Dica: Quando fiz a minha dissertação, meus gráficos ficavam em uma pasta junto com os códigos em R que escrevi (fora dessa estrutura). Para facilitar nas chamadas, substituí a pasta `figuras` por um link para esse diretório.

5. Os arquivos `LICENSE` e `README.md` podem ser apagados.

6. Você vai precisar criar um arquivo de referências (.bib).

Por fim, como o template original destaca: **"Para usar este modelo de trabalho acadêmico, você deve estar utilizando codificação UTF8 no seu editor LaTeX. Esta configuração se aplica a todos os arquivos envolvidos à produção do trabalho acadêmico usando este modelo."**

Nota: Trabalhos escritos em outras línguas
------------------------------------------
Tirei tudo o que se refere à escrita de trabalhos em outros idiomas (por simplicidade). Se é o caso do seu trabalho não fique assustado. Comparando a minha versão com a original você deve conseguir fazer as alterações necessárias.

"Preciso de ajuda para escrever em LaTeX"
-----------------------------------------
Todo esse template pode parecer desesperador para quem nunca trabalhou com LaTeX, mas fique tranquilo. A linguagem é bem mais simples do que parece e aprendê-la deve ser um trabalho bem menor do que ficar configurando a sua dissertação/tese em outros softwares.

Em geral a regra é: A primeira semana é uma tortura, dentro de um mês você está trabalhando na mesma velocidade que em outros softwares, e em dois meses você começa a se perguntar como um dia foi capaz de usar qualquer outra coisa.

Para começar, sugiro que você procure algum tutorial online. Uma sugestão gratuita é a [playlist](https://www.youtube.com/watch?v=gFAQd0ueIMc&list=PLCRFsOKSM7eNGNghvT6QdzsDYwSTZxqjC) do pessoal do Overleaf (antigo ShareLaTeX) no YouTube (tenha bastante café em casa).

### "Instalo o LaTeX meu computador ou trabalho remotamente?"
Se você não sabe nada da linguagem e setá inseguro, use o [Overleaf](https://pt.overleaf.com). É um site gratuito para trabalhar em LaTeX na nuvem, bem no estilo do office do Google. Tudo o que você precisa já deve estar pronto para ser usado lá, sem a necessidade de instalar nada.

Por outro lado, se você já domina o LaTeX (ou só quer aprender mais), eu recomendo usar o seu próprio computador. Muita gente vai discordar de mim aqui e não quero escrever uma bíblia, mas **na minha opinião**, as vantagens são as seguintes:

1. Você pode aprender bastante sobre o seu sistema instalando o compilador manualmente.
2. Você pode fazer controle de versões por Git (mesmo que o Overleaf já tenha ferramentas para isso).
3. Seus arquivos estão disponíveis offline.
4. Você pode criar um arquivo de bibliografias (.bib) único para o seu sistema.
5. Você pode escolher o seu editor de texto.
    * Editar LaTeX usando Vim se tornou uma paixão para mim. Não vou entrar em muitos detalhes, mas as duas ferramentas se complementam incrivelmente bem. Algum dia devo criar um repositório com as minhas configurações para isso.

Licença
-------
Quero ser terrivelmente claro aqui.

1. Deixei aqui a licença MIT para transmitir a seguinte mensagem: Não me importo com o que você vai fazer com esse repositório. Modifique, distribua e use este repositório como achar melhor.

2. Se você sente que eu estou violando os seus direitos com este projeto, entre em contato comigo. Se for necessário, eu **VOU APAGAR** este repositório sem pensar duas vezes.
    * O template original é assinado por Fábio Rodrigues Silva, e se baseia no projeto [abnTeX2](https://www.abntex.net.br).

"Quero contribuir com o projeto"
--------------------------------
Este trabalho é mais um exercício (ou uma brincadeira) do que qualquer outra coisa. Sugestões são bem-vindas mas, por favor, não fique chateado caso a minha resposta demore.

