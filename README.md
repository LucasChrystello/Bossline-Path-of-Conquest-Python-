# Bossline-Path-of-Conquest-Python-

## Descrição do Projeto
BossLine é um jogo de aventura em texto onde os jogadores enfrentam uma série de inimigos em um formato de "Boss Rush". O jogo será executado em um terminal, utilizando arte de caracteres para representar a HUD, os inimigos e os personagens. O objetivo do jogo é derrotar todos os chefes e resolver desafios.

## Estrutura do Projeto
O projeto será dividido em várias bibliotecas que encapsulam funcionalidades específicas do jogo. Abaixo está uma descrição de cada biblioteca e como elas serão referenciadas no módulo principal.

### Estrutura de Bibliotecas

1. **mecanica.py**
   - **Descrição:** Este módulo contém a lógica principal do jogo, incluindo:
     - Sistema de turnos
     - Cálculo de danos
     - Gestão de vida do jogador e dos inimigos
     - Condições de vitória e derrota
     - Funções de aleatoriedade
   - **Referência no módulo principal:**
     ```python
     from mecanica_logistica import iniciar_jogo, verificar_vitoria
     ```

2. **inimigos.py**
   - **Descrição:** Este módulo armazena os dicionários ou objetos que representam os inimigos do jogo, incluindo seus atributos e comportamentos.
   - **Referência no módulo principal:**
     ```python
     from inimigos import inimigos_data, comportamento_inimigo
     ```

3. **itens.py**
   - **Descrição:** Este módulo contém os dicionários ou objetos que representam os itens disponíveis no jogo, como poções e equipamentos.
   - **Referência no módulo principal:**
     ```python
     from itens import itens_disponiveis
     ```

4. **interface.py**
   - **Descrição:** Este módulo é responsável pela arte de interface do usuário (HUD) e pela exibição de informações no terminal.
   - **Referência no módulo principal:**
     ```python
     from interface import exibir_hud, exibir_mensagem
     ```

5. **arte.py**
   - **Descrição:** Este módulo contém as artes de caracteres que representam os personagens e cenários do jogo.
   - **Referência no módulo principal:**
     ```python
     from arte import arte_personagens, arte_inimigos
     ```

### Módulo Principal
O módulo principal do jogo (por exemplo, `main.py`) irá importar todos os módulos mencionados e orquestrar o fluxo do jogo, gerenciando a interação do jogador, o combate e a progressão do jogo.

```python
# main.py
from mecanica_logistica import iniciar_jogo, verificar_vitoria
from inimigos import inimigos_data
from itens import itens_disponiveis
from interface import exibir_hud, exibir_mensagem
from arte import arte_personagens

def main():
    iniciar_jogo()
    # Lógica do jogo

if __name__ == "__main__":
    main()
