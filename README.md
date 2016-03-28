# MBS - Monitor Batch Simples
[Aula 9] Monitor Batch Simples - Parte I
[Aula 10] Monitor Batch Simples - Parte II
# FAQ

##Q1: O que é um monitor batch?
A: O monitor batch, nesta disciplina, é um programa responsável por executar uma sequência de tarefas, ou jobs. Estes jobs são lidos de um arquivo de texto (um dispositivo do tipo mvn.dispositivo.Disco que deverá estar na Unidade Lógica 0 da MVN) que possui um formato específico (ver a próxima pergunta). O "monitor" foi o embrião dos sistemas operacionais como os conhecemos hoje, e você pode ler mais a respeito dessa evolução aqui.

##Q2: O que é um job?
A: Um job é uma tarefa que o MBS sabe executar. Na aula de hoje, o MBS deverá compreender dois tipos de job: load (LO) e dump (DU). O job de load lê os parâmetros do arquivo de texto e invoca a sub-rotina do loader, que é mesma sub-rotina desenvolvida no Lab. 7, mas que nesta aula será fornecida como material auxiliar, já escrita em linguagem simbólica. De maneira semelhante, o job de dump apenas lê os parâmetros de dump do arquivo de texto e invoca a sub-rotina do dumper (também fornecida).

##Q3: O que é a Linguagem de Controle do MBS?
A: É uma linguagem formal que define qual é o formato dos arquivos que são compreendidos pelo MBS. Se um arquivo não obedece precisamente a este formato, ele é inválido, e o seu MBS deverá usar a instrução OS da MVN para imprimir as mensagens de erro apropriadas.

##Q4: Quais são os casos de erro que o meu MBS vai precisar verificar e tratar?
A: O seu MBS deve tratar estas 4 situações de erro. Se, durante a leitura do arquivo de jobs, o MBS encontrar alguma destas situações, ele deve usar a instrução OS, conforme explicado neste slide.

##Q5: Se o MBS usa a instrução OS (implementada em Java), é melhor fazer a parte de Java (ex. 1) primeiro, certo?
A: Não. Recomendamos que você comece pela parte do MBS (assembly), pois é a parte mais complexa. Implemente o MBS assumindo que a instrução OS funciona, e depois se preocupe em implementá-la.

##Q5: Onde está o material teórico de referência para consultar?
A: Aqui. Estes são os slides da Aula 16. No laboratório de hoje, vamos usar apenas o conteúdo coberto até no slides 1 a 16. No próximo laboratório, vamos continuar trabalhando com o MBS, e com as extensões (instruções EX e CL) que são apresentadas nos slides 17 a 39.

##Q5: Como eu testo meu programa?
A: Ah, ótima pergunta. Na aula de hoje, vamos usar o SAAA (Sistema Avançadíssimo de Avaliação Automática; a pronúncia é análoga à de IEEE) para corrigir os exercícios. Isto é: você poderá corrigir os exercícios antes de submetê-los, e já saberá a nota final <Pausa para aplausos>.

#Slides de referência:

Aula 16 (teórica) (apenas slides 1 a 16)

#Arquivos fornecidos para a aula:

+dumper.asm (dumper escrito em linguagem simbólica)
+loader.asm (loader escrito em linguagem simbólica)
+utils.asm (sub-rotinas que poderão ser úteis para a implementação do MBS)
+main.asm (esqueleto do programa que você precia implementar)

#Entrega:
após executar a correção com o SAAA, enviar para o Sharif Judge um único arquivo zip (mbs-parte1.zip), contendo os seguintes arquivos:

- [ ] UnidadeControle.java: arquivo modificado para implementar a instrução OS.
- [ ] main.asm: monitor batch desenvolvido.
