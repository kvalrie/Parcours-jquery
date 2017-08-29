
# Exercice Jquery - Partie 4

## Exercice 1 :

Créer une liste avec trois éléments (Pierre, Feuille, Ciseaux). Ajouter un bouton « Shifumi ! ». Lorsque l'on clique sur « Shifumi ! », choisir un élément au hasard (Pierre, Feuille ou Ciseaux). Le comparer à l'élément choisi par le joueur pour voir qui a gagné entre l'humain et la machine.

Bonus : Ajouter un compteur de victoires et de défaites et afficher le pourcentage de victoire contre l'ordinateur.

<body>

<div class="choix" >
    <button id="pierre" >Pierre</button>
    <button id="papier" >Papier</button>
    <button id="ciseaux" >Ciseaux</button>
</div>


<button id="shifumi" >SHIFUMI!</button> 

    <div id="output"></div>
    <p></p>




<script type="text/javascript" src='jquery.js' ></script>
<script>
$('#choix').css('display','flex');

var ordi = 0;
var user = 0;
var msg = "";

$('#pierre').click(function(){
     user = 1;
});

$('#papier').click(function(){
     user = 2;
});
$('#ciseaux').click(function(){
    
     user = 3;
        
});
var nb_essais = 0;
var victoire = 0;
$('#shifumi').click(function(){
    ordi = Math.floor((Math.random() * 3) + 1);
    nb_essais = nb_essais + 1;

    if(user == 1){
        if( ordi == user){
            msg = ('idem')

        }else if(ordi == 2){
            msg = ('Défaite')
        }
        else if( ordi == 3){
            msg = ('victoire')
            victoire = victoire + 1;
        }

    }else if(user == 2){

        if( ordi == user){
            msg = ('idem')

        }else if(ordi == 1){
            msg = ('Défaite')
        }
        else if( ordi == 3){
            msg = ('victoire')
            victoire = victoire + 1;
        }

    }else if(user == 3){

        if( ordi == user){
            msg = ('idem')

        }else if(ordi == 1){
            msg = ('Défaite')
        }
        else if( ordi == 2){
            msg = ('victoire')
            victoire = victoire + 1;
        }
    }

var reussite = (victoire/nb_essais)*100;
    $('p').replaceWith('<p> tu as ' + reussite + '% de reussite.lol </p>' )
    console.log(user);
    console.log(ordi);
    $('#output').text(msg);


});




</script>
</body>

## Exercice 2 :

Demander à l'aide d'un formulaire le salaire d'une personne, son genre et son nombre d'enfants.

Calculer le salaire en décomptant les frais suivants:

- Charges : 18 %;
- Assurance : 7%;
- Cotisations : 5%;

Il est possible de recevoir des réductions sur les frais totaux sous certaines conditions :

- Si l'employé est une femme, elle reçoit 2% de réduction.
- Si l'employé a 3 enfants à charge, il reçoit 1% de réduction.
- Si l'employé a 4 enfants à charge, il reçoit 2% de réduction.

## Exercice 3 :

Créer un formulaire qui demande le nom, le prénom, l'adresse mail et le numéro de téléphone de l'utilisateur.
Verifier que l'adresse mail est bien une adresse mail, vérifier que le numéro de téléphone ne comporte que des chiffres, et que le nom et le prénom ne contiennent que des lettres ou des tirets.


## Exercice 4 :

Créer un formulaire demandant le nom, le prénom, la date de naissance, le lieu de naissance, l'emploi et la société.
Créer un bouton "Générer" permettant de créer une courte phrase de présentation.

Exemple : Si les données saisies sont : "Jérôme OTT, 5/06/1990, Margny-lès-Compiègne, Formateur, Novei", la phrase de présentation sera : "Jérôme OTT, né le 5/06/1990 à Margny-lès-Compiègne, actuellement Formateur à Novei
