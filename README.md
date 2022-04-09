# Treinamento FULLSTACK

### Comandos básicos git (Windows)
- cd: usado para caminhar entre as pastas.
- dir: lista todas as pastas.
- mkdir: cria uma nova pasta.
- rmdiv 'nome da pasta: remove toda a pasta (/S /Q).
- $git rm 'nome do arquivo': remove um arquivo.
- ls: lista dos o diretório que está selecionado.
- Tecla TAB: auto-complete.
- $git clone 'link SSH': realiza o clone de repositórios.

### Flags
- -a: Para listar até pastas ou arquivos ocultos;
- -m: flag para dar o commit;

### Iniciação de um repositório
- Para configurar pelcaso seja a primeira vez usamos usuário e email do git;

1. Email
- git config --global user.email 'escreve seu email aqui';
2. User
git config --global user.name 'seu user aqui'

- Caso o user ou email esteja incorreto usamos;
- git config --global --unset 'nome da propriedade' (user.email; user.name).

### Manipulação de diretório Git e GitHub
- $git inti: inicia uma pasta como repositório e adiciona a pasta .git.
- $git status: retorna se há alguma pasta ou arquivo modificado para envialo ao stage.
- $git add: serve para enviar os arquivos para o commit. Para enviar se adiciona o nome do arquivo ao o * para enviar todos os documentos.
- $gti commit -m 'comment' :  adiciona os arquivos no stage e manda o seu comentário.
1. Para inserir os dados do repositório local e envialos para um repositório remoto utilizamos:
- $git remote add origin 'link do github repositório'.
- $git remote -v: retorna a lista de diretórios.
2. Para enviar as alteraçoes do stage para o repositório remoto utilizamos:
- $git push origin master

- Caso exista algua alteração de outros usuários precisamos executar o pull para ter as pastas e repositório atualizado.

3. Para receber os novos dados atualizados do repositório e evitar erros utilizamos: 
- $git pull origin master
- Alteramos ou atualizamos o conteúdo para funcionar sem erros.

### Chaves SSH
- Conecta o seu computador local com o seu github e melhora a interação com os repositórios. Para criar uma chave SSH, fazemos os seguintes passos:

1. No github, vamos até as chaves SSH e voltamos para o git,
lá é onde vamos criar as chaves. 
2. O comando utilizado para gerar as chaves é :
- ssh-keygen -t es25519 -C 'seu email aqui'; 
- logo apos irá pedir uma senha;
- Depois de confirmar sua identificação as chaves estarão salvas.

3. Depois vamos visualizar a pasta das chaves e ler a chave publica para colocala no github.
- O comando utilizado é $cat 'nome da sua chave aqui'. (Ele irá ler sua chave pub)
- Depois de criar a chave no github, precisamos de um agente para gerenciar os diretórios.
- O comando utilizado para gerar o agente é: eval $(ssh-agent -s);
- Depois adicionamos a chave para o agente utilizando o comando: ssh-add 'id da sua chave privada'.