# Exercice concernant Root me

## FTP - Authentification

`Pour résoudre cette challenge voici les étapes à faire. `

- Télécharger le fichier ch1.pcap
- Ouvrir avec wireshark
- Sur un protocol FTP on fait click droite
- Suivre / Flux TCP
- le mot de passe est le caractère qui se trouve après PASS

## TELNET - authentification

` Après avoir résolue le 1er challenge , voici les étapes pour resoudre le challenge authentificaction.`

- Télécharger le fichier ch2.pcap
- Ouvrir sur wireshark
- Sur un protocol TCP on fait un click droite
- Suivre / flux TCP
- le mot de passe c'est le mot qui se trouve après Password :

## ETHERNET - trame

` Maitenant le challenge trame`

- En demarant le challenge trame, le site nous affiche une serie de code en hexadecimal.
- Pour decoder ce code hexadecimal, on doit se rendre sur un site qui convertie un code hexadecilal en text.
- Lorsque la conversion sera fini on obtient un chaine à base 64. On reconaît ce dernier par la presence des === derier le chaine.
- on copie ce chaine puis on va sur un site qui decode les base64
- Le mot de passe est la réponse de ce base64 décoder

## Authentification twitter

`Pour resoudre le challenge twitter`

- on demarre le challenge en telechargant le fichier ch3.pcap
- on l'ouvre sur wireshark
- click droite sur la seul ligne qui apparaî dans wireshak.
- Suivre / flux TCP
- Sur la ligne Authorization , on remarque la presence d'une code base64 on copie ce code.
- On decode ce code et on obtient le mot de passe

## Bluetooth - Fichier inconnu

` Pour résoudre le challenge bleutooth`

- on télécharge le ch18.pcap en demmarant le challenge
- on ouvre ce dernier sur wireshark
- on click sur un protocol HCI EVT
- en haut on remarque l'option wireless
- on click on choisi l'option équipement bleutooth
- une fenêtre s'ouvre où on trouve l'adresse mac et le model du téléphone
- on copie l'adresse mac puis le model du téléphone (0C:B3:19:B9:4F:C6GT-S7390G)
- On decode ce code sur https://www.sha1.fr/
- La réponse sera le code du challenge

## DNS -transfert zone

`Pour résoudre ce challenge(DNS -transfert de zone), on utilse le terminal`

- On utilse la commande dig -h pour connaitre les ligne de commande que l'on veut utilisée
- Il suffie donc de suivre l'usage mentionné
- Pour savoir le ou bien connaitre la solution de ce challenge, on doit utilisé une commande comme celle de du dessus.

  `dig @challenge01.root-me.org -p 54011 ch11.challenge01.root-me.org txt `
