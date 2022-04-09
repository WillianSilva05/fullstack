# Teste treinamento FULLSTACK

### Chaves SSH

- Conecta o seu computador remoto com o seu github e melhora a interação com os repositórios.

Para criar uma chave SSH, fazemos os seguintes passos.

1. No github, vamos até as chaves SSH e voltamos para o git,
lá é onnde vamos criar as chaves.
O comando utilizado para gerar as chaves é :
- ssh-keygen -t es25519 -C 'seu email aqui';
logo apos irá pedir uma senha;
Depois de confirmar sua identificação e chaves estarão salvas.

2. Depois vamos visualizar a pasta das chaves e ler a chave publica para colocala no github.
- O comando utilizado é $cat 'nome da sua chave aqui'.
- Depois de criar a chave no github, precisamos de um agente para gerenciar os diretórios.
- O comando utilizado para gerar o agente é: 
eval $(ssh-agent -s);
- Depois adicionamos a chave para p agente:
ssh-add 'id da sua chave privada'

### Iniciação de um repositório

- Abrir o git e criar uma pasta, e então para iniciar o repositorio usamos o comando;
git init.

- Para configurar a primeira vez o usuário e email do git utiliazamos;
1. Email
git config --global user.email 'escreve seu email aqui';
2. User
git config --global user.name 'seu user aqui'

- Caso o user ou email esteja incorreto usamos;
git config --global --unset 'nome da propriedade' (user.email; user.name)

### Para adicionar alterações no repositório

- Para criar o repositório local (git init)
1. git add 'nome do arquivo' ou * (adiciona todos os arquivos)
2. git commit -m 'comentário'
3. git status; retorna o status dos documentos no repositório e se há alguma alteração ou commit pendente.

### Para criar repositórios remotos que vão para o github

- Utilizamos o para criar o apelido do link.
git remote add origin 'link do repositório github.
- Para listar os repositórios disponíveis neste apelido usamos.
git remote -v

### Comandos básicos git

- cd; usado para caminhar entre as pastas.

- ls; lista todos os arquivos da pasta.

- dir; retorna todas as pastas.

- mkdir; cria uma nova pasta.