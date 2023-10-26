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

* Abra o terminal e atualize o sistema com `sudo apt update`.
* Instale o Nginx com `sudo apt install nginx`.
* Inicie o serviço com `sudo systemctl start nginx`.
* Verifique o status com `sudo systemctl status nginx` para garantir que o Nginx esteja em execução.
* Vá para o diretório de configuração com `cd /etc/nginx/sites-available/`.
* Abra o arquivo de configuração padrão com um editor de texto, como `sudo nano default`.
* No arquivo de configuração, substitua o conteúdo pela seguinte linha: `echo "ADA + AdaTech + SeuNome = Sucesso!" > /var/www/html/index.html`.
* Salve o arquivo e saia do editor.
* Reinicie o Nginx com `sudo systemctl restart nginx`
