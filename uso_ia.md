maryana:

ferramenta: IA overview do google
trecho: bugs na compilação
finalidade: pesquisei o por que recebia "multiple <<EOF>> rules for start condition COMMENT" na hora de compilar o flex e recebia um loop de eof
o que fiz: entendi que o flex encontrava mais de 1 regra de EOF por que todas as regras de EOF devem seguir o mesmo caminho para o final e quando analisei o do comment não estava, o que também dava loop se não padronizasse, então no <<EOF>>{return END_OF_FILE;} precisava de um <<INITIAL>> e a outra regra de EOF deveria se referir a esse INITIAL quando fosse ativada


ferramenta: IA overview do google
trecho: expressões regulares
finalidade: entender expressões regulares para os erros
o que fiz: entendi como escrevia as expressões regulares

ferramente: claude
trecho: revisão
finalidade: ver se estava tudo certo
o que fiz: entendi o feedback e onde dizia que estava errado eu ia corrigir (mas não dando o trecho para copiar)

mileny:

ferramenta: Claude
trecho: regra de reconhecimento de inteiros negativos
finalidade: pedi uma explicação de como o flex funciona ao casar padrões, para entender como implementar a lógica que diferencia quando um "-" é subtração e quando faz parte de um número negativo.
O que fiz: entendi o conceito de lookahead com yyless() e escrevi a regra, adaptando a verificação de ultimo_token aos tokens do meu arquivo


ferramenta: Claude 
trecho: regras de palavras reservadas, operadores relacionais/lógicos, pontuação e constantes inteiras em microc.flex
finalidade: pedi uma revisão desses trechos do código, comparando com os requisitos do enunciado (Secao 4 e 5), para verificar se os tokens estavam corretos e se faltava algo
o que fiz: usei a revisão como verificação — identifiquei que faltava atualizar a variável ultimo_token em algumas regras e corrigi

Ferramenta: Claude Haiku 5.5
Trecho: Scanner (microc/scanner.c, microc/microc.flex)
Finalidade: foi pedido para estruturar o adaptador do scanner do TP1 e corrigir o que não estava funcionando
O que fiz: recebi a sugestão de estrutura do adaptador, a separação do YYSTYPE em microc_yylval.h e a troca das mensagens de erro por strdup. Compilei, testei e corrigi o que deu erro.

Ferramenta: Claude Haiku 5.5
Trecho: Gerador (src/codegen.c)
Finalidade: foi pedido para implementar a leitura do arquivo de tokens (opção --tokens) e para encontrar a causa do erro 'entrada' undeclared no main gerado
O que fiz: recebi a proposta da função gen_token_de_arquivo, que testei com um arquivo de tokens de exemplo. Ajustei o formato aceito pelo sscanf e o tratamento da vírgula antes de linha, depois de o teste apontar o problema. Também identifiquei que um parser.c editado à mão estava desatualizado e decidi regenerá-lo em vez de manter a edição manual.

Ferramenta: Claude Haiku 5.5
Trecho: Depuração (saída do valgrind e erros de compilação)
Finalidade: foi pedido para interpretar os blocos still reachable do valgrind e localizar a causa dos erros de compilação
O que fiz: executei os comandos, colei as saídas de volta e verifiquei que o soma.mc não tinha vazamentos. Concluí que os 16.930 bytes still reachable no caminho de erro léxico são buffers do flex que não foram liberados, não vazamento, e decidi não alterar o gerador só para zerá-los.
