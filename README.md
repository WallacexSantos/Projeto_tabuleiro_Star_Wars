programa {
  inclua biblioteca Util --> u
  funcao inicio() {
    inteiro opcao=0, nome=0, rolardado, dado, casa_jogador_1=0, casa_jogador_2=0, menu = 0, EPISODE = 1
    inteiro pontuacao_jogador_1 = 0, pontuacao_jogador_2 = 0, opcao_casa_15 = 0, dado_jogador_1_casa_22, dado_jogador_2_casa_22
    inteiro soma ,dado_2 = 0 ,rolardado_casa15, casa_vazia = 0, rodada_jogador_1_livre = 0, rodada_jogador_2_livre = 0, dado_4_lados_j1=0, dado_4_lados_j2=0
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
    enquanto(menu == 0){
    enquanto (opcao == 0){
    faca{
        escreva("\n===================================\n")
        escreva("_________TABULEIRO STAR WARS_________\n")
        escreva("=====================================\n")
        escreva(" Digite [1] Jogar              Digite [4] Sair do Jogo\n")
        escreva(" DIgite [2] Verificar Placar\n")
        escreva(" Digite [3] Créditos\n")
        escreva("=====================================\n")
      leia(opcao)
      se (opcao  < 1 ou opcao > 4){ 
        escreva("opção invalida, digite novamente: ")
      }
    }
    enquanto(opcao  < 1 ou opcao > 4)
    limpa()
    }
//AQUI TALVEZ TENHA UM ERRO NA CONTAGEM PARA SEGUNDA VEZ QUANDO O NOME ESTIVER 1, TALVEZ NAO ENTRE AQUI
    se (opcao == 1){ 
      se (nome == 0) { nome++
        escreva("==============================================================")
        escreva("\nCada jogador deve escolher seu nome e destino: JEDI ou SITH")
        escreva("\nEssa escolha definirá o seu caminho e não pode ser desfeita")
        escreva("\nJogador 1 (JEDI). Digite o seu nome: ")
        leia(nome_jogador_1)
        escreva("\nJogador 2 (SiTH). Digite o seu nome: ")
        leia(nome_jogador_2)
        escreva("==============================================================")
      }
      se (opcao == 1){
          escreva("\n        █████████████████████████")
		escreva("\n        █─▄▄▄▄█─▄─▄─██▀▄─██▄─▄▄▀█")
		escreva("\n        █▄▄▄▄─███─████─▀─███─▄─▄█")
		escreva("\n        ▀▄▄▄▄▄▀▀▄▄▄▀▀▄▄▀▄▄▀▄▄▀▄▄▀")
		escreva("\n      █████████████████████████████")
		escreva("\n      █▄─█▀▀▀█─▄██▀▄─██▄─▄▄▀█─▄▄▄▄█")
		escreva("\n      ██─█─█─█─███─▀─███─▄─▄█▄▄▄▄─█")
		escreva("\n      ▀▀▄▄▄▀▄▄▄▀▀▄▄▀▄▄▀▄▄▀▄▄▀▄▄▄▄▄▀")
		u.aguarde(2000)
		escreva("\n                BOARD GAME          ")
		u.aguarde(500)
		escreva("\n                 EPISODE ",EPISODE,"          ")
		u.aguarde(500)
		escreva("\nHá muito tempo, em uma galáxia muito, muito distante...")
		u.aguarde(500)
		escreva("\n\nA galáxia vive um momento de tensão.")
		escreva("\nDois caminhos se erguem diante daqueles sensíveis à Força:  .")
		u.aguarde(500)
		escreva("\no caminho da luz, seguido pelos nobres Jedi,  ")
		u.aguarde(500)
		escreva("\ne o caminho da escuridão, dominado pelos poderosos Sith.")
		u.aguarde(500)
		escreva("\n\nEm meio a esse conflito, dois destinos começam a se cruzar.")
		u.aguarde(500)
		escreva("\nDe um lado, ",nome_jogador_1," trilhando o caminho da luz.  ")
		u.aguarde(500)
		escreva("\nDo outro, ",nome_jogador_2," abraçando o poder do lado sombrio.")
		u.aguarde(500)
		escreva("\n\nCada decisão poderá alterar o rumo da jornada,")
		u.aguarde(500)
		escreva("\ne cada passo pode aproximá-los da vitória… ou da queda.")
		u.aguarde(500)
		escreva("\nEscolha seu caminho... e que a Força esteja com você.")
		u.aguarde(500)
		escreva("\n==============================================================")
      }
    }
    se (opcao == 1) {
      casa_jogador_1 = 0
      casa_jogador_2 = 0
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
        }senao{
        	dado = u.sorteia(1, 6)
        	escreva("rolando dado...")
        	escreva(dado, "\n")
        	casa_jogador_1 = casa_jogador_1 + dado
        }
        se(casa_jogador_1 == 1) {
          escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
     	escreva("\nQue a Força esteja com você")
        } senao se(casa_jogador_1 == 2){
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
          	}    
               dado = u.sorteia(1, 3)
               escreva("\nrolando dado...")
               escreva(dado, "\n")
               casa_jogador_1 = casa_jogador_1 + dado
               escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
               
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
          }
        }
        enquanto(rolardado != 1)
        dado = u.sorteia(1, 6)
        escreva("\nrolando dado...")
        escreva(dado, "\n")
              se  ( dado==2 ou dado==4 ou dado==6 ) {
              escreva("parabens voce se manteve na casa " , casa_jogador_1)
              } senao {
              casa_jogador_1 = casa_jogador_1-3 
                escreva("voce voltou para a casa " , casa_jogador_1)
                        //o grupo deve escolher e implementar funcionalidades propostas pela
//própria equipe
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
            escreva("Dois jogadores deverao jogar um dado, quem tirar o menor numero devera voltar 4 casa ")
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
        		 leia(rolardado_casa15)
        		 se(rolardado_casa15==1){
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
          se(rolardado_casa15 != 1){
            escreva("opcao incorreta, aperte 1 para rolar dado")
          }
    	   
                  
                        //Você deve jogar dois dados, o tanto que sair, você deverá retroceder as casas
          }
          senao se(casa_jogador_1 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
            escreva("\nLuke Skywalker:\nEu sou um Jedi, como meu pai antes de mim.")
            escreva("Para avançar, gire um dado, caso tire par podera prosseguir")
            faca{
          	escreva( "\n" ,nome_jogador_1, " ,digite 1 para rolar o dado: ")
          	leia(rolardado)
          	se(rolardado != 1){
            		escreva("opcao incorreta, aperte 1 para rolar dado")
          	}
       	 }enquanto(rolardado != 1)
			escreva("\nrolando dado...")
        		escreva(dado, "\n")
           	 dado_2=u.sorteia(1, 6)
            se(dado_2==1 ou dado_2==3 ou dado_2==5){
            	escreva("Você não podera avançar")
            	rodada_jogador_1_livre = rodada_jogador_1_livre + 1
            	
            }
                        //Só avança se tirar um número par
          }
          senao se(casa_jogador_1 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa 25")
            escreva("\nYoda:\nUm Jedi você se tornou.")
            pontuacao_jogador_1 ++
            EPISODE ++
        		escreva ("\nvitoria ",nome_jogador_1)
            u.aguarde(2000)
            opcao = 0
          
          }
          se (rodada_jogador_2_livre !=0){
          	rodada_jogador_2_livre--
          }
          }
          se (casa_jogador_1 <25)
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
        }senao{
        dado = u.sorteia(1, 6)
        escreva("rolando dado...")
        escreva(dado, "\n")
        casa_jogador_2 = casa_jogador_2 + dado
        }
        se(casa_jogador_2 == 1) {
          escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
          escreva("\nDarth Maul: \nFinalmente vamos nos revelar aos Jedi. Finalmente teremos vingança.")
        } senao se(casa_jogador_2 == 2){
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
          	}    
               dado = u.sorteia(1, 3)
               escreva("\nrolando dado...")
               casa_jogador_2 = casa_jogador_2 + dado
               escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_1)
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
            		escreva("\nRecite a frase: Não, eu sou sei pai")
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
          }
        }
        enquanto(rolardado != 1)
        dado = u.sorteia(1, 6)
        escreva("\nrolando dado...")
        escreva(dado, "\n")
        se  ( dado==1 ou dado==3 ou dado==5 ) {
              escreva("parabens voce se manteve na casa " , casa_jogador_2)
              } senao {
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
          senao se(casa_jogador_2 == 23){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader: \nNão há escapatória. Não me obrigue a destruí-lo!")
            escreva ("\nNessa casa você deverá jogar dois dados, a soma dos dados serão as casas que você deve retroceder")
                  	escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar os dados: ")
        		 	leia(rolardado_casa15)
        		 se(rolardado_casa15==1){
            		dado = u.sorteia(1,6)
                 	dado_2 = u.sorteia(1, 6)
                    soma = dado + dado_2
                    casa_jogador_2 = casa_jogador_2 - soma
      		  	escreva("\nrolando dado...")
       			escreva(dado)
     		   	escreva("\nrolando dado...")
     			escreva(dado_2)
     			escreva("\n", nome_jogador_2  ," devera retroceder ", soma," casas")    
        		 }senao se(rolardado_casa15 != 1){
            		escreva("opcao incorreta, aperte 1 para rolar dado")
         		 }
          }
               //Você deve jogar dois dados, o tanto que sair, você deverá retroceder as casas
               
          senao se(casa_jogador_2 == 24){
            escreva("voce andou " ,dado, " casas, e está na casa " ,casa_jogador_2)
            escreva("\nDarth Vader: \nNão, eu sou sei pai")
            escreva("Para avançar, gire um dado, caso tire impar podera prosseguir")
            faca{
          	escreva( "\n" ,nome_jogador_2, " ,digite 1 para rolar o dado: ")
          	leia(rolardado)
          	se(rolardado != 1){
            		escreva("opcao incorreta, aperte 1 para rolar dado")
          	}
       	 }enquanto(rolardado != 1)
			escreva("\nrolando dado...")
        		escreva(dado, "\n")
           	 dado_2=u.sorteia(1, 6)
            se(dado_2==1 ou dado_2==3 ou dado_2==5){
            	escreva("Você não podera avançar")
            	rodada_jogador_2_livre = rodada_jogador_2_livre +1
            }
            
                        //Só avança se tirar um número impar
          }
          senao se(casa_jogador_2 >= 25){
            escreva("voce andou " ,dado, " casas, e está na casa 25")
            escreva("\nPalpatine:\nSua jornada para o lado sombrio está completa.")
        		pontuacao_jogador_2 ++
        		escreva ("\nvitoria ",nome_jogador_2)
            EPISODE ++
            u.aguarde(2000)
            opcao = 0
        
                   	}
                   se (rodada_jogador_1_livre !=0){
          	    rodada_jogador_1_livre--
          }
          }
      }     
  }
  se (opcao == 2){
  	escreva("\n==============================================================")
  	escreva("\n____________________________PLACAR____________________________")
  	escreva ("\n\n",nome_jogador_1," ", pontuacao_jogador_1," vitórias")
  	escreva ("\n",nome_jogador_2," ", pontuacao_jogador_2," vitórias")
  	se (pontuacao_jogador_1 == pontuacao_jogador_2){
  	   escreva("\nA Força está em equilíbrio")
  	}
  	senao se (pontuacao_jogador_1 > pontuacao_jogador_2){
  	   escreva("\nA Força tende para a luz.")
  	}
  	senao se (pontuacao_jogador_1 < pontuacao_jogador_2){
  	   escreva("\nO lado sombrio está dominando.")
  	}
  	escreva ("\nDigite [0] para retornar ao menu ")
  	leia (opcao)
  	enquanto (opcao !=0){ 
        escreva("opção invalida, Digite [0] para retornar ao menu: ")
        leia (opcao)
    escreva("\n==============================================================")
      }
      limpa()
  }
  se (opcao == 3){
u.aguarde(100)
escreva("                            ,ooo888888888888888oooo,")
u.aguarde(100)
escreva("\n                          o8888YYYYYY77iiiiooo8888888o                             ██      ██   ██████   ██       ██       ██████    ██████   ████████")
u.aguarde(100)
escreva("\n                         8888YYYY77iiYY8888888888888888                            ██      ██  ██    ██  ██       ██      ██    ██  ██    ██  ██")
u.aguarde(100)
escreva("\n                        [88YYY77iiY88888888888888888888]                           ██      ██  ██    ██  ██       ██      ██    ██  ██        ██")
u.aguarde(100)
escreva("\n                        88YY7iYY888888888888888888888888                           ██  ██  ██  ████████  ██       ██      ████████  ██        ██████")
u.aguarde(100)
escreva("\n                       [88YYi 88888888888888888888888888]                          ██  ██  ██  ██    ██  ██       ██      ██    ██  ██        ██")
u.aguarde(100)
escreva("\n                       i88Yo8888888888888888888888888888i                          ██  ██  ██  ██    ██  ██       ██      ██    ██  ██        ██")
u.aguarde(100)
escreva("\n                       i|        ^^^88888888^^^     o  [i                          ██  ██  ██  ██    ██  ██       ██      ██    ██  ██    ██  ██")
u.aguarde(100)
escreva("\n                      oi8  i           o8o          i  8io                         ████████    ██    ██  ████████ ███████ ██    ██   ██████   ████████")
u.aguarde(100) 
escreva("\n                    ,77788o ^^  ,oooo8888888ooo,   ^ o88777,                       ")
u.aguarde(100)
escreva("\n                    7777788888888888888888888888888888877777                       ")
u.aguarde(100)
escreva("\n                     77777888888888888888888888888888877777                        ")
u.aguarde(100)
escreva("\n                      77777788888888^7777777^8888888777777                         ")
u.aguarde(100)
escreva("\n       ,oooo888 ooo   88888778888^7777ooooo7777^8887788888        ,o88^^^^888oo          ██████   ██████    ██████   ██      ██  ████████")
u.aguarde(100)
escreva("\n    o8888777788[];78 88888888888888888888888888888888888887 7;8^ 888888888oo^88              ██  ██    ██  ██    ██  ██      ██  ██")
u.aguarde(100)
escreva("\n   o888888iii788 ]; o 78888887788788888^;;^888878877888887 o7;[]88888888888888o              ██  ██    ██  ██        ██      ██  ██")
u.aguarde(100)
escreva("\n   88888877 ii78[]8;7o 7888878^ ^8788^;;;;;;^878^ ^878877 o7;8 |878888888888888              ██  ██    ██   ██████   ██      ██  ██████")
u.aguarde(100)
escreva("\n  [88888888887888 87;7oo 777888o8888^;ii;;ii;^888o87777 oo7;7[]8778888888888888              ██  ██    ██        ██  ██      ██  ██")
u.aguarde(100)
escreva("\n  88888888888888[]87;777oooooooooooooo888888oooooooooooo77;78]88877i78888888888              ██  ██    ██        ██  ██      ██  ██")
u.aguarde(100)
escreva("\n o88888888888888 877;7877788777iiiiiii;;;;;iiiiiiiii77877i;78| 88877i;788888888      ██      ██  ██    ██  ██    ██  ██      ██  ██ ")
u.aguarde(100)
escreva("\n 88^;iiii^88888 o87;78888888888888888888888888888888888887;778| 88877ii;7788888      ██      ██  ██    ██  ██    ██  ██      ██  ██")
u.aguarde(100)
escreva("\n;;;iiiii7iiii^  87;;888888888888888888888888888888888888887;778| 888777ii;78888       ████████    ██████    ██████    ████████   ████████")
u.aguarde(100)
escreva("\n;iiiii7iiiii7iiii77;i88888888888888888888i7888888888888888877;77i 888877777ii78    ")
u.aguarde(100)
escreva("\niiiiiiiiiii7iiii7iii;;;i7778888888888888ii7788888888888777i;;;;iiii 88888888888    ")
u.aguarde(100)
escreva("\ni;iiiiiiiiiiii7iiiiiiiiiiiiiiiiiiiiiiiiii8877iiiiiiiiiiiiiiiiiii877   88888        ")
u.aguarde(100)
escreva("\nii;;iiiiiiiiiiiiii;;;ii^^^;;;ii77777788888888888887777iii;;  77777           78    ")
u.aguarde(100)
escreva("\n77iii;;iiiiiiiiii;;;ii;;;;;;;;;^^^^8888888888888888888777ii;;  ii7         ;i78    ████████      ██     ██      ██  ██  ████████  ██")
u.aguarde(100)
escreva("\n^ii;8iiiiiiii ';;;;ii;;;;;;;;;;;;;;;;;;^^oo ooooo^^^88888888;;i7          7;788    ██     ██    ████    ███     ██  ██  ██        ██")
u.aguarde(100)
escreva("\no ^;;^^88888^     'i;;;;;;;;;;;;;;;;;;;;;;;;;;;^^^88oo^^^^888ii7         7;i788    ██     ██   ██  ██   ████    ██  ██  ██        ██")
u.aguarde(100)
escreva("\n88ooooooooo         ;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;; 788oo^;;          7;i888    ██     ██  ██    ██  ██ ██   ██  ██  ██████    ██")
u.aguarde(100)
escreva("\n887ii8788888      ;;;;;;;ii;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;^87           7;788    ██     ██  ████████  ██  ██  ██  ██  ██        ██")
u.aguarde(100)
escreva("\n887i8788888^     ;;;;;;;ii;;;;;;;oo;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;,,,      ;;888    ██     ██  ██    ██  ██   ██ ██  ██  ██        ██")
u.aguarde(100)
escreva("\n87787888888     ;;;;;;;ii;;;;;;;888888oo;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;,,;i788     ██     ██  ██    ██  ██    ████  ██  ██        ██")
u.aguarde(100)
escreva("\n87i8788888^       ';;;ii;;;;;;;8888878777ii8ooo;;;;;;;;;;;;;;;;;;;;;;;;;;i788 7    ██     ██  ██    ██  ██     ███  ██  ██        ██")
u.aguarde(100)
escreva("\n77i8788888           ioo;;;;;;oo^^ooooo ^7i88^ooooo;;;;;;;;;;;;;;;;;;;;i7888 78    ████████   ██    ██  ██      ██  ██  ████████  ████████")
u.aguarde(100)
escreva("\n7i87788888o         7;ii788887i7;7;788888ooooo7888888ooo;;;;;;;;;;;;;;oo ^^^ 78    ")
u.aguarde(100)
escreva("\ni; 7888888^      8888^o;ii778877;7;7888887;;7;7788878;878;;    ;;;;;;;i78888o ^    ")
u.aguarde(100)
escreva("\ni8 788888       [88888^^ ooo ^^^^^;;77888^^^^;;7787^^^^ ^^;;;;  iiii;i78888888     ")
u.aguarde(100)
escreva("\n^8 7888^        [87888 87 ^877i;i8ooooooo8778oooooo888877ii; iiiiiiii788888888     ")
u.aguarde(100)
escreva("\n  ^^^          [7i888 87;; ^8i;;i7888888888888888887888888   i7iiiiiii88888^^      ██      ██   ██████   ██    ██   ██████    ██████   ██    ██")
u.aguarde(100)
escreva("\n               87;88 o87;;;;o 87i;;;78888788888888888888^^ o 8ii7iiiiii;;          ███    ███  ██    ██   ██  ██   ██    ██  ██    ██  ███   ██")
u.aguarde(100)
escreva("\n               87;i8 877;77888o ^877;;;i7888888888888^^ 7888 78iii7iii7iiii        ████  ████  ██    ██    ████    ██        ██    ██  ████  ██")
u.aguarde(100)
escreva("\n               ^87; 877;778888887o 877;;88888888888^ 7ii7888 788oiiiiiiiii         ██ ████ ██  ████████     ██     ██        ██    ██  ██ ██ ██")
u.aguarde(100)
escreva("\n                 ^ 877;7 7888888887 877i;;8888887ii 87i78888 7888888888            ██  ██  ██  ██    ██     ██     ██        ██    ██  ██  ████")
u.aguarde(100)
escreva("\n                  [87;;7 78888888887 87i;;888887i  87ii78888 7888888888]           ██      ██  ██    ██     ██     ██        ██    ██  ██   ███")
u.aguarde(100)
escreva("\n                  877;7 7788888888887 887i;887i^  87ii788888 78888888888           ██      ██  ██    ██     ██     ██    ██  ██    ██  ██    ██")
u.aguarde(100)
escreva("\n                  87;i8 788888888888887 887ii;;^ 87ii7888888 78888888888           ██      ██  ██    ██     ██      ██████    ██████   ██    ██")
u.aguarde(100)
escreva("\n                 [87;i8 7888888888888887 ^^^^   87ii77888888 78888888888           ")
u.aguarde(100)
escreva("\n                 87;;78 7888888888888887ii      87i78888888 778888888888           ")
u.aguarde(100)
escreva("\n                 87;788 7888888888888887i]      87i78888888 788888888888           ")
u.aguarde(100)
escreva("\n                [87;88 778888888888888887       7ii78888888 788888888888           ")
u.aguarde(100)
escreva("\n                87;;88 78888888888888887]       ii778888888 78888888888]            ██████      ██     ███    ███  ██      ██  ████████  ██")
u.aguarde(100)
escreva("\n                7;;788 7888888888888888]        i7888888888 78888888888'           ██    ██    ████    ████  ████  ██      ██  ██        ██")
u.aguarde(100)
escreva("\n                7;;788 7888888888888888         'i788888888 78888888888            ██         ██  ██   ██ ████ ██  ██      ██  ██        ██")
u.aguarde(100)
escreva("\n                7;i788 788888888888888]          788888888 77888888888|             ██████   ██    ██  ██  ██  ██  ██      ██  ██████    ██")
u.aguarde(100)
escreva("\n                '7;788 778888888888888|         [788888888 78888888888'                  ██  ████████  ██      ██  ██      ██  ██        ██")
u.aguarde(100)
escreva("\n                ';77888 78888888888888          8888888888 7888888888]                   ██  ██    ██  ██      ██  ██      ██  ██        ██")
u.aguarde(100)
escreva("\n                 778888 78888888888888          8888888888 7888888888|             ██    ██  ██    ██  ██      ██  ██      ██  ██        ██ ")
u.aguarde(100)
escreva("\n                  78888 7888888888888|         [8888888888 7888888888               ██████   ██    ██  ██      ██   ████████   ████████  ████████ ")
u.aguarde(100)
escreva("\n                   7888 788888888888]          88888888888 788888888|              ")
u.aguarde(100)
escreva("\n                    778 78888888888|           |888888888 778888888|               ")
u.aguarde(100)
escreva("\n                    oooooo ^88888^              ^88888^^^^^^^^8888|                ")
u.aguarde(100)
escreva("\n                   87;78888ooooooo8o            ,oooooo oo888oooooo                ")
u.aguarde(100)
escreva("\n                   [877;i77888888888]          [;78887i8888878i7888;                ██████   ████████  ████████  ██    ██  ██    ██  ████████")
u.aguarde(100)
escreva("\n                    ^877;;ii7888ii788          ;i777;7788887787;778;               ██    ██  ██     ██    ██     ██    ██  ██    ██  ██     ██")
u.aguarde(100)
escreva("\n                     ^87777;;;iiii777          ;77^^^^^^^^^^^^^^^^;;               ██    ██  ██     ██    ██     ██    ██  ██    ██  ██     ██")
u.aguarde(100)
escreva("\n                        ^^^^^^^^^ii7]           ^ o88888888877iiioo                ████████  ████████     ██     ████████  ██    ██  ████████")
u.aguarde(100)
escreva("\n                           77777o               [88777777iiiiii;;778               ██    ██  ██   ██      ██     ██    ██  ██    ██  ██   ██ ")
u.aguarde(100)
escreva("\n                           77777iii            8877iiiii;;;77888888]               ██    ██  ██    ██     ██     ██    ██  ██    ██  ██    ██")
u.aguarde(100)
escreva("\n                            77iiii;8           [77ii;778 788888888888              ██    ██  ██     ██    ██     ██    ██  ██    ██  ██     ██")
u.aguarde(100)
escreva("\n                            7iii;;88           iii;78888 778888888888              ██    ██  ██      ██   ██     ██    ██   ██████   ██      ██")
u.aguarde(100)
escreva("\n                           77i;78888]          ;;;;i88888 78888888888              ")
u.aguarde(100)
escreva("\n                          ,7;78888888          [;;i788888 7888888888]              ")
u.aguarde(100)
escreva("\n                          i;788888888           ;i7888888 7888888888               ")
u.aguarde(100)
escreva("\n                          ;788888888|           i77888888 788888888|               ")
u.aguarde(100)
escreva("\n                          ';88888888'           [77888888 788888888]               ███    ███  ██  ██    ██   ██████    ████████  ██")
u.aguarde(100)
escreva("\n                           |[8ooo88]             78888888 788888888                ████  ████  ██  ██   ██   ██    ██   ██        ██")
u.aguarde(100)
escreva("\n                           [88888]               78888888 788888888                ██ ████ ██  ██  ██  ██    ██    ██   ██        ██")
u.aguarde(100)
escreva("\n                              ^^^                [7888888 77888888]                ██  ██  ██  ██  █████     ████████   ██████    ██")
u.aguarde(100)
escreva("\n                                                  88888888 7888887                 ██      ██  ██  ██  ██    ██    ██   ██        ██")
u.aguarde(100)
escreva("\n                                                  77888888 7888887                 ██      ██  ██  ██   ██   ██    ██   ██        ██")
u.aguarde(100)
escreva("\n                                                   ;i88888 788888i                 ██      ██  ██  ██    ██  ██    ██   ██        ██")
u.aguarde(100)
escreva("\n                                                  ,;;78888 788877i7                ██      ██  ██  ██     ██ ██    ██   ████████  ████████")
u.aguarde(100)
escreva("\n                                                 ,7;;i;777777i7i;;7                ")
u.aguarde(100)
escreva("\n                                                 87778^^^ ^^^^87778                ")
u.aguarde(100)
escreva("\n                                                  ^^^^ o777777o ^^^                ")
u.aguarde(100)
escreva("\n                                                  o77777iiiiii7777o                ")
u.aguarde(100)
escreva("\n                                                 7777iiii88888iii777             ====================================== ")
u.aguarde(100)
escreva("\n                                                ;;;i7778888888877ii;;            | Digite [0] para retornar ao menu   |")
u.aguarde(100)
escreva("\n                                               |i77888888^^^^8888877i|           | Digite [1] para repitir a animação |")
u.aguarde(100)
escreva("\n                 (PROJETO STAR BOARD)          77888^oooo8888oooo^8887|          ======================================  ")
u.aguarde(100)
escreva("\n                                              |788888888888888888888888|           ")
u.aguarde(100)
escreva("\n                                              88888888888888888888888888           ")
u.aguarde(100)
escreva("\n                                              |8888888^iiiiiiiii^888888|           ")
u.aguarde(100)
escreva("\n                                                iiiiiiiiiiiiiiiiiiiiii             ")
u.aguarde(100)
escreva("\n                                                    ^^^^^^^^^^^^^                  ")
leia (opcao)
se (opcao == 1){
  opcao = 3
}
enquanto (opcao <0 e opcao >1){ 
        escreva("opção invalida, Digite [0] para retornar ao menu: ")
        leia (opcao)
      }
      limpa()

  }
  se (opcao == 4) {
   menu++
  }
  }
 }
}

