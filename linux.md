# Problema 1: Criação de Novo Usuário

## Para criar um novo usuário no Linux, siga os seguintes passos:

* Abra o terminal ou acesse o servidor Linux.
* Use o comando sudo adduser nome_do_usuario para criar o novo usuário. Substitua "nome_do_usuario" pelo nome do usuário desejado.
* O sistema irá solicitar a definição de uma senha para o novo usuário.
* Preencha as informações adicionais, como nome real, telefone, etc., ou apenas pressione Enter para deixá-las em branco.
* O usuário será criado com um diretório pessoal em `/home/nome_do_usuario`.

## Problema 2: Permissões de Arquivo no Linux

Permissões de arquivo no Linux são representadas por três grupos de permissões: dono, grupo e outros, cada um com três permissões (leitura, escrita e execução). Elas são representadas por números octais (como 400) ou símbolos (como rw-r--r--).

Para definir permissões 400 para uma pasta e todos os arquivos recursivamente, siga os passos:

* Crie uma pasta usando `mkdir nomedapasta`.
* Use o comando `touch arquivo1.txt arquivo2.txt arquivo3.txt arquivo4.txt arquivo5.txt` para criar os 5 arquivos de texto.
* Use o comando `chmod -R 400 nomedapasta` para definir as permissões 400 recursivamente na pasta e seus arquivos. Isso concede permissão de leitura apenas para o dono dos arquivos e da pasta.
  
  <img width="571" alt="Screenshot 2023-10-25 at 21 34 17" src="https://github.com/laysearaujo/devops/assets/46059216/20b43475-7e64-4a42-8682-b8c3b6770125">

## Problema 3: Instalação e Configuração do Nginx

Para instalar e configurar o servidor web Nginx no Linux, siga os passos:

* Abra o terminal e atualize o sistema com `brew update`.
  
  <img width="569" alt="Screenshot 2023-10-25 at 21 46 23" src="https://github.com/laysearaujo/devops/assets/46059216/b6596387-0623-486c-9f88-6c6ff7dbf901">
* Instale o Nginx com `brew install nginx`.
  
  <img width="565" alt="Screenshot 2023-10-25 at 21 48 53" src="https://github.com/laysearaujo/devops/assets/46059216/d99aede5-5891-4a25-88d3-045db62b9813">
* Inicie o serviço com `brew services start nginx`.

  <img width="572" alt="Screenshot 2023-10-25 at 21 52 11" src="https://github.com/laysearaujo/devops/assets/46059216/e663bfd7-369b-4a3a-a832-6e8840249100">
* Verifique o status com `brew services list` para garantir que o Nginx esteja em execução.

  
  <img width="566" alt="Screenshot 2023-10-25 at 21 51 28" src="https://github.com/laysearaujo/devops/assets/46059216/491b84d4-f592-4f46-abde-4b2eb87824fa">
* Vá para o diretório de configuração com `cd /opt/homebrew/etc/nginx`.

  <img width="569" alt="Screenshot 2023-10-25 at 21 58 38" src="https://github.com/laysearaujo/devops/assets/46059216/9b4568d2-249a-4b3f-a170-ab473dbe858a">

* Abra o arquivo de configuração padrão com um editor de texto, como `sudo nano nginx.conf`.
* No arquivo de configuração, substitua o conteúdo pela seguinte linha: `echo "ADA + AdaTech + SeuNome = Sucesso!" > /var/www/html/index.html`.
* Salve o arquivo e saia do editor.

  <img width="561" alt="Screenshot 2023-10-25 at 22 30 58" src="https://github.com/laysearaujo/devops/assets/46059216/b7eee816-e0bb-4fde-8d0f-c98ed6e07f09">
* Reinicie o Nginx com `sudo brew services restart nginx`

  <img width="426" alt="Screenshot 2023-10-25 at 22 29 33" src="https://github.com/laysearaujo/devops/assets/46059216/04990679-bd6a-4db5-a0bf-d0a721f33e74">
