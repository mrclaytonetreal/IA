# IA
Tudo sobre IA Inteligencia Artificial

Manual: Como Rodar o DeepSeek GRÁTIS na Sua Máquina!
Autor: claytonet

O que é o DeepSeek-R1?
O DeepSeek-R1 é um modelo de linguagem de grande escala desenvolvido pela startup chinesa DeepSeek. Este modelo de primeira geração destaca-se por suas capacidades de raciocínio avançadas, alcançando desempenho comparável ao OpenAI-o1 em tarefas de matemática, codificação e raciocínio lógico. Uma característica notável do DeepSeek-R1 é sua eficiência, alcançando alta performance com um orçamento significativamente menor em comparação com outros modelos de ponta. Além disso, o modelo é gratuito e de código aberto, permitindo que desenvolvedores em todo o mundo o utilizem e personalizem conforme necessário.

Instalando o Ollama
O Ollama é uma plataforma que permite executar modelos de linguagem de grande escala localmente em sua máquina, oferecendo maior controle e privacidade. A seguir, apresentamos o processo de instalação para diferentes sistemas operacionais.

Para macOS
Instale o Homebrew (caso ainda não o tenha):

sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
Instale o Ollama:

sh
brew install ollama
Este comando baixará e instalará o Ollama a partir do repositório Homebrew.

Verifique a instalação:

sh
ollama --version
Este comando deve retornar a versão instalada do Ollama, confirmando que a instalação foi bem-sucedida.

Para Windows
Baixe o instalador para Windows:
Acesse o site oficial do Ollama e clique em “Download for Windows”.

Execute o instalador:
Abra o arquivo baixado e siga as instruções do assistente de instalação.

Verifique a instalação:
Abra o Prompt de Comando e digite:

sh
ollama --version
Se a versão do Ollama for exibida, a instalação foi concluída com sucesso.

Para Linux
Atualize os pacotes do sistema:

sh
sudo apt update && sudo apt upgrade -y
Instale as dependências necessárias:

sh
sudo apt install -y curl
Baixe e execute o script de instalação do Ollama:

sh
curl -fsSL https://ollama.com/install.sh | sh
Este comando detectará automaticamente a arquitetura do seu sistema e instalará a versão apropriada do Ollama.

Verifique a instalação:

sh
ollama --version
Este comando deve retornar a versão instalada do Ollama, confirmando que a instalação foi bem-sucedida.

Executando o modelo DeepSeek-R1 de 14B no Ollama
Após instalar o Ollama, você pode executar o modelo DeepSeek-R1 de 14 bilhões de parâmetros seguindo os passos abaixo:

Baixe o modelo DeepSeek-R1:

sh
ollama pull deepseek-r1:14b
Este comando fará o download do modelo especificado para o seu sistema.

Execute o modelo:

sh
ollama run deepseek-r1:14b
Isso iniciará uma sessão interativa onde você pode inserir prompts e receber respostas do modelo.

Para mais informações e suporte, visite o repositório oficial do Ollama no GitHub.

O que é o Open WebUI?
O Open WebUI é uma interface web de código aberto, auto-hospedada e rica em recursos, projetada para operar modelos de linguagem de grande escala (LLMs) localmente. Compatível com APIs semelhantes à OpenAI e integrando-se perfeitamente com o Ollama, o Open WebUI oferece uma plataforma intuitiva para interagir com modelos como o DeepSeek-R1. Sua interface amigável facilita a experimentação e o desenvolvimento de aplicações baseadas em LLMs. (docs.openwebui.com)

Instalando o Open WebUI
A instalação do Open WebUI pode ser realizada de duas maneiras principais: utilizando o Docker ou através de uma instalação manual. A seguir, detalharemos ambos os métodos.

Instalação via Docker
Pré-requisitos:

Docker instalado em seu sistema.

Baixe e execute a imagem Docker do Open WebUI:

sh
docker run -d -p 3000:8080 -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama
Este comando baixa a imagem do Open WebUI com suporte integrado ao Ollama e a executa em um contêiner Docker. A aplicação ficará acessível em http://localhost:3000

Explicação dos parâmetros:

-d: Executa o contêiner em segundo plano (modo “detached”).
--network=host: Utiliza a rede do host, permitindo que o contêiner acesse serviços em execução no host diretamente.
-v open-webui:/app/backend/data: Monta um volume chamado open-webui para persistência de dados.
--name open-webui: Nomeia o contêiner como open-webui.
--restart always: Garante que o contêiner seja reiniciado automaticamente em caso de falha.
ghcr.io/open-webui/open-webui:main: Especifica a imagem do Open WebUI a ser utilizada.
Acesse a interface web:

Abra seu navegador e navegue até http://localhost:3000/. No primeiro acesso, será solicitado que você crie uma conta de administrador fornecendo um nome, e-mail e senha.

Integrando o Open WebUI com o Ollama para Executar o Modelo DeepSeek-R1
Após instalar o Open WebUI e o Ollama, você pode configurar o ambiente para executar o modelo DeepSeek-R1 de 14 bilhões de parâmetros.

Passos:

Baixe o modelo DeepSeek-R1:

sh
ollama pull deepseek-r1:14b
Este comando faz o download do modelo especificado para o seu sistema.

Configure o Open WebUI para reconhecer o modelo:
No Open WebUI, vá até a seção de modelos e adicione o modelo deepseek-r1:14b à lista de modelos disponíveis.

Selecione o modelo e comece a interagir:
Na interface do Open WebUI, selecione o modelo DeepSeek-R1 e comece a inserir prompts para receber respostas geradas pelo modelo.

Pronto! Agora você está equipado para explorar o poder do modelo DeepSeek-R1 utilizando o Open WebUI integrado ao Ollama em seu sistema. Lembre-se de experimentar diferentes comandos e configurações para obter o máximo dessa ferramenta poderosa.
