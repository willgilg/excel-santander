
# Excel com Inteligencia Aritifical - Entrega de projeto

Repositório para entregar aula 
"Criando uma Ferramenta de Controle de Investimentos com Excel"

[Link para o repo:](https://github.com/willgilg/excel-santander)

- [Documentação Git]

### Formulas do Excel utilizadas na aula
| Formulas  | Explicação |
|-------|---------|
|=VF(C9;C8*12;C7*-1)| VF (Valor Futuro) C9 (Juros) C18 (Anos × 12)  C7 (Valor Mensal)  Vezes -1 (Para Inverter sinal negativo)|
|=PROCV(G3;$A:$D;4;FALSO) | PROCV = G3 = VALOR PROCURADO; $A:$D = COLUNAS DA COLUNA A ATÉ D;  4 = COLUNA 4; FALSO = CORRESPONDENCIA EXATA|

## Calculando valor futuro (Patrimonio acumulado)

![Investimento mensal](assets/images/1.png)
```
=VF(C9;C8*12;C7*-1)
```

## Calculando dividendos mensais 

Dividendos = Patrimonio acumulado * 1% 

![Dividendos Mensais](assets/images/2.png)

```
Dividendos = Patrimonio acumulado * 1% 
```
```
=patrimonio*rendimento_carteira
```


## Dica para utilizar numeros "invisíveis" no Excel 
  *COLOQUE OS NUMEROS NA COLUNA AO LADO 
![Cenários](assets/images/3.png)

PINTE OS DE BRANCO PARA USAR O VALOR NA FORMULA

APERTE F4 DUAS VEZES PARA FICAR A$20 = ISSO FAZ QUE SEJA POSSIVEL COPIAR A FORMULA ARRASTANDO PARA BAIXO DEM ALTERAR OS NUMEROS DAS COLUNAS QUE VOCE VAI DEIXAR "INIVISEVEL"



### SUGESTÃO DE INVESTIMENTO 
  *30% DO SALARIO

### VARIAVEIS GLOBAIS NOMEAÇÃO DE INTERVALOS \ CELULAS

  *Vá no canto superior esquerdo e de um nome a célula 

  *Aperte a tecla F3 para ABRIR OS NOMES DAS VARIAVEI
![Investimento mensal](assets/images/7.png)

## Menu de configurações

![Investimento mensal](assets/images/6.png)



## PERFIS DE INVESTIMENTO 


### PERFIS DE INVESTIMENTO DINAMICO
  *1 - Criar campo de texto validado com 
```
Conservador;Moderado;Agressivo;
```

![Investimento mensal](assets/images/9.png)
  *2 - Criar um tabela de apoio para pegar os com os valores PERCENTUAIS e os tipos de FII's
   
  *3 - O valor da coluna A é o concatenação dos valores da coluna B e C "=B3&"-"&C3" para que fique o texto seja "**TIPO-DE-FI-PERCENTUAL SUGERIDO**"
  *Isso é chamado de chave composta

![Investimento mensal](assets/images/11.png)

  *4 - Criar um PROCV da planilha de apoio no campo de texto "Percentual sugerido"
  Correspondência exata = FALSO
PROCV =  
```
=PROCV(G3;$A:$D;4;FALSO)
```

## Explicação PROCV 
PROCV = G3 = VALOR PROCURADO; $A:$D = COLUNAS DA COLUNA A ATÉ D;  4 = COLUNA 4; FALSO = CORRESPONDENCIA EXATA


  *5 - Criar procv junto a formula de concatenação na columa Percentual Suegerido,
  *Ficando:

```
=PROCV($C$25&"-"&B29;Planilha2!$A:$D;4;FALSO)
```

## Formula da concatanação + PROCV 
![Investimento mensal](assets/images/12.png)