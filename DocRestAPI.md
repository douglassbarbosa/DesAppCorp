Documentação da API REST QrCode API
====================================

A API REST dessa alicação é uma demosntração da Aplicação que esta sendo desenvolvida para TCC do curso de Sistemas da Informação,
essa é uma versão pública com as requisições: GET, POST, PUT e DELETE no endpoint `/usuario/` Esta API não requer autenticação.

## Usuários
----------
O recurso Usuários representa uma demonstração de como o Usuário será cadastrado.


    Propriedade - Descrição
    ============== 
    id - O identificador exclusivo pelo qual identificar o usuário
    nome - O nome do usuário, definido no cadastro
    tituloQrcode - O título do Qr Code 
    imgQrcode - A url da imagem do Qr Code, gerada no cadastro do mesmo
    tituloConteudo - O Título do conteúdo associado ao Qr Code, na versão completa poderá ter mais de um conteúdo dinâmico para o mesmo Qr Code
    descricaoConteudo - A descrição do conteúdo.
    linkConteudo - Link externo 
    ==============   ===============


## Listar Usuários

### GET

`/usuarios`

Retorna uma lista de todos os usuários cadastrados

`/usuarios`

     [
        {
            "id": 1,
            "nome": "Douglas Barbosa",
            "tituloQrcode": "Casa de Praia",
            "imgQrcode": "folder_default/img_qrcode00001.png",
            "tituloConteudo": "Ar condicionado Inteligente",
            "descricaoConteudo": "Para usar o arcondicionado inteligente é necessário instalar o App Samsung Home",
            "linkConteudo": "store.google.com/samsungHome.apk"
        },
        {
            "id": 3,
            "nome": "Carla",
            "tituloQrcode": "Wi-fi para Hóspedes",
            "imgQrcode": "folder_default/img_qrcode00004.png",
            "tituloConteudo": "Primeiro Acesso",
            "descricaoConteudo": "Rede: Pousada Maria Mariah - Senha: Número do seu Quarto + Mês atual no formato MM",
            "linkConteudo": "www.posadamariamariah.com/guiaDeUsuario"
        },
        {
            "id": 5,
            "nome": "Edu",
            "tituloQrcode": "Montagem Fácil",
            "imgQrcode": "folder_default/img_qrcode00002.png",
            "tituloConteudo": "Mesa de computador",
            "descricaoConteudo": "Ferramentas Necessárias: Chave de Fendas 5 e 8",
            "linkConteudo": "www.youtube.com/cs9856saxs"
        },
        {
            "id": 6,
            "nome": "Carla",
            "tituloQrcode": "Wi-fi para Hóspedes",
            "imgQrcode": "folder_default/img_qrcode00004.png",
            "tituloConteudo": "Primeiro Acesso",
            "descricaoConteudo": "Rede: Pousada Maria Mariah - Senha: Número do seu Quarto + Mês atual no formato MM",
            "linkConteudo": "www.posadamariamariah.com/guiaDeUsuario"
        }
    ]



## Cadastrar Usuário

### POST
`/usuarios`

Cadastra um usuário e seu QrCode. 
**Parâmetros: Body - raw - JSON**


    {
        "nome": "Carla",
        "tituloQrcode": "Wi-fi para Hóspedes",
        "imgQrcode": "folder_default/img_qrcode00004.png",
        "tituloConteudo": "Primeiro Acesso",
        "descricaoConteudo": "Rede: Pousada Maria Mariah - Senha: Número do seu Quarto + Mês atual no formato MM",
        "linkConteudo": "www.posadamariamariah.com/guiaDeUsuario"
    }




## Deletar Usuário

`DELETE /usuarios/2`

Exclui o usuário e todo o seu QrCode, retorna STATUS 200



## Atualizar o Usuário

`PUT /usuarios/5`

Atualiza o usuário e retorna o usuaário atualizado


    { 
        "nome": "Eduardo Barbosa",
        "tituloQrcode": "Montagem Fácil",
        "imgQrcode": "folder_default/img_qrcode00002.png",
        "tituloConteudo": "Mesa de computador",
        "descricaoConteudo": "Ferramentas Necessárias: Chave de Fendas 5 e 8",
        "linkConteudo": "www.youtube.com/cs9856saxs"
    }




