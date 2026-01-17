## Commands to install miniconda
```
→ ~ (this is commando to see it the directory that you are)
→ ls -a 👀 Mostrar arquivos e pastas (inclusive ocultos)
→ mkdir -p ~/miniconda3

Esse comando:
mkdir -p ~/miniconda3
O que ele faz 👇
mkdir → cria diretórios
-p → cria os diretórios pais automaticamente (se não existirem) e não dá erro se a pasta já existir
~ → representa o diretório home do usuário (ex: /home/seu_usuario)
miniconda3 → nome da pasta que será criada
📁 Resultado:
/home/seu_usuario/miniconda3
Quando usar -p?
Exemplo:
mkdir -p ~/apps/python/miniconda3
Isso cria toda a estrutura:
apps/
└── python/
    └── miniconda3/
```


### > wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
```
→ O que acontece aqui 👇

→ wget → baixa arquivos da internet

→ URL → instalador oficial do Miniconda 3 (Linux 64-bit)

-O ~/miniconda3/miniconda.sh
→ salva o arquivo com o nome miniconda.sh dentro da pasta ~/miniconda3
```


### > bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3 (Instalando)
```
→ Esse comando faz uma instalação automática (silent) do Miniconda — ótima escolha 👍

→ bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3

→ O que cada flag significa 👇

-b (batch)
👉 instala sem perguntas (modo não interativo)

-u (update)
👉 atualiza uma instalação existente no mesmo diretório, se houver

-p ~/miniconda3 (prefix)
👉 define o diretório de instalação como ~/miniconda3
```


### > rm ~/miniconda3/miniconda.sh (Removendo)
```
→ Removendo o arquivo
```


### > rm ~/miniconda3/miniconda.sh (Ativando o conda)
```
→ Ativando o conda python - source ~/miniconda3/bin/activate
→ conda -h
→ conda search python → Busca versões disponíveis do Python no conda.

→ conda create -n ambiente python=3.10
→ conda create -n ambiente python=3.8


→ conda activate ambiente # Ativando o env ambiente
→ conda deactivate
→ conda env remove --name <env_name>






conda create -n snow python=3.10

# Instalar dentro do env ambiente 
pip install jupyter


**rm ~/miniconda3/miniconda.sh**


# python -m ipykernel install --user --name ambiente --display-name "my_jupyter"
python -m ipykernel install --user --name ambiente

Installed kernelspec ambiente in /root/.local/share/jupyter/kernels/ambiente
jupyter notebook --allow-root


Jupyter notebook support, interactive programming and computing that supports Intellisense, debugging and more.
This extension is enabled in the Remote Extension Host because it prefers to run there. Learn More


Visual Code
=> You will need to configure the installation of the plugin notebook, and after that, change your environment to the correct one.

```
