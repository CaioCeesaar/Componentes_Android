# ImageView

É o componente responsável por mostrar imagens ao usuário

Ao arrastar a imageView para o design, o android studio vai abrir a tela de pick a resource

### Src

É usado para definir a imagem que será exibida na imageView. Ele pode receber um recurso de imagem como PNG, JPEG ou GIF, ou uma URL de imagem na interner

### adjustViewBounds

É usado para ajustar o tamanho da imageView de acordo com o tamanho da imagem. Quando seu valor é definido como true, a imageView ajusta seu tamanho para corresponder ao tamanho da imagem, mantendo a proporção original da imagem. Isso é útil para garantir que imagem seja exibida corretamente, independentemente do tamanho da tela ou da densidade de pixels

### ScaleType

É usado para definir como a imagem é dimensionada para se ajustar à imageView. Existem várias opções de escalonamento disponívels, incluindo:

- CENTER: A imagem é centralizada na ImageView sem ser dimensionada.
- CENTER_CROP: A imagem é redimensionada para preencher a ImageView, mantendo a proporção original. Isso pode resultar em partes da imagem sendo cortadas.
- CENTER_INSIDE: A imagem é dimensionada para caber inteiramente dentro da ImageView, mantendo a proporção original. Isso pode resultar em barras pretas nas laterais ou no topo e na parte inferior da imagem.
- FIT_CENTER: A imagem é dimensionada para caber inteiramente dentro da ImageView, mantendo a proporção original. Isso pode resultar em barras pretas nas laterais ou no topo e na parte inferior da imagem.
- FIT_START: A imagem é dimensionada para caber inteiramente dentro da ImageView, mantendo a proporção original. Isso pode resultar em barras pretas nas laterais ou no topo da imagem.
- FIT_END: A imagem é dimensionada para caber inteiramente dentro da ImageView, mantendo a proporção original. Isso pode resultar em barras pretas na parte inferior e nas laterais da imagem.
- FIT_XY: A imagem é redimensionada para preencher a ImageView, não mantendo a proporção original. Isso pode distorcer a imagem.

### Como alterar a imagem de uma imageView a partir de um botão? 

Para isso, podemos usar o método `setImageResource(id)` e passar no id a imagem que se deseja apresentar na imageView.

```kotlin
  binding.botao.setOnCLickListener {
    binding.imageView.setImageResource(R.drawable.imagem_desejada)
  }
```
