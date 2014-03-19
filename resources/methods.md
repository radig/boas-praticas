# Métodos
<em>Esta página é apenas um esboço e pode ser melhorada</em>
## 1. Obrigatório

Seguir os padrões PSR-2, item 4.3 para escrita de métodos.

## 2. Nomes de métodos
### 2.1 Introdução
É interessante manter um padrão de nomes em diferentes projetos, a fim de que seja mais previsível para quem tenha acesso ao código.
Porém não podem haver redundâncias ou replicações de códigos caso tais métodos façam parte de um mesmo pacote. Dessa forma, utilizar um
mesmo padrão de nomes também ajuda a identificar esses casos.

De preferência não abreviar nomes de métodos de forma a evitar ambiguidades ou somente abreviar caso uma palavra seja extensa e sua abreviação 
tenha significado claro para todos que a lêem, sem a necessidade de consultar a documentação. Claro, a utilização de um PHPDoc detalhado é 
altamente recomendada. 

### 2.2 Getters and Setters
Métodos cujo objetivo é retornar informações de um conjunto de dados ou o resultado de alguma operação aritmética, lógica, algoritmica, etc 
podem seguir o padrão 'get[aquiloQueSeObtem]'. O mesmo vale para 'setters' (métodos que alteram o valor de alguma propriedade, da classe 
ou de um conjunto de dados): 'set[aquiloQueSeAltera]'. 

Exemplos:
    
    /**
     * Obtém a temperatura da CPU
     */
    public function getCpuTemperature() {

    }

    /**
    * Obtém estatísticas da CPU
    */
    public function getCpuStats() {

    }

### 2.3 Ações de Controller
Quando um método tem o papel de uma action de controller da estrutura MVC, evitar que seu nome fique extenso e desencoraje seu acesso direto
pela URL. Salvo em casos em que tais ações representem uma api REST com extensa lista de funções complexas em que tais métodos podem ter 
um nome descritivo e fácil de memorizar.

De preferência, um método de uma classe controller deve manter a lógica necessária apenas para tratamento da requisição/resposta, delegando regras
de negócio e manipulação de dados para o model ou classes equivalentes.
