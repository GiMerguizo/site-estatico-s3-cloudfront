# Criando Sites Estáticos com Amazon S3 e CloudFront
Repositório para entrega do Projeto Prático da [DIO](https://web.dio.me/home) - _Atualizado em 18/07/2023_

## Serviços utilizados
- Amazon S3
- CloudFront

## S3
### Criando um bucket
- Criar um bucket no S3 
    - Manter as configurações padrões
- Fazer o upload dos arquivos

Bucket criado: cloudfront-site-receita

## Cloudfront
### Configurações
- Abrir o Cloudfront
- Criar uma distribuição
    - Apontar para o bucket criado
    - **Origin Access** 
        - Legacy access identities
        - Yes, update the bucket policy
        - Permite que o cloudfornt acesse as páginas
    - **Default cache behavior**
        - Redirect HTTP to HTTPS

- Acesso ao bucket somente pelo cloudfront
- Testar o _Domain Name_ => vai dar erro (Access Denied)

#### Editar as configurações
**Default root object**
- index.html
- Testar novamente o domínio

### Páginas de erro
Entrar no cloudfront criado > Error Pages > Create custom error response
- Customizar os erros

## Referências
- [Curso - DIO](https://web.dio.me/lab/criando-sites-estaticos-com-amazon-s3-e-cloudfront/)
- [Repositório no GitHub](https://github.com/cassianobrexbit/dio-live-cloudfront)