# Veremos como podemos usar git com Branch

## 1 - Primeiro sempre que terminarmos uma parte do código devemos dar commit

```JavaScript
git init // Aqui é para criar o git
git  branch -M main // Criar uma brench para main
git add . // Adiciona tudo o que vc fez
git commit -m ""// dizer oq vc fez neste commit
```

## 2- Depois que fizer as primeiras linhas  sempre faça uma nova brach

Vamos imaginar o seguinte vc fez uma pagina inteira e entrego para seu cliente, porém agora ele quer um login. Mas vc pensa "Se eu fizer isso no main pode estragar meu projeto, e agora oq faço?" Ai que entra a criação de branch

```JavaScript
// Criar uma branch nova
// Além de criar uma branch ele já troca a branch que vc está
git switch -c nome-da-branch

// Caso o switch não funcione utilize
git checkout nome-da-brench

// Criar um novo pelo modo de cima
git checkout -b nome-da-brench
// vc pode ver quantos commits já realizou
git log

// Caso queira algo mais bonito e em uma unica linha
git log --graph --all --oneline
```

Desta forma vc cria uma branch e utilizará ela da melhor forma possivel

## 3- Finalizei oque precisava na branch, então finalize

Após vc ter terminado tudo o que precisava na branch, agora vc deve juntar ela com sua principal (main). MAS LEMBRE-SE SÓ JUNTE QUANDO TIVER TERMINADO TUDO NA BRENCH

```JavaScript
// Para navegar pelas brenchs ou no caso agora que é ir para main
git switch nome-da-branch // assim vc consegue navegar entre as branchs

// para juntar as informações das branchs para a principal
git merge nome-da-brench

// Após a junção das branch vc precisa apagar a que vc tinha criando
// assim deixa o código mais organizado
git branch -d nome-da-brench  // se não der certo use -D para tentar apagar a brench
```

Assim se quiser vc pode já enviar pro git hub sem nenhum problema.

## 4- (Obs) Caso vc pare de codar e precisa continuar o projeto sem juntar na brench main?

Vamos pensar na seguinte situação. Vc finalizou seu dia de trabalho mas vc ainda não terminou oq precisava na sua branch como vc faz para enviar pro Git Hub?

```JavaScript
// Para enviar a branch para o git hub
git push --set-upstream origin nome-da-brench

// Se preferir vc pode dar git push NA BRENCH QUE NÃO É A PRINCIPAL
// Para poder ver esse código acima para poder copiar

```

Agora vamos dizer que já terminou oq tinha que fazer, ja juntou as branch e apagou localmente sua branch. Porém no GitHub ainda está lá a brench como vc pode apagar?

```JavaScript
git push origin --delete nome-da-branch

// para puxar a brench feita no GitHub
git pull origin <nome-da-branch>
```
