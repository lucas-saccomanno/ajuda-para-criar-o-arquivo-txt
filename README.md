# Envio de E-mails Personalizados com Template

Este projeto permite enviar e-mails personalizados para uma lista de clientes usando um arquivo de template em texto (`.txt`) e uma planilha Excel com os dados dos clientes.

---

## Configuração do e-mail remetente e servidor SMTP

Você pode usar **qualquer tipo de e-mail** (Gmail, Outlook, Yahoo, empresa, etc). Para isso, é necessário configurar corretamente:

- **E-mail remetente**: seu endereço de e-mail completo.
- **Senha**: pode ser sua senha normal ou uma senha de app (recomendada para Gmail com 2FA).
- **Servidor SMTP**: endereço do servidor SMTP do seu provedor (ex: `smtp.gmail.com`, `smtp.office365.com`, etc).
- **Porta SMTP**: geralmente `587` para TLS, `465` para SSL, ou outra porta definida pelo provedor.
- **Tipo de conexão**: TLS, SSL ou sem criptografia.

---

## Sobre a senha de app

- Para contas Gmail com verificação em duas etapas (2FA), você deve usar uma **senha de app** gerada no painel do Google.  
- Para outros provedores, consulte o administrador ou o suporte para saber se precisa usar senha de app ou senha normal.

Tutorial para gerar senha de app no Gmail:
[https://support.google.com/mail/answer/185833?hl=pt-BR](https://support.google.com/mail/answer/185833?hl=pt-BR)
Link para a criaçâo da senha:
[https://myaccount.google.com](https://myaccount.google.com](https://myaccount.google.com/apppasswords?continue=https://myaccount.google.com/?hl%3Dpt_BR%26utm_source%3DOGB%26utm_medium%3Dact%26gar%3DWzEyMF0&rapt=AEjHL4M-FVCKwwJakvEFvQEpf03dw5cnvYQkSnZMSUu4OM1J_w5vquJ2HPpYLqUpBaisZdn9PujXenSwZDemRhjbcn5ncF3-I0Fr-122KtmJK9OnwN9cPbI))

---

## Como escrever o arquivo TXT do template para envio de e-mails

O arquivo `.txt` funciona como um modelo para o e-mail, onde você pode colocar variáveis que serão substituídas pelos dados de cada cliente.

### Estrutura do arquivo `template.txt`

1. **Primeira linha:** título (assunto) do e-mail.  
2. **Demais linhas:** corpo do e-mail.

### Personalização com variáveis

Você pode usar variáveis dentro de `{{` e `}}`, que devem corresponder aos nomes das colunas na planilha Excel.

### Exemplo de `template.txt`

Pagamento em atraso - {{nome}}

Olá {{nome}}, tudo bem?

Estamos entrando em contato para informar que sua fatura de {{produto}} no valor de {{valor}} venceu no dia {{vencimento}}.

Caso já tenha efetuado o pagamento, por favor desconsidere este e-mail.

Atenciosamente,
Equipe XYZ

---

## Estrutura da planilha Excel

- A planilha deve conter uma coluna `email` com os e-mails dos destinatários.  
- Outras colunas podem ser usadas para preencher as variáveis no template (ex: `nome`, `produto`, `valor`, `vencimento`).

---

## Como usar

1. Configure seu e-mail, senha, servidor SMTP, porta e tipo de conexão na interface ou no script.  
2. Coloque o arquivo `template.txt` e a planilha `.xlsx` na mesma pasta do script.  
3. Execute o script para enviar os e-mails personalizados.

---

## Dúvidas ou contribuições

Se tiver dúvidas ou quiser ajudar no projeto, abra uma issue ou envie um pull request.

---

Obrigado por usar o projeto!  
Lucas Saccomanno
