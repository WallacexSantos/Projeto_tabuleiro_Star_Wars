programa {
  inclua biblioteca Util --> u
  funcao inicio() {
    inteiro opcao=1, nome=0, rolardado, dado, casa_jogador_1=0, casa_jogador_2=0
    inteiro pontuacao_jogador_1 = 0, pontuacao_jogador_2 = 0, opcao_casa_15 = 0, dado_jogador_1_casa_22, dado_jogador_2_casa_22
    inteiro soma ,dado_2 = 0 ,rolardado_casa23, casa_vazia = 0, rodada_jogador_1_livre = 0, rodada_jogador_2_livre = 0, dado_4_lados_j1=0, dado_4_lados_j2=0
    cadeia nome_jogador_1 = "jedi" , nome_jogador_2 = "sith"
    u.aguarde(1000)
    escreva("\n░██████╗████████╗░█████╗░██████╗░  ░██╗░░░░░░░██╗░█████╗░██████╗░░██████╗")
    u.aguarde(1000)
    escreva("\n██╔════╝╚══██╔══╝██╔══██╗██╔══██╗  ░██║░░██╗░░██║██╔══██╗██╔══██╗██╔════╝")
    u.aguarde(1000)
    escreva("\n╚█████╗░░░░██║░░░███████║██████╔╝  ░╚██╗████╗██╔╝███████║██████╔╝╚█████╗░")
    u.aguarde(1000)
    escreva("\n░╚═══██╗░░░██║░░░██╔══██║██╔══██╗  ░░████╔═████║░██╔══██║██╔══██╗░╚═══██╗")
    u.aguarde(1000)
    escreva("\n██████╔╝░░░██║░░░██║░░██║██║░░██║  ░░╚██╔╝░╚██╔╝░██║░░██║██║░░██║██████╔╝")
    u.aguarde(1000)
    escreva("\n╚═════╝░░░░╚═╝░░░╚═╝░░╚═╝╚═╝░░╚═╝  ░░░╚═╝░░░╚═╝░░╚═╝░░╚═╝╚═╝░░╚═╝╚═════╝░")
    u.aguarde(2000)
    limpa()
    faca{
      escreva("=====================================\n")
      escreva("_________TABULEIRO STAR WARS_________\n")
      escreva("=====================================\n")
      escreva(" Digite [1] Jogar\n")
      escreva(" DIgite [2] Verificar Placar\n")
      escreva(" Digite [3] Sair do Jogo\n")
      escreva("=====================================\n")
      leia(opcao)
      se (opcao  < 1 ou opcao > 3){ 
        escreva("opção invalida, digite novamente: ")
      }
    }
    enquanto(opcao  < 1 ou opcao > 3)
    limpa()
    //AQUI TALVEZ TENHA UM ERRO NA CONTAGEM PARA SEGUNDA VEZ QUANDO O NOME ESTIVER 1, TALVEZ NAO ENTRE AQUI
    se (opcao == 1){ 
      se (nome == 0) { nome++
        escreva("Digite o nome do jogador 1: ")
        leia(nome_jogador_1)
        escreva("Digite o nome do jogador 2: ")
        leia(nome_jogador_2)
      }
    }
    se (opcao == 1) {
      enquanto(casa_jogador_1 <25 e casa_jogador_2 <25){
        se ( rodada_jogador_1_livre == 0 ) {
          faca{
            escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
            leia(rolardado)
            se(rolardado != 1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
            }
          }
          enquanto(rolardado != 1)
          se(dado_4_lados_j1==1){
        	  dado_4_lados_j1 = dado_4_lados_j1-1 
        	  dado = u.sorteia(1, 4)
        	  escreva("rolando dado...")
        	  escreva(dado, "\n")
       	    casa_jogador_1 = casa_jogador_1 + dado
          }
          senao{
        	  dado = u.sorteia(1, 6)
        	  escreva("rolando dado...")
        	  escreva(dado, "\n")
        	  casa_jogador_1 = casa_jogador_1 + dado
          }
          se(casa_jogador_1 == 1) {
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
     	      escreva("\nQue a Força esteja com você")
          } 
          senao se(casa_jogador_1 == 2){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nObi-Wan Kenobi: \nA Força estará com você. Sempre!!")
            escreva("\n",nome_jogador_1, " avancou até a casa 5")
            casa_jogador_1 = casa_jogador_1 + 3
            escreva("\nQui-Gon Jinn:\nSeu foco determina sua realidade.")
            //deve avançar o jogador para a casa 5 feito!!!
          }
          senao se(casa_jogador_1 == 3){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nAnakin Skywalker:\nÉ aqui que a diversão começa")
            escreva("\n",nome_jogador_1, " jogue um dado adicional de 3 lados: ")
            //deve jogar um dado adicional de 3 lados
            escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
            leia(rolardado)
            enquanto(rolardado != 1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado)
          	}    
            dado = u.sorteia(1, 3)
            escreva("\nrolando dado...")
            escreva("\n" , dado)
            casa_jogador_1 = casa_jogador_1 + dado
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\n...")
          }
          senao se(casa_jogador_1 == 4){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nYoda:\nMuito a aprender você ainda tem.")
          }
          senao se(casa_jogador_1 == 5){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nQui-Gon Jinn:\nSeu foco determina sua realidade.")
          }
          senao se(casa_jogador_1 == 6){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nObi-Wan Kenobi:\nA Força é o que dá poder a um Jedi.")
          }
          senao se(casa_jogador_1 == 7){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nObi-Wan Kenobi:\nSenti uma grande perturbação na Força…")
            escreva("\n",nome_jogador_1, " fique sem jogar por 1 rodada.")
            //deve impedir que o jogador jogue o dado por 1 rodada feito!!!
            rodada_jogador_1_livre = rodada_jogador_1_livre +2
          }
          senao se(casa_jogador_1 == 8){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nQui-Gon Jinn:\nSinta, não pense… use seus instintos.")
          }
          senao se(casa_jogador_1 == 9){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nYoda:\nFaça. Ou não faça. Não existe tentativa.")
          }
          senao se(casa_jogador_1 == 10){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nObi-Wan Kenobi:\nEra dito que você destruiria os Sith…")
            escreva("\n",nome_jogador_1, " trocou de casa com ",nome_jogador_2)
            escreva("\nObi-Wan Kenobi:\nVocê era o escolhido!.")
            casa_vazia = casa_jogador_1
            casa_jogador_1 = casa_jogador_2
            casa_jogador_2 = casa_vazia
          }
          senao se(casa_jogador_1 == 11){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nYoda:\nSempre há mais a aprender.")
          }
          senao se(casa_jogador_1 == 12){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nLuke Skywalker:\nTenho um mau pressentimento sobre isso.")
            escreva("\n",nome_jogador_1, " retornou 1 casa.")
            casa_jogador_1 = casa_jogador_1 - 1
            escreva("\n",nome_jogador_1, " está casa ", casa_jogador_1)
            escreva("\nYoda:\nSempre há mais a aprender.")
            //deve retroceder 1 casa feito!!!!
          }
          senao se(casa_jogador_1 == 13){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nLuke Skywalker:\nEu não tenho medo")
          }
          senao se(casa_jogador_1 == 14){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nHan Solo:\nEu resolvo isso.")
          }
          senao se(casa_jogador_1 == 15){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nRecite uma frase de star wars na vida real ou volte 2 casas")
            escreva("\n1. Recitar frase ")
            escreva("\n2. Voltar 2 casas ")
            leia(opcao_casa_15)
            enquanto(opcao_casa_15 < 1 ou opcao_casa_15 > 2){
              escreva("\nopcao incorreta, digite 1. Recitar frase ou digite 2 para Voltar 2 casas ")
            	leia (opcao_casa_15)
            }
            se(opcao_casa_15 == 1){
            	escreva("\nRecite a frase: Que a força esteja com você.")
            }
            se(opcao_casa_15 == 2){
            	casa_jogador_1 = casa_jogador_1 - 2
            	escreva(nome_jogador_1, " voltou para casa ", casa_jogador_1)
            }
            //deve cantar um trecho de uma música (na vida real) ou voltar 2 casa FALTA A MUSICA
          }
          senao se(casa_jogador_1 == 16){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nYoda:\nA Força é poderosa.")
          }
          senao se(casa_jogador_1 == 17){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nPadmé Amidala:\nPrecisamos agir com cautela.")
          }
          senao se(casa_jogador_1 == 18){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nMace Windu:\nVocê está neste Conselho, mas não lhe concedemos o posto de Mestre.")
          }
          senao se(casa_jogador_1 == 19){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nAdmiral Ackbar:\nÉ uma armadilha")
            escreva("\n",nome_jogador_1, " voltou para a casa 1.")
            casa_jogador_1 = 1
            escreva("\nQue a força esteja com você.")
            //deve voltar para a casa 1 feito!!!
          }
          senao se(casa_jogador_1 == 20){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nYoda:\nDifícil de ver, o futuro é.")
            escreva("\nvoce deve jogar um dado adicional, se cair um numero par voce deve manter na casa, se cair um numero impar deve retroceder 3 casas " )
            faca{
              escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
              leia(rolardado)
                se(rolardado != 1){
                  escreva("opcao incorreta, aperte 1 para rolar dado")
                  leia(rolardado)
                }
            }
            enquanto(rolardado != 1)
            dado = u.sorteia(1, 6)
            escreva("\nrolando dado...")
            escreva(dado, "\n")
            se( dado==2 ou dado==4 ou dado==6 ) {
              escreva("parabens, voce se manteve na casa " , casa_jogador_1)
            } 
            senao {
              casa_jogador_1 = casa_jogador_1-3 
              escreva("voce voltou para a casa " , casa_jogador_1)
              //o grupo deve escolher e implementar funcionalidades propostas pela própria equipe
            }
          }
          senao se(casa_jogador_1 == 21){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nObi-Wan kenobi:\nSe você me derrubar, me tornarei mais poderoso do que pode imaginar.")
            escreva("\nNa próxima rodada você ira girar um dado de 4 lados")
            dado_4_lados_j1++
            //Você jogara um dado d4 na próxima rodada
          }
          senao se(casa_jogador_1 == 22){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nLuke skywalker:\nNão lutarei com você, pai.")
            escreva("Dois jogadores deverao jogar um dado, quem tirar o menor numero devera voltar 4 casas ")
            escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
            leia(rolardado)
            enquanto(rolardado != 1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado)
            }
            dado_jogador_1_casa_22 = u.sorteia(1, 6)
            escreva("\nrolando dado...")
            escreva(dado_jogador_1_casa_22, "\n")
            escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar o dado: ")
            leia(rolardado)
            enquanto(rolardado != 1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado)
            }
            dado_jogador_2_casa_22 = u.sorteia(1, 6)
            escreva("\nrolando dado...")
            escreva(dado_jogador_2_casa_22, "\n")
            se (dado_jogador_2_casa_22 > dado_jogador_1_casa_22){
              casa_jogador_1 = casa_jogador_1-4
              escreva (nome_jogador_2 ," venceu o duelo")
              escreva ("\n", nome_jogador_1 ," voltou 4 casas e esta na casa ",casa_jogador_1)
            }
            senao se (dado_jogador_2_casa_22 < dado_jogador_1_casa_22){
              casa_jogador_1 = casa_jogador_1-4
              escreva (nome_jogador_1 ," venceu o duelo")
              escreva ("\n", nome_jogador_2 ," voltou 4 casas e esta na casa ",casa_jogador_1)
            }
            senao{
          	  escreva ("Empate, os dois se mantiveram na mesma casa")
            }
          }
          senao se(casa_jogador_1 == 23){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nLeia Organa:\nQuanto mais você aperta o controle, mais sistemas vão escapar..")
            escreva ("\nNessa casa você deverá jogar dois dados, a soma dos dados serão as casas que você deve retroceder")
            escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar os dados: ")
        		leia(rolardado_casa23)
            enquanto(rolardado_casa23!=1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado_casa23)
            }
            dado = u.sorteia(1,6)
            dado_2 = u.sorteia(1, 6)
            soma = dado + dado_2
            casa_jogador_1 = casa_jogador_1 - soma
      		  escreva("\nrolando dado...")
       			escreva(dado)
     		   	escreva("\nrolando dado...")
     			  escreva(dado_2)
     			  escreva("\n", nome_jogador_1  ," devera retroceder ", soma," casas")    
        	}
          //Você deve jogar dois dados, o tanto que sair, você deverá retroceder as casas
          senao se(casa_jogador_1 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nLuke Skywalker:\nEu sou um Jedi, como meu pai antes de mim.")
            escreva("Para avançar, gire um dado, caso tire par podera prosseguir")
            faca{
          	  escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
          	  leia(rolardado)
          	  se(rolardado != 1){
            		escreva("opcao incorreta, aperte 1 para rolar dado")
                leia(rolardado)
          	  }
       	    } 
            enquanto(rolardado != 1)
			      escreva("\nrolando dado...")
            dado_2=u.sorteia(1, 6)
        		escreva(dado_2, "\n")
            se(dado_2==1 ou dado_2==3 ou dado_2==5){
            	escreva("Você não podera avançar")
            	rodada_jogador_1_livre = rodada_jogador_1_livre + 1
            }
            senao se(dado_2==2 ou dado_2==4 ou dado_2==6){
              casa_jogador_1 = casa_jogador_1 + dado_2
            }
          //Só avança se tirar um número par
          }
          senao se(casa_jogador_1 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa 25")
            escreva("\nYoda:\nUm Jedi você se tornou.")
            pontuacao_jogador_1 ++
        		escreva ("\nvitoria ",nome_jogador_1)
          }
          se (rodada_jogador_2_livre !=0){
          	rodada_jogador_2_livre--
          }
        }
        se (casa_jogador_1 <25){
          se (rodada_jogador_2_livre == 0 ) {
            faca{
              escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar o dado: ")
              leia(rolardado)
              se(rolardado != 1){
                escreva("opcao incorreta, aperte 1 para rolar dado")
              }
            }
            enquanto(rolardado != 1)
            se(dado_4_lados_j2 == 1){
        	    dado_4_lados_j2 = dado_4_lados_j2-1 
        	    dado = u.sorteia(1, 4)
        	    escreva("rolando dado...")
        	    escreva(dado, "\n")
        	    casa_jogador_2 = casa_jogador_2 + dado
            }
            senao{
              dado = u.sorteia(1, 6)
              escreva("\nrolando dado...")
              escreva(dado, "\n")
              casa_jogador_2 = casa_jogador_2 + dado
            }
          se(casa_jogador_2 == 1) {
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Maul: \nFinalmente vamos nos revelar aos Jedi. Finalmente teremos vingança.")
          } 
          senao se(casa_jogador_2 == 2){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine:\nPoder! Poder ilimitado!")
            escreva("\n",nome_jogador_2, " avancou até a casa 5")
            casa_jogador_2 = casa_jogador_2 + 3
            //deve avançar o jogador para a casa 5 feito!!!
            escreva("\nDarth Vader:\nO poder do lado sombrio é mais forte do que você imagina.")
          }
          senao se(casa_jogador_2 == 3){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nGeneral Grievous:\nIsso fará uma bela adição à minha coleção.")
            escreva("\n",nome_jogador_2, " jogue um dado adicional de 3 lados: ")
            //deve jogar um dado adicional de 3 lados
            escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar o dado: ")
            leia(rolardado)
            enquanto(rolardado != 1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado)
          	}    
            dado = u.sorteia(1, 3)
            escreva("\nrolando dado...")
            escreva("\n" , dado)
            casa_jogador_2 = casa_jogador_2 + dado
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\n...")
          }
          senao se(casa_jogador_2 == 4){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine:\nO lado sombrio da Força é um caminho para muitas habilidades que alguns consideram… não naturais.")
          }
          senao se(casa_jogador_2 == 5){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader:\nO poder do lado sombrio é mais forte do que você imagina.")
          }
          senao se(casa_jogador_2 == 6){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine:\nSeu ódio o tornou poderoso.")
          }
          senao se(casa_jogador_2 == 7){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader:\nSua falta de fé é perturbadora.")
            escreva("\n",nome_jogador_2, " fique sem jogar por 1 rodada.")
            //deve impedir que o jogador jogue o dado por 1 rodada feito!!!
            rodada_jogador_2_livre = rodada_jogador_2_livre+2
          }
          senao se(casa_jogador_2 == 8){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine:\nUse sua raiva… ela te dá poder.")
          }
          senao se(casa_jogador_2 == 9){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader:\nNão há escapatória.")
          }
          senao se(casa_jogador_2 == 10){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader:\nJunte-se a mim, e juntos dominaremos a galáxia como pai e filho.")
            escreva("\n",nome_jogador_2, " trocou de casa com ",nome_jogador_1)
            escreva("\nDarth Vader:\nEu vejo através das mentiras dos Jedi.")
            casa_vazia = casa_jogador_1
            casa_jogador_1 = casa_jogador_2
            casa_jogador_2 = casa_vazia
          }
          senao se(casa_jogador_2 == 11){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nCount Dooku:\nO lado sombrio revela a verdade.")
          }
          senao se(casa_jogador_2 == 12){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader:\nSinto algo… uma presença que não sentia desde…")
            escreva("\n",nome_jogador_2, " retornou 1 casa.")
            casa_jogador_2 = casa_jogador_2 - 1
            escreva("\n",nome_jogador_2, " está casa ", casa_jogador_2)
            escreva("\nCount Dooku:\nO lado sombrio revela a verdade.")
            //deve retroceder 1 casa feito!!!
          }
          senao se(casa_jogador_2 == 13){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader:\nVocê terá medo")
          }
          senao se(casa_jogador_2 == 14){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader:\nIsso está sob controle.")
          }
          senao se(casa_jogador_2 == 15){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nRecite uma frase de star wars na vida real ou volte 2 casas")
            escreva("\n1. Recitar frase ")
            escreva("\n2. Voltar 2 casas ")
            leia(opcao_casa_15)
            enquanto(opcao_casa_15 < 1 ou opcao_casa_15 > 2){
              escreva("\nopcao incorreta, digite 1. Recitar frase ou digite 2 para Voltar 2 casas ")
            	leia (opcao_casa_15)
            }
            se(opcao_casa_15 == 1){
            	escreva("\nRecite a frase: Não, eu sou seu pai")
            }
            se(opcao_casa_15 == 2){
            	casa_jogador_2 = casa_jogador_2 - 2
            	escreva(nome_jogador_2, " voltou para casa ", casa_jogador_2)
            }
            //deve cantar um trecho de uma música (na vida real) ou voltar 2 casa FALTA A MUSICA
          }
          senao se(casa_jogador_2 == 16){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine:\nO lado sombrio é mais forte.")
          }
          senao se(casa_jogador_2 == 17){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nGrand Moff Tarkin:\nO medo manterá os sistemas na linha.")
          }
          senao se(casa_jogador_2 == 18){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine:\nEu sou o Senado.")
          }
          senao se(casa_jogador_2 == 19){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine:\nSua ira o traiu.")
            escreva("\n",nome_jogador_2, " voltou para a casa 1.")
            casa_jogador_2 = 1
            escreva("\nDarth Maul: \nFinalmente vamos nos revelar aos Jedi. Finalmente teremos vingança.")
            //deve voltar para a casa 1 feito!!!
          }
          senao se(casa_jogador_2 == 20){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nPalpatine: \nTudo está acontecendo como eu previ,")
            escreva("\nvoce deve jogar um dado adicional, se cair um numero par voce deve manter na casa, se cair um numero impar deve retroceder 3 casas " )
            faca{
              escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar o dado: ")
              leia(rolardado)
              se(rolardado != 1){
                escreva("opcao incorreta, aperte 1 para rolar dado")
                leia(rolardado)
              }
            }
            enquanto(rolardado != 1)
            dado = u.sorteia(1, 6)
            escreva("\nrolando dado...")
            escreva(dado, "\n")
            se( dado==1 ou dado==3 ou dado==5 ){
              escreva("parabens voce se manteve na casa " , casa_jogador_2)
            } 
            senao {
              casa_jogador_2 =casa_jogador_2-3
              escreva("voce voltou para a casa " , casa_jogador_2)
              //o grupo deve escolher e implementar funcionalidades propostas pela
              //própria equipe
            }
          }
          senao se(casa_jogador_2 == 21){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader: \nSeu poder é fraco.")
            escreva("\nNa próxima rodada você irá girar um dado de 4 lados")
            dado_4_lados_j2++
            //Você jogara um dado d4 na próxima rodada
          }
          senao se(casa_jogador_2 == 22){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader: \nSe não quer lutar, então ira selar o seu destino..")
            escreva("Dois jogadores deverao jogar um dado, quem tirar o menor numero devera voltar 4 casa ")
            escreva( "\n" ,nome_jogador_2, " digite 1 para rolar o dado: ")
            leia(rolardado)
            enquanto(rolardado != 1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado)
            }
            dado_jogador_2_casa_22 = u.sorteia(1, 6)
            escreva("\nrolando dado...")
            escreva(dado_jogador_2_casa_22, "\n")
            escreva( "\n" ,nome_jogador_1, " digite 1 para rolar o dado: ")
            leia(rolardado)
            enquanto(rolardado != 1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado)
            }
            dado_jogador_1_casa_22 = u.sorteia(1, 6)
            escreva("\nrolando dado...")
            escreva(dado_jogador_1_casa_22, "\n")
            se(dado_jogador_2_casa_22 > dado_jogador_1_casa_22){
              casa_jogador_1 = casa_jogador_1-4
              escreva (nome_jogador_2 ," venceu o duelo")
              escreva ("\n", nome_jogador_1 ," voltou 4 casas e esta na casa ",casa_jogador_1)
            }
            senao se(dado_jogador_2_casa_22 < dado_jogador_1_casa_22){
              casa_jogador_2 = casa_jogador_2-4
              escreva (nome_jogador_1 ," venceu o duelo")
              escreva ("\n", nome_jogador_2 ," voltou 4 casas e esta na casa ",casa_jogador_1)
            }
            senao{
          	  escreva ("Empate, os dois se mantiveram na mesma casa")
            }
          }
          senao se(casa_jogador_2 == 23){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader: \nNão há escapatória. Não me obrigue a destruí-lo!")
            escreva("\nNessa casa você deverá jogar dois dados, a soma dos dados serão as casas que você deve retroceder")
            escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar os dados: ")
        		leia(rolardado_casa23)
            enquanto(rolardado_casa23!=1){
              escreva("opcao incorreta, aperte 1 para rolar dado")
              leia(rolardado_casa23)
            }
            dado = u.sorteia(1,6)
            dado_2 = u.sorteia(1, 6)
            soma = dado + dado_2
            casa_jogador_2 = casa_jogador_2 - soma
      		  escreva("\nrolando dado... ")
       			escreva(dado)
     		   	escreva("\nrolando dado... ")
     			  escreva(dado_2)
     			  escreva("\n", nome_jogador_2  ," devera retroceder ", soma," casas")    
        	}
          //Você deve jogar dois dados, o tanto que sair, você deverá retroceder as casas
          senao se(casa_jogador_2 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader: \nNão, eu sou seu pai")
            escreva("Para avançar, gire um dado, caso tire impar podera prosseguir")
            faca{
          	  escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
          	  leia(rolardado)
          	  se(rolardado != 1){
            		escreva("opcao incorreta, aperte 1 para rolar dado")
                leia(rolardado)
          	  }
       	    } 
            enquanto(rolardado != 1)
			      escreva("\nrolando dado...")
            dado_2=u.sorteia(1, 6)
        		escreva(dado_2, "\n")
            se(dado_2==2 ou dado_2==4 ou dado_2==6){
            	escreva("Você não podera avançar")
            	rodada_jogador_2_livre = rodada_jogador_2_livre + 1
            }
            senao se(dado_2==1 ou dado_2==3 ou dado_2==5){
              casa_jogador_2 = casa_jogador_2 + dado_2
            }
            //Só avança se tirar um número impar
          }
          }
          senao se(casa_jogador_2 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa 25")
            escreva("\nPalpatine:\nSua jornada para o lado sombrio está completa.")
        		pontuacao_jogador_2 ++
        		escreva ("\nvitoria ",nome_jogador_2)
          }
          se (rodada_jogador_1_livre !=0){
            rodada_jogador_1_livre--
          }
        }
      }     
    }
  }
 }
