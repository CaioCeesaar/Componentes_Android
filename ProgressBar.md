# ProgressBar

É uma view gráfica que mostra algum processo. Ela pode ser usada para exibir o status de um trabalho sendo feito, como analisar ou baixar um arquivo. Existem dois tipos de Progressbar: determinada (duração fixa) e indeterminada (duração desconhecida). É possível personalizar a aparência da barra de progresso usando recursos xml

Temos dois tipos de progress bar, a circular e a horizontal (muito utilizada para demonstrar o progresso de download de um determinado arquivo, por exemplo)

### MinHeight/MinWidth

Definem a altura e a largura da barra de progresso

### Max

Define o valor máximo da barra de progresso

### Progress

Define o progresso padrão da barra de progresso, que pode ser definido de 0 a max

### Style

Define o estilo da barra de progresso, que pode ser horizontal ou circular

### Visibility

Atributo que define a visibilidade do componente, podendo ser visible, invisible ou gone

```kotlin
class MainActivity : AppCompatActivity() {

    private lateinit var binding: ActivityMainBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding = ActivityMainBinding.inflate(layoutInflater)
        setContentView(binding.root)

        setStatus()

binding.toggleButton.setOnCheckedChangeListener { _, _ ->
            setStatus()
        }

    }

    private fun setStatus() {

        binding.textStatus.text = if (binding.toggleButton.isChecked){
            binding.progressBar.isVisible = true
            "Ligado"
        } else {
            binding.progressBar.isVisible = false
            "Desligado"
        }
    }

}
```
