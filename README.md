Laboratório: importação de XML no Pentaho Data Integration
Projeto experimental para testar o fluxo de importação de arquivos XML compatíveis com o Pentaho Data Integration (PDI) no Spoon.
> **Status:** experimento de laboratório, sem garantia de produção. Este projeto parte do pacote **PDI CE 9.4.0.0-343**. Não é uma versão oficial do Pentaho nem uma atualização para PDI 10.
O que foi modificado
Foi adicionado à barra do Spoon um botão Importar XML, ligado à ação nativa de importação do PDI (`spoon.importFileFromXML()`). As etapas, imagens e demais arquivos da distribuição original foram mantidos.
O botão abre a importação nativa do Pentaho para arquivos XML de jobs e transformações PDI. Ele não interpreta XML de qualquer sistema nem cria automaticamente um job Pentaho a partir de um formato arbitrário. A geração automática de job representada na imagem é apenas uma proposta de interface, não uma função implementada.
Prévia da interface
A imagem abaixo é um mockup conceitual, não uma captura de uma execução funcional. Ela está incluída em `docs/images/pdi-xml-import-mockup.png`.
![Mockup conceitual da interface Spoon com opção de importar XML](https://private-us-east-1.manuscdn.com/sessionFile/7ITTqjmRCibydVqcKN9UUc/sandbox/ZhisE328wMFp3iCNb7pcFz-images_1794704124696_na1fn_L2hvbWUvdWJ1bnR1L3BkaS1jZS14bWwtbGFiL2RvY3MvaW1hZ2VzL3BkaS14bWwtaW1wb3J0LW1vY2t1cA.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvN0lUVHFqbVJDaWJ5ZFZxY0tOOVVVYy9zYW5kYm94L1poaXNFMzI4d01GcDNpQ05iN3BjRnotaW1hZ2VzXzE3OTQ3MDQxMjQ2OTZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzQmthUzFqWlMxNGJXd3RiR0ZpTDJSdlkzTXZhVzFoWjJWekwzQmthUzE0Yld3dGFXMXdiM0owTFcxdlkydDFjQS5wbmciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTYwODMyMDB9fX1dfQ__&Key-Pair-Id=K2QY5QTL8JSY6C&Signature=MEQCIAl6yDLCavxu9ldRqIe6G~w8l1MUrEgZXXJWSjIuRegEAiBxJjHI1hP-ZetW1fc7dw306A5BUVg6Mhfi~xFiwQKI~g__)
Como executar
Baixe ou extraia o pacote customizado em uma pasta nova.
Instale e configure uma versão de Java compatível com a distribuição PDI 9.4.
Inicie o Spoon:
Windows: execute `data-integration/Spoon.bat`.
Linux: entre em `data-integration` e execute `chmod +x spoon.sh && ./spoon.sh`.
macOS: abra `data-integration/Data Integration.app`, se disponível na distribuição.
No Spoon, use o botão Importar XML e selecione um arquivo exportado pelo Pentaho.
Confira o job ou a transformação importada antes de executar. Teste primeiro com dados descartáveis e sem credenciais de produção.
Arquivo XML de teste
Adicione ao repositório um XML de exemplo que você tenha autorização para compartilhar, por exemplo em `examples/job-exemplo.xml`. Atualize este README com o nome real do arquivo e com a origem do exemplo.
Não inclua senhas, tokens, dados pessoais, endereços de bancos de produção ou outros segredos no XML. Use credenciais de laboratório e substitua dados sensíveis por valores fictícios.
Estrutura sugerida do repositório
```text
.
├── README.md
├── docs/
│   └── images/
│       └── pdi-xml-import-mockup.png
├── examples/
│   └── job-exemplo.xml       # adicionar XML de teste autorizado
└── patches/
    └── spoon.xul             # alteração de interface, se optar por publicar o patch
```
Publicação e distribuição
Este repositório é independente e não é afiliado, aprovado ou mantido pela Pentaho ou pela Hitachi Vantara. “Pentaho” e “Pentaho Data Integration” são mencionados apenas para identificar o software de origem.
Antes de publicar uma cópia do pacote completo, confira a licença aplicável a cada componente incluído e preserve os avisos de direitos autorais, licenças e atribuições da distribuição original. A distribuição contém componentes de terceiros com termos próprios. A licença Apache 2.0 do PDI não concede direitos sobre marcas registradas.
Uma opção mais simples para um repositório público é publicar o patch (`spoon.xul`), este README, a imagem conceitual e um XML de teste autorizado, e instruir cada pessoa a obter o PDI original por uma fonte autorizada. Se optar por distribuir o pacote completo, prefira um artefato de Release em vez de adicionar o ZIP de aproximadamente 368 MB ao histórico Git normal; verifique também os termos de cada componente antes de anexá-lo.
Créditos e licenças
Base: Pentaho Data Integration Community Edition 9.4.0.0-343, fornecido pelo responsável pelo laboratório.
Customização do Spoon: botão de acesso direto à importação nativa de XML.
Autor da proposta de interface: André Moura.
Consulte `data-integration/LICENSE.txt`, `data-integration/PentahoDataIntegration_OSS_Licenses.html` e os avisos contidos na distribuição para as licenças e atribuições dos componentes.
Limitações conhecidas
A customização aqui descrita acrescenta um atalho para a importação nativa do Pentaho; não implementa conversão genérica de XML.
O mockup não comprova execução nem compatibilidade com um XML específico.
A versão do mecanismo continua sendo a distribuição base 9.4.0.0-343.
Teste a importação no seu ambiente e com uma cópia de segurança antes de usar jobs importantes.
