### Si dans une requète SQL, on écrit nom LIKE '%X_' :
Le '%' signifie qu'on s'en fou de ce qu'il y a avant le 'X', il peut y avoir une infinité de chaine de caracètres comme aucune
Le '_' est une condition, il faut que le X soit suivi obligatoirement d'un et un seul caractère.
Donc LIKE '%X_' signifie qu'on prend n'importe quel mot ou le 'X' est l'avant dernière lettre (modifié)
### 