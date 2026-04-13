programa {
  inclua biblioteca Util --> u
  funcao inicio() {
    inteiro opcao=1, nome=0, rolardado, dado, casa_jogador_1=0, casa_jogador_2=0
    cadeia nome_jogador_1 = "jedi' , nome_jogador_2 = "sith"
    faca{
      escreva("BEM VINDO AO TABULEIRO STAR WARS")
      escreva("\n1. TECLE 1 PARA Jogar")
      escreva("\n2. Verificar placar")
      escreva("\n3. Fechar o Jogo ")
      escreva("\n ")
      leia(opcao)
      se (opcao  < 1 ou opcao > 3){ 
        escreva("opção invalida, digite novamente: ")
      }
    }
    enquanto(opcao  < 1 ou opcao > 3)

    se (opcao == 1) 
      se (nome == 0) { nome++
        escreva("Digite o nome do jogador 1: ")
        leia(nome_jogador_1)
        escreva("Digite o nome do jogador 2: ")
        leia(nome_jogador_2)
    }
    se (opcao == 1) {
      enquanto(casa_jogador_1 <25 e casa_jogador_2 <25){
        faca{
          escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
          leia(rolardado)
          se(rolardado != 1){
            escreva("opcao incorreta, aperte 1 para rolar dado")
          }
        }
        enquanto(rolardado != 1)
        dado = u.sorteia(1, 6)
        escreva("\nrolando dado...")
        escreva(dado, "\n")
        casa_jogador_1 = casa_jogador_1 + dado
        se(casa_jogador_1 == 1) {
          escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
        } senao se(casa_jogador_1 == 2){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 3){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 4){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 5){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 6){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 7){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 8){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 9){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 10){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 11){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 12){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 13){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 14){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 15){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 16){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 17){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 18){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 19){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 20){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 21){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 22){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 23){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
          senao se(casa_jogador_1 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
          }
        
        faca{
          escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar o dado: ")
          leia(rolardado)
          se(rolardado != 1){
            escreva("opcao incorreta, aperte 1 para rolar dado")
          }
        }
        enquanto(rolardado != 1)
        dado = u.sorteia(1, 6)
        escreva("\nrolando dado...")
        escreva(dado, "\n")
        casa_jogador_2 = casa_jogador_2 + dado
        se(casa_jogador_2 == 1) {
          escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
        } senao se(casa_jogador_2 == 2){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 3){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 4){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 5){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 6){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 7){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 8){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 9){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 10){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 11){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 12){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 13){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 14){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 15){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 16){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 17){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 18){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 19){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 20){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 21){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 22){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 23){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
          senao se(casa_jogador_2 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          }
      }
    }
  }
}
