# Projeto_tabuleiro_Star_Wars
programa {
  funcao inicio() {
    inteiro opcao=1
    faca{
    escreva("BEM VINDO AO TABULEIRO STAR WARS")
    escreva("\n1. Jogar")
    escreva("\n2. Verificar placar")
    escreva("\n3. Fechar o Jogo ")
    escreva("\n ")
    leia(opcao)
     se (opcao  < 1 ou opcao > 3){ 
     escreva("opção invalida, digite novamente: ")
     }
    }
    enquanto(opcao  < 1 ou opcao > 3)
  }
}
