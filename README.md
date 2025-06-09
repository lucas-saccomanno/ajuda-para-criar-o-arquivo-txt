# Envio de E-mails Personalizados com Template

Este projeto permite enviar e-mails personalizados para uma lista de clientes usando um arquivo de template em texto (`.txt`) e uma planilha Excel com os dados dos clientes.

---

## Como escrever o arquivo TXT do template para envio de e-mails

O arquivo `.txt` funciona como um modelo para o e-mail, onde você pode colocar variáveis que serão substituídas pelos dados de cada cliente.

### Estrutura do arquivo `template.txt`

1. **Primeira linha:** título (assunto) do e-mail.  
2. **Demais linhas:** corpo do e-mail.

---

### Personalização com variáveis

Você pode usar variáveis dentro de `{{` e `}}`, que devem corresponder aos nomes das colunas na planilha Excel.

---

### Exemplo de `template.txt`

Pagamento em atraso - {{nome}}

Olá {{nome}}, tudo bem?

Estamos entrando em contato para informar que sua fatura de {{produto}} no valor de {{valor}} venceu no dia {{vencimento}}.

Caso já tenha efetuado o pagamento, por favor desconsidere este e-mail.

Atenciosamente,
Equipe XYZ

---

### Como funciona

- O programa substitui as variáveis pelo conteúdo da planilha para cada cliente.  
- O título (primeira linha) vira o assunto do e-mail.  
- O corpo (linhas seguintes) vira a mensagem do e-mail.

---

### Dicas importantes

- As variáveis `{{variavel}}` devem bater exatamente com o nome das colunas do Excel.  
- Salve o arquivo `.txt` em UTF-8 para evitar problemas com caracteres especiais.  
- Não use espaços dentro das chaves, ex: `{{nome}}` é correto, `{{ nome }}` pode causar erro.

---

## Estrutura da planilha Excel

- A planilha deve conter uma coluna `email` com os e-mails dos destinatários.  
- Outras colunas podem ser usadas para preencher as variáveis no template (ex: `nome`, `produto`, `valor`, `vencimento`).

---

## Como usar

1. Configure seu e-mail e senha de app no script (para Gmail, veja como gerar a senha de app no [tutorial oficial](https://support.google.com/mail/answer/185833?hl=pt-BR)).  
2. Coloque o arquivo `template.txt` e a planilha `.xlsx` na mesma pasta do script.  
3. Execute o script para enviar os e-mails personalizados.

---

## Dúvidas ou contribuições

Se tiver dúvidas ou quiser ajudar no projeto, abra uma issue ou envie um pull request.

---

Obrigado por usar o projeto!  
Lucas Saccomanno
