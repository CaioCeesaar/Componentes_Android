# TextView

TextView é um componente de interface do usuário que exibe texto em aplicativos Android

Atribuímos ids aos componentes que serão usados programaticamente

### Android:text x tools:text

O atributo `android:text` é usado para definir o texto exibido pelo TextView em tempo de execução, enquanto o atributo `tools:text` é usado apenas para fins de visualização no layout do Android Studio e não é exibido em tempo de execução.

### textSize

O atributo `textSize` é usado para definir o tamanho do texto exibido pelo TextView. Ele pode ser definido em unidades de pixels (por exemplo, `20sp`, é o mais recomendado) ou em unidades dimensionais independentes de densidade (por exemplo, `20dp`), o que permite que o tamanho do texto se adapte a diferentes densidades de tela

### textColor

O atributo `textColor` é usado para definir a cor do texto exibido pelo TextView. Ele pode ser definido usando um valor de cor específico (por exemplo, `#FF0000` para vermelho) ou usando um recurso de cor definido no arquivo `colors.xml`. Também é possível definir a cor do texto para mudar quando o TextView estiver em um estado diferente, como quando estiver selecionado ou pressionado.

### Setar o texto programaticamente em kotlin

Para definir o texto de um TextView programaticamente em Kotlin, podemos usar a propriedade `text` do componente. Por exemplo, se tivermos um TextView com id `myTextView`, podemos definir o texto da seguinte maneira:

```
val textView = findViewById<TextView>(R.id.myTextView)
textView.text = "Meu texto programático"

```

Dessa forma, o texto do TextView será "Meu texto programático". É importante lembrar que para definir o texto programaticamente, devemos primeiro obter uma referência ao componente usando o método `findViewById`. 

### Font Custom

Para baixar uma fonte podemos usar o site dafont.com, após baixar o arquivo de fonte do site, é necessário formatar o seu nome, colocando apenas letras minúsculas e sem caracteres especiais.

Criar um diretório font dentro do res, copiar e colar o arquivo de fonte que foi baixado e usar o atributo fontFamily dentro do nosso textView

### Build

É importante usar do build caso esteja com problemas no projeto
