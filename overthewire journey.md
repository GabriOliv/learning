Liste des défis 

bandit 0 
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

ls -la  = l for "long listing format 
        = a for "all entries"

ll      = alis de ls 

find / -name -- ''

for a dashed file : 
cat ./-

Ici, ./- signifie "le fichier nommé - dans le répertoire courant (./). En spécifiant ./-, vous indiquez explicitement à la commande cat que vous faites référence à un fichier dont le nom est "-", et non à un argument de ligne de commande.
cat < - 
This type of approach has a lot of misunderstanding because using - as an argument refers to STDIN/STDOUT i.e dev/stdin or dev/stdout .So if you want to open this type of file you have to specify the full location of the file such as ./- .For eg. , if you want to see what is in that file use cat ./-

bandit1 
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

bandit2 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

cat 'le nom du fichier avec des espaces' 

bandit3 
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

bandit4 
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

file ./*         = afficher si data ou ascii 

~ = dans mon home 
/ = dans la racine du serveur 
cd /

j'ai copié un truc, home avec le clavier pour revenir au début 

z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S


chaque user est à l'intérieur de home 


cd avec bandit6, home de /home 



cat /etc/passwd

bandit7
"The password for the next level is stored in the file data.txt next to the word millionth"
grep millionth data.txt
TESKZC0XvTetK0S9xNwm25STk5iWrBvP


With -u, --unique option
Opposite of the above option, the -u option prints unique lines i.e., non-duplicate lines. Therefore, in the below example, it prints ChhatrapatiShahuMaharaj as an output:

$ sort file2 | uniq -u

sort data.txt | uniq -u

UNIQ -U DOIT ETRE UTILISE AVEC SORT car sort va trier et rassembler les occurences car il va trier 
bandit8 EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit9 G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit10  > 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

base64 -d  data.txt

commande tr pour passer des trucs de lower case à upper case 
cat linux.txt | tr [a-z] [A-Z]


cp /home/bandit12/data.txt .
-p pour préserver les droits 
Pour copier ICI (le point)

file nous dit par quoi il a été compressé 

Pour renommer un fichier : 

mv nom nomnouveau 

Il faut bien toujours mettre la nouvelle extension pour décompresser, cas rare mais attention sinon ça peut ne pas marcher. 

CTRL + R pour voir l'historique de toutes nos commandes 

tar -xzvf 
x extraire v verbose v gzip f files 
quand c'est pas du targz pas besoin de z 

bunzip -dv 

xxd -r  
revert, convertit un fichier hexa en binaire 

alias pour voir les alias 

faire un --help au lieu d'un man 