programa {
  inclua biblioteca Util --> u
  funcao inicio() {
    inteiro opcao=1, nome=1, preparado, dado
    cadeia nome_jogador_1, nome_jogador_2
    

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

    // Problema n1: Tem que ter um sorteio ou (dado) de 2 lados, 1 e 2, se o dado cair 1,
    // O jogador 1 começa, se cair 2, o jogador 2 começa

    // Problema n2: como deverá ser feita as casas? minha sugestão é por números, ex: (caiu na casa 5 de 20)
    // volte 2 casas, então 5 - 2. (3 de 20)

    // Dica: para fazer o dado, já botei lá no topo a biblioteca 'inclua biblioteca Util --> u'
    // para fazer um numero girar aleatoriamente use 'dado = u.sorteia(1, 3)' 

    faca { 
      se (nome==2) {
      escreva(nome_jogador_1, " Aperte 1 quando preparado: ")
      leia(preparado)

      se (preparado==1) {
        escreva("girando dado...")
        dado = u.sorteia(1, 3)
        escreva(dado)

      }
        }
        }
    enquanto (preparado!=1) 
    

    
      
    


    

    
     
    
    

    


  }
}
