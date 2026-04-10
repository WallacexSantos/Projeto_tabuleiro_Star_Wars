# Projeto_tabuleiro_Star_Wars
programa {
  funcao inicio() {
    inteiro opcao
    escreva("𝘽𝙀𝙈 𝙑𝙄𝙉𝘿𝙊 𝘼𝙊 𝙏𝘼𝘽𝙐𝙇𝙀𝙄𝙍𝙊 𝙎𝙏𝘼𝙍 𝙒𝘼𝙍𝙎")
    escreva("\n1. Jogar")
    escreva("\n2. Verificar placar")
    escreva("\n3. Fechar o Jogo ")
    escreva("\n ")
    leia(opcao)
    enquanto(opcao < 1 ou opcao > 3){
      escreva("opção invalida, digite novamente: ")
      leia(opcao)
    }
  }
}
