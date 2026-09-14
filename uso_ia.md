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
