your token is 2A31L79asukciNyi8uppkEuSx

Pour resoudre ce challenge nous avons utilise gdb. Le binaire
fourni nous demander un uid different du notre. Par consequent nous avons lance
gdb puis disas main ensuite nous avons trouve " 0x0804859a <+14>: cmp    $0x1092,%eax"
valeur de retour de getuid, nous lui avons set un breakpoint "b * 0x0804859a "
puis nous avons fait la commande suivante "set $eax=4242" 4242 est le uid attendu par
le binaire
