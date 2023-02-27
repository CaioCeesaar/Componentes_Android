# Switch

Permite aos usuário alternarem entre duas opções ou estados. É uma forma comum de entrada em muitos aplicativos e telas de configuração do sistema operacional.

### Checked

É uma propriedade do swirtch que indica se o estado atual do switch está ativado (checked) ou desativado (unchecked). Quando o switch está ativado essa propriedade é definida como true; quando está desativado é definida como false.

### ThumbTint

Permite definir a cor do botão deslizante (thumb) que é usado para alternar entre os estados ativado e desativado. Isso pode ser feito usando um recurso de cor ou um valor hexadecimal que representa uma cor

### TrackTint

Permite definir a cor da trilha (track) que é usada para indicar o estado atual do switch. Isso também pode ser feito usando um recurso de cor ou um valor hexadecimal

### setOnCheckedChangeListener

É usado para definir um listener que é chamado sempre que o estado do switch é alterado pelo usuário. Quando o usuário altera o estado do switch, o método onCheckedChanged é chamado com dois parâmetros: o switch que foi alterado e o novo estado (true ou false). Isso permite que o programador execute ações específicas com base no estado atual do switch, como desativar ou ativar recursos ou opções dentro do aplicativo.

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding = ActivityMainBinding.inflate(layoutInflater)
        setContentView(binding.root)

        setStatus() // Chamada para já mostrar a mensagem ativado/desativado na primeira execução

        binding.switchMaterial.setOnCheckedChangeListener { _, _ ->
            setStatus()
        }

    }

    private fun setStatus(){
        binding.textStatus.text = if (binding.switchMaterial.isChecked) {
            "Ativado"
        } else {
            "Desativado"
        }
    }
```
