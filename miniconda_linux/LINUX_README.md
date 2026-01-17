## Commands to install miniconda
> ~ (this is commando to see it the directory that you are)
> ls -a 👀 Mostrar arquivos e pastas (inclusive ocultos)

> mkdir -p ~/miniconda3
```
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
O que acontece aqui 👇

wget → baixa arquivos da internet

URL → instalador oficial do Miniconda 3 (Linux 64-bit)

-O ~/miniconda3/miniconda.sh
→ salva o arquivo com o nome miniconda.sh dentro da pasta ~/miniconda3
```


### > bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
```
Esse comando faz uma instalação automática (silent) do Miniconda — ótima escolha 👍

bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3

O que cada flag significa 👇

-b (batch)
👉 instala sem perguntas (modo não interativo)

-u (update)
👉 atualiza uma instalação existente no mesmo diretório, se houver

-p ~/miniconda3 (prefix)
👉 define o diretório de instalação como ~/miniconda3
```



