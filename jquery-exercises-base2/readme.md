
# Exercices JQuery - Partie 2

**IMPORTANT**
Toutes les ressources aux exercices sont fournies.

## Exercice 1
Au clic sur le bouton, afficher une boite de dialogue avec le message de votre choix.

## Exercice 2
Au double click, modifier la largeur de l'image à 500px;

 $('#image').dblclick(function(){
      $(this).width('500');
      });

## Exercice 3
Afficher ou masquer la div texte au clic des liens fournis.
 $('#afficher').click(function(){
    $('#texte').show();
  });
  $('#cacher').click(function(){
    $('#texte').hide();
  });
## Exercice 4
Au clic sur un bouton de couleur, modifier la couleur du texte de la div

$('#green').click(function(){$('#texte').css('color','green');});
$('#red').click(function(){$('#texte').css('color','red');});
$('#blue').click(function(){$('#texte').css('color','blue');});

## Exercice 5
Quand un champ a le focus, définir sa bordure à "1px solid green". Quand le champ perd le focus, définir la bordure à "1px solid red"

$('input').focusin(function(){$(this).css('border','1px solid green')});
$('input').focusout(function(){$(this).css('border','1px solid red')});

## Exercice 6
Au passage de la souris sur un bouton de couleur, colorer le texte. Le texte doit redevenir noir quand la souris quitte le bouton.

$('#green').hover(function(){$('#texte').css('color','green');},function(){$('#texte').css('color','black');});
$('#red').hover(function(){$('#texte').css('color','red');},function(){$('#texte').css('color','black');});
$('#blue').hover(function(){$('#texte').css('color','blue');},function(){$('#texte').css('color','black');});


## Exercice 7
Exercice récapitulatif des séries 1 et 2. Les instructions se trouvent dans le fichier HTML.
/* agrandir la police de caractères (120%) */
                $('#instructions :first-child').click(function(){$('body').css('font-size','120%');});
                
                /* diminuer la police de caractères (80%) */
                $('#instructions :nth-child(2)').click(function(){$('body').css('font-size','80%');});
                
                /* mettre en gras ou remettre en normal les mots en vert */
                $('#instructions :nth-child(3)').toggle(function(){$('.vert').css('font-weight','bold');}, function(){$('.vert').css('font-weight','normal');});
                
                /* souligner ou remettre en normal les mots en rouge */
                $('#instructions :nth-child(4)').toggle(function(){$('.rouge').css('text-decoration','underline');}, function(){$('.rouge').css('text-decoration','none');});
                
                /* remplacer le logo par une autre image au survol */
                $('#instructions :nth-child(5)').hover(function(){$('img').replaceWith('<img src="koala.jpg"/>');}, function(){$('img').replaceWith('<img src="jquery-logo.png"/>');});
                
                /* Afficher l'URL des liens dans une infobulle lors du survol des liens */
                $('a').hover(function(){$(this).tooltip();}) ;
                
                /* ajouter "Chapitre 1 :" devant le 1er titre h2<br>et "Chapitre 2 :" devant le 2ème titre h2 */
                $('h1').prepend('Chapitre 1 :');
                $('h2:nth-of-type(2)').prepend('Chapitre 2 :');