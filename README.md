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


###













https://github.com/duh-h/Collision/assets/123125593/74691f16-795f-4c1b-b95b-0e0b9d3e8c08

