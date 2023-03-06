## AWK Tutoriels

### Ressources

google => awk filetype:pdf

### Histoire

### Introduction général (utilisation basic)

travail sur des fichiers textes en mode ligne par ligne.
Une ligne est par défaut terminée par un retourn à la ligne. 
Retour à ligne : EOL (\n)


awk "[filtre] {traitement}; "


filtre:
    /motif/ => regex
    /motif1/,/motif2/ => interval de ligne à traiter. 
                         dès qu'une ligne contient le <motif1>
                         on afficher jusqu'à la ligne qui contient
                         le motif <motif2> (inclus)

    expression => dans un test logique



BEGIN {}
[filtre] {}
END {}

#### print

print $
print


#### Variables Interne
    - $0  : enregistrement en cours (la ligne courante)
    - $i  : $1,$2 ... les champs de l'enregistrement
    - FS  : field separator => séparateur de champ par défaut
    - NR  : number record (compteur du nombre d'enregistrements lus)
    - FNR :

### 

### implémentations

#### awk 
    la base => commun à toutes les implems

#### gawk
    - [gnu official600](https://www.gnu.org/software/gawk/manual/gawk.pdf)

    - mailing list
        + [bug](https://lists.gnu.org/mailman/listinfo/bug-gawk)
        + [help](https://lists.gnu.org/archive/html/help-gawk/)

    - sources
        => tests unitaires

#### mawk
#### tawk
#### redit /stack / ???



#### astuces / onliner

##### compter le nombre de lignes d'un fichier
awk 'END {print NR}' fichier

##### affichier le contenu d'un fichier
awk '1' fichier

##### numéroter les lignes
awk '{ print NR" "$0 }'














