# Emporio-da-cidade.
Projeto de aplicação de uma venda virtual, com o objetivo de explorar os principais recursos da tecnologia e como integrá-las de maneira produtiva e eficiente para o cliente. O projeto é construído durante os cursos Desenvolvimento de Software, pelos alunos de ADS na Univerdsidade São Francisco Polo Itatiba.

# Desenvolvedores

Ana Larysa Silva Lima

Daniel Petroni

Léo da Silva Quallio
  
# Tecnologia usada - BACKEND
• Java com Spring, Jpa e hibernate.

• Postgres como banco de dados. 

# Tecnologia usada - FRONTEND
• Flutter.


# Como Iniciar o projeto 



Com o node instalado, abra o seu terminal (Linux) ou o seu PowerShell (Windows) e navegue até a pasta onde você quer copiar o site em questão. Execute o comando:

npm install website-scraper website-scraper-puppeteer

Ele vai instalar as bibliotecas website-scraper e website-scraper-puppeteer através do npm na sua máquina.
Agora, crie um arquivo index.js nesta mesma pasta onde o comando acima foi executado, adicione o seguinte código Javascript e substitua a URL do site que você quer baixar/copiar/clonar, assim como a pasta onde você quer que os arquivos sejam salvos.

	const scrape = require('website-scraper');
	const PuppeteerPlugin = require('website-scraper-puppeteer');
	const path = require('path');
	

	scrape({
	    // Forneça a URL do site que você quer copiar
	    urls: ['https://github.com/Analarysa/Emporio-da-cidade.git.'],

	

	    // Especifique a pasta onde os arquivos do site serão salvos em pasta-do-site
	    directory: path.resolve(__dirname, 'pasta-do-site'),
	    
	    // carregue o plugin do Puppeteer
	    plugins: [ 
	        new PuppeteerPlugin({
	            launchOptions: { 
	                headless: true
	            },
	            scrollToBottom: {
	                timeout: 10000, 
	                viewportN: 10 
	            }
	        })
	    ]
	});
  

Código Javascript para baixar os arquivos HTML, CSS, Javascript e HTML de um site na internet de forma automática.
Agora volte para o terminal (ou PowerShell) e rode o script que você acabou de criar usando:

node index.js

O script vai baixar o site completo (em HTML), assim como seus arquivos Javascript e CSS para o seu computador.
