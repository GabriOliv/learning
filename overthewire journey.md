BANDIT 0 

ls -la  = l for "long listing format 
        = a for "all entries"

find / -name -- ''

for a dashed file : 
cat ./-

Ici, ./- signifie "le fichier nommé - dans le répertoire courant (./). En spécifiant ./-, vous indiquez explicitement à la commande cat que vous faites référence à un fichier dont le nom est "-", et non à un argument de ligne de commande.
cat < - 
This type of approach has a lot of misunderstanding because using - as an argument refers to STDIN/STDOUT i.e dev/stdin or dev/stdout .So if you want to open this type of file you have to specify the full location of the file such as ./- .For eg. , if you want to see what is in that file use cat ./-
