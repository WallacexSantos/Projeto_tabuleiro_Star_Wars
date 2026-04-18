programa {
  inclua biblioteca Util --> u
  funcao inicio() {
    inteiro opcao=1, nome=0, rolardado, dado, casa_jogador_1=0, casa_jogador_2=0, pontuacao_jogador_1 = 0, pontuacao_jogador_2 = 0
    cadeia nome_jogador_1 = "jedi" , nome_jogador_2 = "sith"
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
     	escreva("Que a Força esteja com você")
        } senao se(casa_jogador_1 == 2){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Obi-Wan Kenobi: \nA Força estará com você. Sempre!!")
            //deve avançar o jogador para a casa 5
          }
          senao se(casa_jogador_1 == 3){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Anakin Skywalker:\nÉ aqui que a diversão começa")
            //deve jogar um dado adicional de 3 lados
          }
          senao se(casa_jogador_1 == 4){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Yoda:\nMuito a aprender você ainda tem.")
          }
          senao se(casa_jogador_1 == 5){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Qui-Gon Jinn:\nSeu foco determina sua realidade.")
          }
          senao se(casa_jogador_1 == 6){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Obi-Wan Kenobi:\nA Força é o que dá poder a um Jedi.")
          }
          senao se(casa_jogador_1 == 7){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Obi-Wan Kenobi:\nSenti uma grande perturbação na Força…")
            //deve impedir que o jogador jogue o dado por 1 rodada
          }
          senao se(casa_jogador_1 == 8){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Qui-Gon Jinn:\nSinta, não pense… use seus instintos.")
          senao se(casa_jogador_1 == 9){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Yoda:\nFaça. Ou não faça. Não existe tentativa.")
          }
          senao se(casa_jogador_1 == 10){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Obi-Wan Kenobi:\nEra dito que você destruiria os Sith…")
            //deve trocar as casa em que os jogadores estão
          }
          senao se(casa_jogador_1 == 11){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Yoda:\nSempre há mais a aprender.")
          }
          senao se(casa_jogador_1 == 12){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Luke Skywalker:\nTenho um mau pressentimento sobre isso.")
             //deve retroceder 1 casa
          }
          senao se(casa_jogador_1 == 13){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Luke Skywalker:\nEu não tenho medo")
          }
          senao se(casa_jogador_1 == 14){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Han Solo:\nEu resolvo isso.")
          }
          senao se(casa_jogador_1 == 15){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            
            //deve cantar um trecho de uma música (na vida real) ou voltar 2 casa
          }
          senao se(casa_jogador_1 == 16){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Yoda:\nA Força é poderosa.")
          }
          senao se(casa_jogador_1 == 17){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Padmé Amidala:\nPrecisamos agir com cautela.")
          }
          senao se(casa_jogador_1 == 18){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Mace Windu:\nVocê está neste Conselho, mas não lhe concedemos o posto de Mestre.")
          }
          senao se(casa_jogador_1 == 19){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Admiral Ackbar:\nÉ uma armadilha")
            //deve voltar para a casa 1
          }
          senao se(casa_jogador_1 == 20){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_1 == 21){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_1 == 22){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_1 == 23){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_1 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_1 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("Yoda:\nUm Jedi você se tornou.")
            pontuacao_jogador_1 ++
        		escreva ("\nvitoria ",nome_jogador_1)
          }
          se (casa_jogador_1 <25)
          {
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
          escreva("Darth Maul: \nFinalmente vamos nos revelar aos Jedi. Finalmente teremos vingança.")
        } senao se(casa_jogador_2 == 2){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nPoder! Poder ilimitado!")
            //deve avançar o jogador para a casa 5
          }
          senao se(casa_jogador_2 == 3){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("General Grievous:\nIsso fará uma bela adição à minha coleção.")
            //deve jogar um dado adicional de 3 lados
          }
          senao se(casa_jogador_2 == 4){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nO lado sombrio da Força é um caminho para muitas habilidades que alguns consideram… não naturais.")
          }
          senao se(casa_jogador_2 == 5){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Darth Vader:\nO poder do lado sombrio é mais forte do que você imagina.")
          }
          senao se(casa_jogador_2 == 6){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nSeu ódio o tornou poderoso.")
          }
          senao se(casa_jogador_2 == 7){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Darth Vader:\nSua falta de fé é perturbadora.")
            //deve impedir que o jogador jogue o dado por 1 rodada
          }
          senao se(casa_jogador_2 == 8){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nUse sua raiva… ela te dá poder.")
          }
          senao se(casa_jogador_2 == 9){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Darth Vader:\nNão há escapatória.")
          }
          senao se(casa_jogador_2 == 10){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Darth Vader:\nJunte-se a mim, e juntos dominaremos a galáxia como pai e filho.")
            //deve trocar as casa em que os jogadores estão
          }
          senao se(casa_jogador_2 == 11){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Count Dooku:\nO lado sombrio revela a verdade.")
          }
          senao se(casa_jogador_2 == 12){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Darth Vader:\nSinto algo… uma presença que não sentia desde…")
            //deve retroceder 1 casa
          }
          senao se(casa_jogador_2 == 13){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Darth Vader:\nVocê terá medo")
          }
          senao se(casa_jogador_2 == 14){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Darth Vader:\nIsso está sob controle.")
          }
          senao se(casa_jogador_2 == 15){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            
            //deve cantar um trecho de uma música (na vida real) ou voltar 2 casa
          }
          senao se(casa_jogador_2 == 16){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nO lado sombrio é mais forte.")
          }
          senao se(casa_jogador_2 == 17){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Grand Moff Tarkin:\nO medo manterá os sistemas na linha.")
          }
          senao se(casa_jogador_2 == 18){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nEu sou o Senado.")
          }
          senao se(casa_jogador_2 == 19){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nSua ira o traiu.")
            //deve voltar para a casa 1
          }
          senao se(casa_jogador_2 == 20){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_2 == 21){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_2 == 22){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_2 == 23){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_2 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
          }
          senao se(casa_jogador_2 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("Palpatine:\nSua jornada para o lado sombrio está completa.")
        		pontuacao_jogador_2 ++
        		escreva ("\nvitoria ",nome_jogador_2)
                   	}
          }
      }
    }
  }
}
