programa {
  funcao inicio() {
    inteiro opcao=1, nome=1
    caracter nome_jogador_1, nome_jogador_2

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

    
    se (opcao == 1) 
      se (nome == 1) { nome++
        escreva("Digite o nome do jogador 1: ")
        leia(nome_jogador_1)
        escreva("Digite o nome do jogador 2: ")
        leia(nome_jogador_2)
    }
    
     
    
    

    


  }
}
