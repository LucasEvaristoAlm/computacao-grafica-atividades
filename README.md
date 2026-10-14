# Atividades de Computação Gráfica

**Disciplina:** Computação Gráfica

**Integrantes:** Gabriel Medeiros de Souza Costa e Lucas Evaristo Almeida de Paula

Este repositório reúne as atividades que fizemos nas aulas. Em cada seção estão o código e a captura do resultado.

## 1. Cubo com Satélite Texturizado

Fizemos o cubo principal com `mosaico.png` e colocamos o satélite como filho dele. O satélite usa `grade_uv.png` repetida 2x2, acompanha o movimento do cubo e também gira no próprio eixo X.

**Resposta da questão:** As coordenadas UV indicam qual parte da imagem vai em cada ponto da superfície do cubo. Com `repeatUV = [2,2]`, a imagem se repete duas vezes em cada direção, então o padrão aparece repetido nas faces.

**Arquivos:** [código](Aula_Texturas/alunos/atividade_cubo.py) e [captura](Aula_Texturas/alunos/capturas/resultado.png).

## 2. Braço Robótico

Montamos o braço com pivôs no ombro e no cotovelo. Assim, as partes conectadas acompanham as rotações: A/D giram a base, W/S movem o ombro e I/K movem o cotovelo.

**Resposta da questão:** Usamos pivôs porque uma caixa girada diretamente roda em torno do próprio centro. Com um `Object3D` na articulação, o braço e o antebraço giram pela extremidade onde estão conectados. A hierarquia também faz cada parte acompanhar o movimento do seu pai.

**Arquivos:** [código](Aula_GrafoCena/alunos/atividade_braco.py) e [captura](Aula_GrafoCena/alunos/capturas/resultado.png).

## 3. Mini Sistema Solar

Fizemos o planeta orbitar o Sol a uma distância de `0.6` e a Lua orbitar o planeta a `0.2`. O Sol e o planeta também giram sobre os próprios eixos, e as setas ajustam a velocidade da órbita do planeta.

**Resposta da questão:** Em `R @ T`, a matriz mais à direita é aplicada primeiro: `T` coloca o planeta à distância certa e `R` faz essa posição girar ao redor do Sol. A rotação própria fica à direita da translação para girar o planeta em torno do seu centro antes de colocá-lo na órbita. Assim, ele não gira em torno do Sol por causa da rotação do próprio eixo.

**Arquivos:** [código](Aula_Transformacoes/alunos/atividade_sistema_solar.py) e [captura](Aula_Transformacoes/alunos/capturas/resultado.png).
