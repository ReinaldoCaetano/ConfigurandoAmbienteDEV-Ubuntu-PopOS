#  Configurando Ambiente de Desenvolvimento- PopOS, Ubuntu e derivados Debian

<h2>
🛑 Pré-requistos
</h2>


<strong>- [x] Sistema operacional 🐧 Linux [Debian](https://www.debian.org/derivatives/index.pt.html#:~:text=Um%20derivado%20do%20Debian%20%C3%A9,objetivos%20que%20eles%20mesmos%20estabeleceram.) ou derivados dele.</strong>

 
<h3>🔺 Instalação Git </h3>

🔸 <strong>1.</strong> Abra o terminal (Ctrl + Alt + t) e vamos verificar se temos o git instalado:

```
git --version
```

🔸 <strong>2.</strong> Execute o comando:

```
sudo apt-get install git-all
```

🔸<strong>3.</strong> Confirme novamente se o git realmente está instalado:

```
git --version
```

🔸 <strong>4.</strong> Vamos começar as configurações iniciais:

​🔸	<strong>4.1</strong> Cofigurar o nome de usuário

```
git config --global user.name "Seu nome"
```

​🔸	<strong>4.2</strong> Configurar o endereço de e-mail:

​ <em>É de suma importância que o ENDEREÇO DE E-MAIL SEJA O MESMO DO GITHUB afim de evitar conflitos!</em>

```
git config --global user.email seuemail@email.br
```

​🔸 <strong>4.3</strong> Vamos conferir a lista de configurações:

```
git config --list
```

🔸 <strong>5.</strong> Pronto, git instalado e configurado com sucesso!

<br>

<h3>🔺 Instalação GitHub-Desktop </h3>

🔹 <strong>1.</strong> Acessar o site oficial do [Flatpack](https://flatpak.org/setup/) e instale de acordo com seu linux, no caso o PopOs ja vem por padrão instalado más teoricamente seria rodar esses comandos  

```
sudo apt install flatpak
```
```
flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
🔹 <strong>2.</strong> Para instalar GitHub-Desktop basta usar o terminal ou a loja de aplicativos 

```
flatpak install flathub io.github.shiftey.Desktop
```
<br>

<h3>🔺 Instalação do ASDF </h3>

<strong>O que é ASDF ?</strong>

<em>[ASDF](https://asdf-vm.com/guide/getting-started.html) É uma ferramenta para gerenciamento de versões, diferentemente do rbenv para Ruby ou nvm para o Node. js, que gerenciam linguagens específicas. Também nominada como ASDF-VM, ela administra versões para diversas linguagens, por meio do seu sistema de [plugins](https://github.com/asdf-vm/asdf-plugins)  <strong>Vantagens</strong> Além da facilidade para configurar ambientes, o ASDF fornece a possibilidade de configurar versões globais e locais. Global para os casos de configuração padrão, e local para projetos específicos quando é indispensável o uso de uma versão específica</em>


🔸 <strong>1.</strong> Para Instalar asdf Precisamos de algumas dependencias de pacote como git e curl, então abra o terminal

```
sudo apt install curl git-all -y
```

🔸 <strong>2.</strong> Para fazer download do asdf basta executar</em>

```
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.11.3
```

🔸 <strong>3.</strong> Existem muitas combinações diferentes de shells, no caso do Ubuntu e PopOs por padrao vem o bash, basta editar aquivo ~/.bashrc e add o codigo abaixo, Duvidas de configurar para outro shell na documentação [ASDF](https://asdf-vm.com/guide/getting-started.html#official-download) tem a resposta !

```
. "$HOME/.asdf/asdf.sh"
```

🔸 <strong>4.</strong> Verificando se o asdf esta instalando e configurado:
```
asdf --version
```
<br>
<h3>🔺 Instalação do Java Usando ASDF </h3>

🔸 <strong>1.</strong> Add plugin java com asdf 

```
asdf plugin add java
```

​🔸	<strong>2.</strong> listando as versões do java :

```
asdf list all java 
```

​🔸	<strong>3.</strong> Depois de escolher a versão entre as mais de 190 que tem basta instalar:

```
asdf install java openjdk-17.0.2
```

​🔸	<strong>4.</strong> Você pode configurar umac como padrao Como um java Global ou local 

```
asdf global java openjdk-17.0.2
```
🔸 <strong>5.</strong> Para configurar java home basta add no seu shell o caminho do [link](https://github.com/halcyon/asdf-java) no caso do ubuntu e PopOS  que é o bash basta edd ao arquivo ~/.bashrc 

```
. ~/.asdf/plugins/java/set-java-home.bash
```


<br>

<h3>🔺 Instalação do Maven Usando ASDF </h3>

🔸 <strong>1.</strong> Add plugin Maven com asdf 

```
asdf plugin add maven
```

🔸​	<strong>2.</strong> listando as versões do java :

```
asdf list all maven
```

🔸​	<strong>3.</strong> Depois de escolher a versão:

```
asdf install maven 3.9.1
```
🔸​	<strong>4.</strong> Configurar maven Global:

```
asdf global maven 3.9.1
```

🔸​	<strong>5.</strong> Verificar Maven instalado e em uso:

```
mvn --version
```

<br>

<h3>🔺 Instalação Intellij </h3>

🔹 <strong>1.</strong> Acessar o site oficial do [Flatpack](https://flatpak.org/setup/) e instale de acordo com seu linux, no caso o PopOs ja vem por padrão instalado más teoricamente seria rodar esses comandos  

```
sudo apt install flatpak
```
```
flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
🔹 <strong>2.</strong> Para instalar Intellij basta usar o terminal ou a loja de aplicativo 

```
flatpak install flathub com.jetbrains.IntelliJ-IDEA-Community

```
<br>
<h3>🔺 Instalação Visual Studio Code </h3>

🔹 <strong>1.</strong> Acessar o site oficial do [Flatpack](https://flatpak.org/setup/) e instale de acordo com seu linux, no caso o PopOs ja vem por padrão instalado más teoricamente seria rodar esses comandos  

```
sudo apt install flatpak
```
```
flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
🔹 <strong>2.</strong> Para instalar Visual studio Code basta usar o terminal ou a loja de aplicativo 

```
flatpak install flathub com.visualstudio.code

```
<br>

<h3>🔺 Instalação Eclipse </h3>

🔹 <strong>1.</strong> Acessar o site oficial do [Eclipse](https://www.eclipse.org/downloads/)

🔹 <strong>2.</strong> Fazer o download do instalador, Extraia a pasta e execute arquivo "eclipse-inst".

🔹 <strong>3.</strong> Escolha segunda a opção: Eclipse IDE for Enterprise Java and Web Developers

🔹 <strong>4.</strong> Clique no folder da primeira opção (Java 17 + VM) e selecione o JDK que instalamos na nossa máquina

🔹 <strong>5.</strong> Mantenha as opções "create start menu entry" e "create desktop shortcut"

🔹 <strong>6.</strong> Install

🔹 <strong>7.</strong> Accept now

🔹 <strong>8.</strong> Launch

🔹 <strong>9.</strong> Pronto, intalação concluída

<br>

<h3>🔺 Instalação Docker PopOS ou Ubuntu </h3>


🔸 <strong>1.</strong> A Documentação do [Docker](https://docs.docker.com/engine/install/ubuntu/) pede para atualizar os indice do pacote apt

```
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
```

🔸​	<strong>1.2</strong> Adicione a chave GPG oficial do Docker: :

```
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

🔸​	<strong>1.3</strong> Use o seguinte comando para configurar o repositório:

```
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
🔸​	<strong>2.</strong> Atualize o aptíndice do pacote:

```
sudo apt-get update
```

🔸​	<strong>2.2</strong> Instale o Docker Engine, o containerd e o Docker Compose.

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
<h3> 3. Instalando Docker-Desktop </h3>

🔸​	<strong>3.1</strong> Dependencias para docker-desktop funcionar gnome-terminal, docker Engine, compose  e containerd no caso só falta gnome terminal:

```
sudo apt install gnome-terminal
```

🔸 <strong>3.2</strong> Faça dowload do pacote .deb no site do [Docker](https://docs.docker.com/desktop/install/ubuntu/), para instalar basta dar dois clicks e abrirá a loja para fazer a instalação, tão simples quanto windows ou em caso mais extremos botao direito do mouse e abrir com/ instalador de programas ou via comandos via terminal

```
sudo apt-get update
sudo apt-get install ./docker-desktop-<version>-<arch>.deb
```


<br>

 ======> [Reinaldo](https://www.linkedin.com/in/reinaldovitorcaetano/ "ReinaldoCaetano").
