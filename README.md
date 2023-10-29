# Teste de PSI 1 - Turno 2 - Versão 1

## Informação do aluno

    Nome: ...

Teste termina às 13:25.

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Indica o que é impresso pelo seguinte código. Justifica a tua resposta

    bool x = true && false;
    x |= 2 < 5;
    
    Console.WriteLine(x);

P1 - Resposta

    É impresso: True

    Para definir o valor da variável 'x', aplicamos o operador condicional '&&'
    entre os valores 'true' e 'false'.
    Para que esta condição retorne 'true', é preciso que ambos os valores sejam 'true'.
    Como esse não é o caso, a variável 'x' fica inicialmente com o valor 'false'.
    Na segunda linha, usamos o operador condicional '||' entre os valores 'x' e '2 < 5'.
    Para que esta condição retorne 'true', é preciso que pelo menos um dos valores seja 'true'.
    Como '2 < 5' é uma declaração verdadeira, o valor de 'x' passa a ser 'true'.
    O método Console.WriteLine é responsável por imprimir um tipo de valor. 
    Este valor é passado entre parênteses depois do nome do método.
    Assim sendo, o valor entre parênteses 'x' corresponde ao valor da variável de mesmo nome.

### P2. Considera o seguinte código com um *bug*

    short s = long.MaxValue;

    Console.WriteLine(s);

### Indica uma possível correção para que o código não apresente erros. Explica porque foi necessário fazer essa correção

P2 - Resposta

    Uma possível correção: short s = short.MaxValue;

    A propriedade 'MaxValue' corresponde ao valor máximo de um determinado tipo.
    Neste caso, estamos a tentar guardar o valor máximo de 'long' numa variável 'short'.
    Visto que 'short' tem um alcançe inferior a 'long', é impossível a variável 's' guardar o valor pedido.
    Assim sendo, podemos alterar o tipo a que a propriedade 'MaxValue' acede para 'short'.

### P3. Escreve um programa que solicite ao utilizador dois números reais e apresente o resultado do primeiro (base) elevado ao segundo (expoente). Não podes usar um método da classe Math para obter o resultado

P3 - Resposta

    // Variáveis para guardar números reais e resultado da operação
    float b, e, resultado = 1.0f;

    // Pedir o primeiro número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o primeiro número real: ");
    b = Convert.ToSingle(Console.ReadLine());

    // Pedir o segundo número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o segundo número real: ");
    e = Convert.ToSingle(Console.ReadLine());

    // Ciclo FOR para calcular número base elevado ao número expoente
    for (int i = 0; i < e; i++)
    {
      // Multiplicar número base 'e' vezes e guardar resultado na variável correspondente
      resultado *= b;
    }

    // Imprimir resultado da soma
    Console.WriteLine($"{b} elevado a {e} = {resultado}");

### P4. Estás na pasta raiz do teu repositório local, onde atualizaste um ficheiro de nome 'Classes.cs'. Queres enviar **apenas** esta atualização para o teu repositório remoto. Indica os comandos necessários. A mensagem de commit deve ser apropriada

P4 - Resposta

    1. Adicionar ficheiro 'Classes.cs' para commit
        git add Classes.cs

    2. Fazer commit com mensagem apropriada
        git commit -m "Atualizar ficheiro Classes.cs"

    3. Enviar atualização para o repositório remoto
        git push
