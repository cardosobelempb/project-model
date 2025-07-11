# start 
 ```bash
 npx create-turbo@latest
 npx create-next-app@latest
 nest new backend

 npm i jest ts-jest tsup -D
 ```

 /**
✅ Correções possíveis
🔹 1. Se você só precisa do primeiro item da planilha:
{{ $('Planilha com os dados2').all()[0].json['Titulo referencia'] }}

🔹 2. Se você está dentro de um loop ou quer aplicar isso para cada item (ex: usando Set ou Code):
Use apenas:
{{ $json['Titulo referencia'] }}
Nesse caso, o dado já está acessível no contexto do item atual — não precisa referenciar outro node.

🔹 3. Se você quer todos os valores:
Se quiser uma lista de todos os títulos de referência:
{{ $('Planilha com os dados2').all().map(item => item.json['Titulo referencia']) }}
 
💡 Dica
Evite .item sempre que trabalhar com múltiplos registros. Prefira .all()[0], .map(...) ou, dentro de um nó que processa item por item, apenas $json.

Se quiser, me mostre como está seu fluxo (tipo de nó que usa essa expressão e o que quer fazer com o dado), e eu te passo a forma ideal.
 */