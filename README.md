# ProvaMagento2
> Instruções:  
> - Você tem 24h após a disponibilização do link para entregar sua da prova.    
> - Deverá seguir o roteiro conforme descrito e utilizar as últimas versões dos módulos disponibilizados no repositório.   
> - Pre-requisitos para rodar o magento 2.4.6: Php 8.1 e ElasticSearch  
> - ENTREGA: Disponibilizar um arquivo .zip com o código fonte da prova (se implementar tudo na pasta app, pode enviar somente ela e os arquivos do composer) e o dump do banco de dados

## Roteiro da Prova
#### 1. Instalação do Magento  
    1.1. Instalar Magento 2.4.6 via composer   
    1.2. Fazer o setup install  
    1.3. Criar um novo cliente  
    1.4. Criar um novo produto   
    
#### 2. Instalação de Módulos  
    2.1. Instalar e configurar Módulo de SMTP (mageplaza/module-smtp)  
    2.2. Instalar e configurar Módulo de Pagamento Shipay (shipay_pagamentos_digitais/shipay-magento-pix-qr-gateway)  
        2.2.1. Chaves  
            Access Key: B7vsMjHIyZ7CM7SiDcUUYw  
            Secret Key: Gj-d5Inp-aBiYybcbpWWKPYCkk-tnHJ38Ch3McJSUVgZUFgrxlNzEBRo8MltHVaZGukYeL-bZgMXdBFPq2IsqA  
            Client Id: tr6BsQAyQ3RcWy5HPLY1quMWXLv_VKuLMR0T7H613OQX1H00p3kpL9gzs3c744CiGEv6lWKQyfYPwLGSln-3SFcVt7HLNazro4atNA94se0ZbOKOZgOhnTO0tEtsOgsQqy4IwYdAzeK65z_SRqPYWb96CI0CBp3P0secCbur9kk  
        2.2.2. Fazer pedido de teste usando o pagamento Shipay  
        
#### 3. Customização Frontend  
    3.1. Criar um novo Template usando o template "Magento/luma" como parent  
    3.2. Configurar esse novo template para a loja  
    3.3. Customizar phtml de preço adicinando parcelamento em até 12x usando o valor final do produto no calculo  
    3.4. Remover o campo de busca do header usando layout xml  
    3.5. (DESAFIO)Fazer a customização do plugin de adição ajax de produto no carrinho "Magento_Catalog/js/catalog-add-to-cart" onde seja exibido um modal de confirmação de adição do produto no carrinho
        3.5.1. O modal precisa exibir no titulo a confirmação de adição do produto ao carrinho
        3.5.2. O modal precisa questionar o cliente se o mesmo deseja finalizar a compra ou continuar comprando
        3.5.3. Exibir dois botões um para continuar comprando leva para home e o de finalizar a compra leva para o carrinho
        3.5.4. Realizar a customização utilizando mixin para sobrepor apenas o método necessário do plugin e não todos os métodos do plugin
    
#### 4. Desenvolvimento Módulo  
    4.1. Criar Módulo Hello Word  
        4.1.1. Criar Módulo Básico com uma rota "helloworld"  
        4.1.2. Criar arquivo de layout xml para essa rota definir um arquivo .phtml que terá apenas os dizeres "Hello Word". O bloco utilizado pode ser o padrão "Magento\Framework\View\Element\Template"  
        4.1.3. Acessar a rota e validar a exibição do texto "Hello Word" corretamente e pelo arquivo .phtml definido  
