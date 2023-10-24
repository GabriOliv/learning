My little linux toolbox : 

COMMANDES : 

LS

ls -la  = l for "long listing format 
        = a for "all entries"

ll      = alias de ls 



LOCATE

Pour chercher un fichier, priviliger locate (apt get updatedb  + apt get findultils ) 


FIND

Sinon avec find 

  find /  -type f -user hidra -name uwu.TXT



find . -name thisfile.txt

If you need to know how to find a file in Linux called thisfile.txt, it will look for it in current and sub-directories.

file ./uwu.txt
Pour savoir si ASCII ou DATA

FIND + GREP 

Use Grep to Find Files Based on Content
The find command in Linux is great but it can only filter the directory tree according to filename and meta data. To search files based on what they contain you’ll need a tool like grep. Take a look:

find . -type f -exec grep "forinstance" '{}' \; -print

This goes through every object in the current directory tree (.) that’s a file (-type f) and then runs grep ” forinstance ” for every file that matches, then prints them on the screen (-print). The curly braces ({}) are a placeholder for those results matched by the Linux find command. The {} go inside single quotes (‘) so that grep isn’t given a misshapen file name. The -exec command is ended with a semicolon (;), which also needs an escape (\;) so that it doesn’t end up being interpreted by the shell.

Before -exec was implemented, xargs would have been used to create the same kind of output:

find . -type f -print | xargs grep "forinstance"


UNIQ ET SORT 

With -u, --unique option
Opposite of the above option, the -u option prints unique lines i.e., non-duplicate lines. Therefore, in the below example, it prints ChhatrapatiShahuMaharaj as an output:

$ sort file2 | uniq -u

sort data.txt | uniq -u

UNIQ -U DOIT ETRE UTILISE AVEC SORT car sort va trier et rassembler les occurences et ne pas prendre en compte les lignes dupliquées. 

CAT 

 for a dashed file : 
cat ./-

Ici, ./- signifie "le fichier nommé - dans le répertoire courant (./). En spécifiant ./-, vous indiquez explicitement à la commande cat que vous faites référence à un fichier dont le nom est "-", et non à un argument de ligne de commande.

Sinon 

cat < - 

ECHO 

$ echo $PWD 
/Users/Name/Desktop
Vous avez également la possibilité de combiner la sortie des variables avec du texte, comme dans l’exemple ci-dessous :

$ echo "Vous êtes dans le répertoire : $PWD" 
Vous êtes dans le répertoire : /Users/Name/Desktop

Pour créer un fichier et écrire dedans : 

echo 'miaou' > chat.txt

Si je veux rajouter un deuxième miaou 

echo 'miaou' >> chat.txt

Si je veux que ça remplace tout, je réutilise > 

WC 

wc stands for word count. As the name implies, it is mainly used for counting purpose.
1 = LIGNES 
2 = NOMBRES DE MOTS 
3 = CARACTERES/BYTES (A character is one byte in ASCII)

Si on veut juste le nombre de mots on rajoute -w 
Si on veut juste le nombre de lignes on rajout -l 
Le nombre de bytes -c 

It is used to find out number of lines, word count, byte and characters count in the files specified in the file arguments.
By default it displays four-columnar output.
First column shows number of lines present in a file specified, second column shows number of words present in the file, third column shows number of characters present in file and fourth column itself is the file name which are given as argument.

SED : 

sed 's/o/O' <.monfichier >sed-test
Le s stand for substitution, ici on va remplacer le premier o par un O dans chaque ligne 

Si on veut remplacer tous les o par des O : 
sed 's/o/O' <.monfichier >sed-test
Le g stand for global 

Attention utiliser le -i pour changement sinon ça affiche seulement sans faire de changement en dur 

sed -i 's/find/replace/g' filename

Mettre des espaces quand on veut pas modifier string random mais plutôt un mot particulier 
On peut aussi changer les délimiteurs (le caractère après le s) pour éviter toute confusion, si on change un /etc par exemple //etc// ne marchera pas il faudra utiliser : 
sed 's@/etc@lechangement@/' nomdufichier
Le @ après etc est l'autre délimiteur 
On peut aussi ne rien mettre pour remplacer par rien 
sed 's@/etc@@/' nomdufichier

tldr sed | sed 'Replace/s/the/THE/' 

On demande à sed d'aller dans son tldr, et de trouver toutes les lignes où y'a le pattern "Replace" après s pour subtitution et on lui demande de remplacer the par THE dans ces lignes 


Tools such as head and tail allow us to view the bottom or the top of a file. What if we need to view a section in the middle? The following sed one-liner will return lines 5 through 10 from tecmint.txt:

sed -n '5,10p' tecmint.txt


NAVIGATION :

Où suis-je ? 

~ = dans mon home 
/ = dans la racine du serveur 



