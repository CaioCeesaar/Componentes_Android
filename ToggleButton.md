# ToggleButton
É conhecido também como botão de alternância, ele permite aos usuários alternar entre dois estados diferentes. São amplamente utilizados em interfaces de usuário para fornecer uma maneira rápida e fácil para os usuários alternarem entre opções e preferências, sem precisar acessar menus ou configurações adicionais. 

### textOn

Define o texto que será exibido no botão quando ele estiver no estado “ligado”.

### textOff

Define o texto que será exibido no botão quando ele estiver no estado “desligado”.

→ Esses textos geralmente é uma palavra, frase ou ícone que indica o que o botão faz quando está em seu estado atual. Esses atributos são especialmente úteis para dar mais clareza aos usuários sobre a ação que será executada quando o botão é pressionado. Eles ajudam a tornar a interface do usuário mais intuitiva e fácil de usar. Além disso, também podem ser usados para a acessibilidade de usuários com deficiência visual, permitindo que um leitor de tela leia o texto para o usuário.

```kotlin
class MainActivity : AppCompatActivity() {

    private lateinit var binding: ActivityMainBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
binding= ActivityMainBinding.inflate(layoutInflater)
        setContentView(binding.root)

        setStatus()

        binding.toggleButton.setOnCheckedChangeListener { _, _ ->
            setStatus()
        }

    }

    private fun setStatus() {
binding.textStatus.text= if (binding.toggleButton.isChecked){
            "Ligado"
        } else {
            "Desligado"
        }
    }
}
```
