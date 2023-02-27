# RadioButton

Permite selecionar uma única opção em um conjunto de opções mutuamente exclusivas. Quando o usuário seleciona um RadioButton em um grupo, o RadioButton anteriormente selecionado é desmarcado automaticamente.

Exemplo: selecionar tamanho de um produto, em que só podemos marcar uma caixinha com determinado valor.

Os radioButtons são agrupados em um componente chamado de RadioGroup. O RadioButton só funciona de maneira adequada quando estão envolvidas por um RadioGroup.

É importante criar um id para cada um, tanto para o radioGroup tanto para os radioButtons

### Utilizando o RadioButton na prática:

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    binding = ActivityMainBinding.inflate(layoutInflater)
    setContentView(binding.root)

    binding.radioGroup.setOnCheckedChangeListener { _, id ->
        when (id) {
            R.id.rdOpcao1 -> {
                Log.i("INFOTESTE", "Opção 1")
            }
            R.id.rdOpcao2 -> {
                Log.i("INFOTESTE", "Opção 2")
            }
            else -> {
                Log.i("INFOTESTE", "Opção 3")
            }
        }
    }
}
```

Através dessa função podemos obter via Log o que foi marcado.
