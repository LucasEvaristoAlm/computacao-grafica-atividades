# Entrega - Computação Gráfica

**Disciplina:** Computação Gráfica
**Integrantes:** Gabriel Medeiros de Souza Costa e Lucas Evaristo Almeida de Paula

## 1. Cubo com Satélite Texturizado

**Descrição:** O cubo principal usa `mosaico.png`. O satélite, filho do cubo, usa `grade_uv.png` repetida 2x2, acompanha a rotação do cubo e também gira em torno do próprio eixo X.

**Resposta da questão:** As coordenadas UV relacionam pontos da superfície do objeto a posições da imagem da textura. `repeatUV = [2,2]` repete a textura duas vezes em cada eixo UV, fazendo o padrão aparecer duas vezes em cada face.

**Arquivos:** [atividade_cubo.py](Aula_Texturas/alunos/atividade_cubo.py) e [captura](Aula_Texturas/alunos/capturas/resultado.png).

## 2. Braço Robótico

**Descrição:** O braço usa pivôs organizados em um grafo de cena: ombro, braço, cotovelo, antebraço e garra. A base e as articulações são controladas pelo teclado.

**Resposta da questão:** Os pivôs definem o ponto de rotação de cada articulação. Como as caixas girariam em torno do próprio centro, os objetos `Object3D` permitem posicionar o centro de rotação nas extremidades conectadas. A hierarquia pai-filho também faz as partes seguintes acompanharem o movimento das articulações anteriores.

**Arquivos:** [atividade_braco.py](Aula_GrafoCena/alunos/atividade_braco.py) e [captura](Aula_GrafoCena/alunos/capturas/resultado.png).

## 3. Mini Sistema Solar

**Descrição:** O Sol gira sobre o próprio centro; o planeta orbita o Sol e gira sobre o próprio eixo; a Lua orbita o planeta. As setas controlam a velocidade da órbita do planeta.

**Resposta da questão:** Com vetores-coluna, a matriz mais à direita é aplicada primeiro. Em `R @ T`, `T` posiciona o planeta à distância orbital e `R` gira essa posição em torno do Sol. A rotação própria fica à direita da translação para girar o planeta em torno do centro local antes de posicioná-lo na órbita, sem alterar o raio orbital.

**Arquivos:** [atividade_sistema_solar.py](Aula_Transformacoes/alunos/atividade_sistema_solar.py) e [captura](Aula_Transformacoes/alunos/capturas/resultado.png).
