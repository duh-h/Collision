# Collision


o codigo utiliza uma abordagem baseada em impulsos para resolver as colisões entre os corpos.

A fórmula geral do cálculo do impulso em uma colisão é dada por:

J = -(1 + e) * Vr / (1/m1 + 1/m2)

onde:

J é o impulso a ser aplicado durante a colisão.
e é a elasticidade da colisão, um valor entre 0 e 1 que representa a perda de energia na colisão (0 indica uma colisão perfeitamente inelástica, enquanto 1 indica uma colisão perfeitamente elástica).
Vr é a velocidade relativa entre os corpos na direção da normal de colisão(Vr=Vp1.N).
m1 e m2 são as massas dos corpos envolvidos na colisão.







![exemplo_fisica](https://github.com/duh-h/Collision/assets/123125593/f7799f59-cdb8-489e-8cac-14ae5d5a54de)


Resumindo, aqui está uma visão geral dos cálculos envolvidos na colisão entre a bola e o pêndulo:

<H4>1.Definir os parâmetros:</H4>

ma, mb: massas dos corpos A (bola) e B (pêndulo).

rap: vetor de distância do centro de massa do corpo A ao ponto de colisão P.

rbp: vetor de distância do centro de massa do corpo B ao ponto de colisão P.

ωa1, ωb1: velocidades angulares iniciais pré-colisão dos corpos A e B.

ωa2, ωb2: velocidades angulares finais pós-colisão dos corpos A e B.

va1, vb1: velocidades lineares iniciais pré-colisão dos centros de massa A e B.

va2, vb2: velocidades lineares finais pós-colisão dos centros de massa A e B.

vap1: velocidade linear inicial pré-colisão do ponto de impacto P no corpo A.

vbp1: velocidade linear inicial pré-colisão do ponto de impacto P no corpo B.

vp1: velocidade relativa pré-colisão dos pontos de impacto nos corpos A e B.

vp2: velocidade relativa pós-colisão dos pontos de impacto nos corpos A e B.

n: vetor normal (perpendicular) à borda do corpo B.

e: elasticidade da colisão (valor entre 0 e 1).

<H4>2.Calcular as velocidades pré-colisão dos pontos de colisão:</H4>

vap1 = va1 + ωa1 × rap

vbp1 = vb1 + ωb1 × rbp

<H4>3.Calcular as velocidades pós-colisão dos pontos de colisão:</H4>

vap2 = va2 + ωa2 × rap

vbp2 = vb2 + ωb2 × rbp

<H4>4.Calcular as velocidades relativas nos pontos de colisão:</H4>

vp1 = vap1 - vbp1

vp2 = vap2 - vbp2

<H4>5.Calcular a velocidade relativa na direção normal à colisão:</H4>

velocidade normal relativa = vp1 · n

<H4>6.Calcular o impulso de colisão (parâmetro j):</H4>

j = -(1 + e) * (vp1 · n) / (1/ma + 1/mb + (rap × n)² / Ia + (rbp × n)² / Ib)

<H4>7.Calcular as velocidades pós-colisão:</H4>

va2 = va1 + (j * n) / ma

vb2 = vb1 - (j * n) / mb

ωa2 = ωa1 + (rap × (j * n)) / Ia

ωb2 = ωb1 - (rbp × (j * n)) / Ib

Esses cálculos são baseados nas fórmulas e conceitos da física envolvidos em colisões elásticas. O impulso de colisão é utilizado para determinar as mudanças nas velocidades e velocidades angulares dos corpos após a colisão. Vale ressaltar que a implementação exata desses cálculos pode depender do contexto e das especificações detalhadas do sistema físico em questão.











https://github.com/duh-h/Collision/assets/123125593/74691f16-795f-4c1b-b95b-0e0b9d3e8c08

