# Button

Inicialmente é importante lembrar de trabalhar com os componentes que já vem do material design, nesse caso, nosso código xml para inclusão do button seria:

`com.google.android.material.button.MaterialButton`

### Background

Para o background do botão, podemos usar a tag `android:background` e definir uma cor sólida ou um drawable. Também é possível usar o atributo `app:backgroundTint` para aplicar uma cor de fundo com efeito de sombreamento. 

### Padding

O padding do botão pode ser ajustado usando a tag `android:padding` e definindo um valor em pixels ou usando os atributos `app:paddingHorizontal` e `app:paddingVertical` para definir valores separadamente para o preenchimento horizontal e vertical. É importante lembrar de manter o padding do botão consistente com o resto da interface do usuário para garantir uma aparência coesa.

### Icones

Para adicionar um ícone ao botão, podemos usar a tag `app:icon` e definir um drawable. Também é possível usar o atributo `app:iconTint` para aplicar uma cor ao ícone. Se o ícone for adicionado, é importante lembrar de ajustar o padding do botão para que o texto não fique muito próximo ao ícone e garantir que a aparência geral seja equilibrada.

Podemos criar um ícone usando o vector asset do android studio dentro da pasta drawable.

`IconGravity` é um atributo que define a posição do ícone em relação ao texto do botão. Os valores possíveis incluem "start", "top", "end" e "bottom". Por exemplo, se definirmos `app:iconGravity="start"`, o ícone será exibido à esquerda do texto. O valor padrão é "textStart", que coloca o ícone à esquerda do texto em layout horizontal ou acima do texto em layout vertical.

### Click

Todo componente visível é passível de click

Usamos o seguinte código para mostrar um toast quando clicarmos no botão:

```kotlin
binding.button.setOnClickListener {
            Toast.makeText(this, "Enviado amigao", Toast.LENGTH_SHORT).show()
        }
```
