# Principais comandos do Github

## Configurações
- __git config --g user.name <name>__ -> comando para configurar nome do usuário
- __git config --g user.email <email>__ -> comando para configurar o email do usuário
- __git config --g user.name <name>__ -> comando para configurar nome do usuário

## Comandos básicos e mais usados
- __git init <directory>__ -> inicializa um repositório git
- __git clone <repo_url>__ -> clona o repositório selecionado pra sua máquina
- __git remote add origin <repo_url>__ -> liga seu repositório local a um repositório remoto, caso você não tenha clonado um repositório já.
- __git add <directory> ou git add .__ -> adiciona os arquivos ao "stage", seja um arquivo especifico ou usando o "." para adicionar todos
- __git commit -m "message"__ -> vai "commitar"(registrar) seus arquivos e alterações no repositório, criando um 'ponto' na timeline do repositório
- __git push <origin> <branch_name>__ -> após adionar ao staged, fazer os commits, você manda as alterações que vc realizou no repositório local para o remoto
- __git status__ -> informações gerais do repositório e seus arquivos na branch
- __git log__ -> histórico
### Branches: Comandos que envolvem tais
- __git branch__ -> mostra as branches do repositório atual
- __git checkout <branch_name>__ -> navega entre branches disponíveis
- __git checkout -b <branch_name>__ -> cria uma nova branch com nome selecionado
- __git merge <branch_name>__ -> realiza o merge da branch selecionada
- __git fetch <remote> <branch>__ -> verifica se há mudanças no repositório original comparando com seu local
- __git pull <remote>__ -> faz o que o fetch faz, mas também copia as mudanças do repositório remoto pro seu local, atualizando seu repositório local
- __git diff <branch_origem> <branch_destino>__ -> verifica as diferenças entre arquivos dos repositórios local e remoto

# Entendendo Arrays (Javascript)

- Em um exercício onde devemos apresentar um array de 10 posições onde seus elementos estão em ordem decrescente (de 9 a 0):
Elementos: 9	8	7	6	5	4	3	2	1	0
Posições:  0	1	2	3	4	5	6	7	8	9

EXERCICIO 2 LISTA 6:
    - Resolução feita por mim:
            function gerar() {
                while (numbers.length < 10) {
                let proximoNum = numInicial + 1;
                numbers.push(proximoNum);
                numInicial = proximoNum;
                numbers.sort( function (a, b) {
                    return b - a;
                });
                }
    - Resolução que foi corrigida durante a aula (mais simples e fácil):
        function gerar() {
            var numero = [] //length = 0 
            var num = 9 
            for (let index = 0; index < 10; index++) {
                numero[index] = num-- 
                // numero[numero.length] = num-- 
                // num--
                // numero.push(num)
            }
            console.table(numero)
            console.log(numero)
            console.log(numero.toString())
        }

        


