# <h1 align="center"> Instalação docker para iniciantes (LINUX) </h1>
<p>Esse manual foi feito para instalação do docker da maneira que a certificação pede. Existe o script de conveniência, instalação por .deb ou .rpm e essa que é incluíndo os pacotes e depois baixando do repositório.</p>
<ol>
<li>Remova qualquer instalação docker:</li>
<dd>sudo apt-get remove docker docker-engine docker.io containerd runc</dd>
<li>Atualizar a lista de pacotes:</li>
<dd>sudo apt uptade</dd>
<li>Baixando pacotes necessários:</li>
<dd>sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release -y</dd>
<li>Verificar se foi para a sources list:</li>
<dd>ls -l /etc/apt/souces.list.d</dd>
<li>Atualizar a lista de pacotes:</li>
<dd>sudo apt update</dd>
<li>Instalar o docker e seus pacotes:</li>
<dd>sudo apt-get install docker-ce docker-ce-cli containerd.io
</dd>
<li>Varificar se foi instalado:</li>
<dd>docker system info</dd>
<dd>Obs: Por padrão o usuário local não é insediro ao grupo docker, então o Server terá uma mensagem de erro de permissão</dd>
<li>Corrigindo a mensagem de erro do Server adicionando o usuário local ao grupo docker:</li>
<dd>sudo usermod -aG docker $USER</dd>
<li>Verificar se foi adicionado corretamente:</li>
<dd>getent group docker</dd>
<li>Reiniciar o linux</li>
<li>Habilitando o docker:</li>
<dd>sudo systemctl enable docker && sudo systemctl start</dd>
</ol>