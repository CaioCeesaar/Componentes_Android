# EditText

É um componente de interface que permite ao usuário inserir e editar texto. É usado para coletar informações de entrada do usuário em formulários, caixas de diálogo e outros elementos da interface do usuário

### InputType

Define o tipo de entrada de texto que é permitido dentro do componente EditText. Por exemplo, o inputType pode ser definido para aceitar apenas números, texto normal ou um endereço de e-mail

### Text

É o texto que é exibido dentro do componente, esse texto pode ser apagado pelo usuário do aplicativo.

### Hint

É o texto que é exibido dentro do componente EditText quando ele está vazio, serve para indicar ao usuário o tipo de informação que se espera ali dentro.

### Digits

É usado para especificar quais caracteres são permitidos como entrada de texto. É normalmente usado com o atributo inpotType para restringir o tipo de entrada permitida pelo componente EditText.

### MaxLenght

Define o comprimeiro máximo do texto que pode ser inserido no componente EditText

### OnFocusChangeListener

Define um listener que é acionado quando o componente EditText ganha ou perde o foco.

### Exemplo de código:

No exemplo abaixo, ao clicar no botão da tela, o email digitado pelo usuário no editText será enviado como toast.

```kotlin
binding.button.setOnClickListener {
            val email = binding.editText.text.toString()
            Toast.makeText(this, email, Toast.LENGTH_SHORT).show()
        }
```
