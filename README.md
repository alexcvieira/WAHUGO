Migração de um framework website para o Static Web Apps AZURE 

Neste exemplo nós vamos utilizar o framework GOHUGO para criar um website e em seguida migrá-lo para o static web apps junto ao AZURE, então vamos começar com o download do instalador Hugo 

 https://github.com/gohugoio/hugo/releases 

Em seguida vamos instalar o GOHUGO em um diretório de nossa preferência 
Obs.: Recomendamos não instalar junto a unidade C:\ do sistema operacional 

Em seguida vamos adicionar a variável junto ao editor de variável de ambiente Path >> Editar a variável de ambiente e adicionar o caminho aonde o .exe do produto está, em nosso caso D:\Alex\Hugo\bin 
Em seguida vamos abrir o PS como administrador e navegar até a pasta onde está o .exe do HUGO, no meu caso D:\Alex\Hugo\bin\ e vamos digitar o cmdlet abaixo para criamos não só o diretório como também nosso site 

Hugo new site ‘NAME_WEBSITE’ 

Em seguida vamos acessar o diretório aonde o app foi criado D:\Alex\Hugo\bin\WAHUGO\  

Agora vamos inicializar o repositório Git 

Git init 

Agora vamos adicionar um tema de preferência para o submódulo git e vamos especificar o mesmo no arquivo de configuração do HUGO 

git submodule add -b main https://github.com/nunocoracao/blowfish.git themes/blowfish 


Agora vamos confirmar as alterações com o cmdlet abaixo 

git add -A 

git commit -m "initial commit" 

Agora vamos enviar por push nosso aplicativo para o GitHub 

Adicione um repositório no Git de sua preferência e junto ao PowerShell vamos executar o cmdlet abaixo 

git remote add origin https://github.com/<YOUR_USER_NAME>/WAHUGO 

E agora vamos realizar um push do repositório local para o Git 
Obs.: Não crie um README junto ao novo repositório 

Git branch –M main 
git push --set-upstream origin main 

Implementar o website junto ao Static We App – Azure 

Após realizarmos um push e validarmos em nosso repositório vamos seguir com a criação e migração do nosso website para o ‘Static Web App’

Vá para o Portal do Azure
Selecione Criar um Recurso
Pesquise por Aplicativos Web Estáticos
Selecione Aplicativos Web Estáticos
Escolha Criar
 

 

 

 

 
