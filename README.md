# Average-student-situation
Programa para exercício desenvolvido em portugol que calcula uma média ponderada entre 3 números, gerando situações de aprovado, reprovado ou uma recuperação à depender da média adquirida.
portugal.dev


programa{
  funcao inicio(){
    cadeia NomeDoAluno
    real Nota1, Nota2, Nota3, Media, Recuperacao, MediaFinal
    logico Aprovado, Reprovado

    escreva("Qual é o seu nome? ")
    leia(NomeDoAluno)

    escreva("Qual foi a sua nota na avaliação 1? ")
    leia(Nota1)
    escreva("Qual foi a sua nota na avaliação 2? ")
    leia(Nota2)
    escreva("Qual foi a sua nota na avaliação 3? ")
    leia(Nota3)


    se(Nota1 < 0 ou Nota1 >10 ou Nota2 < 0 ou Nota2 > 10 ou Nota3 < 0 ou Nota3 > 10){
      escreva("Valor inválido, insira um valor entre 0 e 10")
    }
    senao{

    Media = (Nota1 + Nota2 + Nota3) / 3
    
    escreva("Sua foi Média foi de ", Media, " - ") //Teste do cálculo da média
    }

    se (Media >= 7){
      escreva(NomeDoAluno, " está aprovado!")
    }
    
    senao se(Media < 5){
      escreva(NomeDoAluno, " está reprovado!")
    }
    
    senao se(Media < 7 ou Media >= 5){
      escreva("Qual a sua nota na recuperação? ")
      leia(Recuperacao)

      MediaFinal = (Recuperacao + Media) / 2
      escreva("Sua média final foi de ", MediaFinal, " - ")

      se(MediaFinal >= 5){
        escreva( NomeDoAluno, " está aprovado")
      }

      senao{
        escreva( NomeDoAluno, " está reprovado")
      }
    }
  }
}
