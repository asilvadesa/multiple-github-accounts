# personal-multiple-github-accounts

### Como configurar multiplas contas GitHub no mesmo computador
- Encontrei um material em inglês para a instalação do Appium para Ubuntu, para mais informações 
[clique aqui](https://confusedcoders.com/general-programming/mobile/how-to-install-appium-in-ubuntu). 

### Steps
### 1. Crie os arquivos Git de configuração
  ```
    $ cd ~
    $ touch .gitconfig .gitconfig-personal .gitconfig-work
  ```

### 2. Copie as seguintes informações para os arquivos Git de configuração
  ```
    $ vim .gitconfig

    [user]
	    name = Anderson Silva de Sa
    [includeIf "gitdir:~/workspace/personal/"]
	    path = ~/.gitconfig-personal
    [includeIf "gitdir:~/workspace/work/"]
	    path = ~/.gitconfig-work
  ```

    $ vim .gitconfig-personal

    [user]
	    name = Anderson Silva de Sa
	    email = asilvadesa@gmail.com

    [core]
	    sshCommand = "ssh -i ~/.ssh/personal_id_rsa"
  ```

    $ vim .gitconfig-work

    [user]
	    name = Anderson Silva de Sa
	    email = asilvagit@gmailcom

    [core]
	    sshCommand = "ssh -i ~/.ssh/work_id_rsa"
  ```

### 3. Crie os diretórios

```
    $ cd ~
    $ mkdir workspace
    $ cd worksppace
    $ mkdir personal work
```

### 4. Crie as chaves SSH

```
    $ cd ~/.ssh
    $ ssh-keygen -f personal_id_rsa
    $ ssh-keygen -f work_id_rsa
```
### 5. Copie as chaves SSH

```
    $ cd ~/.ssh
    $ cat personal_id_rsa.pub
    $ cat personal_id_rsa.pub
```


 

