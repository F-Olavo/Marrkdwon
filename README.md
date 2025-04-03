
##Francisco Olavo da Silva Filho   3° DS-A


```html
<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatorial e Número Primo</title>
</head>

<body>
    <h2>Calculadora de Fatorial e Verificador de Número Primo</h2>

    <!-- Campo de entrada para o usuário digitar um número -->
    <label for="numero">Digite um número:</label>
    <input type="number" id="numero">

    <!-- Botão que chama a função calcular ao ser clicado -->
    <button onclick="calcular()">Calcular</button>

    <!-- Parágrafo onde será exibido o resultado -->
    <p id="resultado"></p>

    <script>
        // Função recursiva para calcular o fatorial de um número
        function calcularFatorial(n) {
            if (n === 0) { 
                return 1; // O fatorial de 0 é sempre 1
            } else {
                return n * calcularFatorial(n - 1); // Chamada recursiva para calcular o fatorial
            }
        }

        // Função para verificar se um número é primo
        function verificarNumeroPrimo(numero) {
            if (numero <= 1) {
                return false; // Números menores ou iguais a 1 não são primos
            }
            for (let i = 2; i < numero; i++) {
                if (numero % i === 0) { 
                    return false; // Se o número for divisível por algum valor além de 1 e ele mesmo, não é primo
                }
            }
            return true; // Se não for divisível por nenhum número além de 1 e ele mesmo, é primo
        }

        // Função principal que chama as outras funções e exibe o resultado
        function calcular() {
            let numero = parseInt(document.getElementById("numero").value); // Obtém o número digitado pelo usuário

            let fatorial = calcularFatorial(numero); // Calcula o fatorial
            let primo = verificarNumeroPrimo(numero); // Verifica se é primo

            // Exibe o resultado na página
            document.getElementById("resultado").innerHTML =
                "O fatorial de " + numero + " é " + fatorial + "<br>" +
                "O número " + numero + (primo ? " é primo." : " não é primo.");
        }
    </script>
</body>

</html>

```
# Respostas

1. Mudanças no código: Ficou mais organizado, legível e fácil de manter com a formatação e os comentários.

2. Importância da rastreabilidade: Facilita a compreensão, correção de erros e colaboração no desenvolvimento.

3. Práticas essenciais para documentação: Comentários explicativos, padronização, documentação externa, versionamento e código modular.

4. Uso do Markdown: Ajuda na formatação e estruturação da documentação, tornando-a mais acessível.

5. Benefícios da padronização: Facilita manutenção e escalabilidade, reduz complexidade e melhora eficiência do código.
