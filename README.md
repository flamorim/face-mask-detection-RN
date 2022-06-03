<div>
Trabalho de RN - Utilizando Pytorch para classificação de imagens com máscara.

Treinamento feito para 3 novas classes: com máscara, sem máscara e máscara errada

Aluno: Flávio Amorim

Número: 211100510

Turma: 2021.1
</div>
<p>

<div>
Foi utilizado o Pytorch com a ResNet50 pré-treinada e feito o treinamento para as 03 novas classes.

O otimizador foi o SGD com os seguintes parâmetros:
*   lr=0.005
*   momentum=0.9
*   weight_decay=0.0005
</div>
<p>


<div>

O resultado no geral não foi satisfatório e pode-se reparar que em alguns erros o score apresentava um valor próximo a 1. Apenas para a classe "com máscara" o resultado foi bom.

Segue abaixo o detalhamento do resultado de 06 imagens e no final deste notebook essas imagens e predições estão exibidas:

*   Primeira imagem com apenas 01 pessoa:
        predicão "máscara errada" (score 0.0656) x label "sem máscara"     (ERROU)
        
*   Segunda imagem com apenas 01 pessoa:
        predicão "com máscara" x label "com máscara"        (ACERTOU)

*   Terceira imagem com 04 pessoas:
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" (score 0.9134) x label "máscara incorreta"  (ERROU)

*   Quarta imagem com 09 pessoas:
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)
        predicão "com máscara" x label "com máscara"        (ACERTOU)

*   Quinta imagem com 01 pessoa:
        predicão "com máscara" x label "com máscara"        (ACERTOU)

*   Sexta imagem com 03 pessoas:
        predicão "com máscara" (score 0.9975) x label  "sem máscara"        (ERROU)
        predicão "máscara incorreta" (score 0.1862) x label "com máscara"  (ERROU)
        não identificou o rosto x label "sem máscara"       (ERROU)
		
</div>
<p>
<div>
Melhorias a serem implementadas:
1.   Verificar um numero maior de épocas
2. Ajustar os hiperparâmetros do otimizador
3.   Refazer o treinamento, descartando as 39 imagens com mais de 15 pessoas, considerando-as como outliers (tem 02 imagens com mais de 100 pessoas)
4.   Utilizar outra rede pré-treinada
5.   Aplicar data augmentation para aperfeiçoar o treinamento

</div>
