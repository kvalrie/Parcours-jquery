
# Exercice Jquery - Partie 3

**IMPORTANT**
Vous devez utiliser Jquery pour faire les exercices.

## Exercice 1
Construisez une page html avec un bouton et un champ texte dans lequel on affiche le nombre de clics sur le bouton.

## Exercice 2
Construisez une page html avec un bouton "+", un bouton "-" et un champ texte dans lequel on augmente ou baisse le chiffre en fonction des boutons cliqués.

## Exercice 3
Construisez une page html avec un bouton et un champ texte. Le but est de trouver un nombre entre 0 et 100. A chaque réponse la page répond :
- plus
- moins
- correct

Quand la réponse est trouvée, on obtient le nombre d'essai que l'on a fait.

var good =17;
    var plus=0;
    
    $('button').click(function(){
                plus=plus+1;
        if ($('input').val() > good){
            $('p:first-of-type').replaceWith('<p>Less</p>');

        }
        
        else if($('input').val() < good){
            $('p:first-of-type').replaceWith('<p>More</p>');
        
        }else if($('input').val() == good){
            

            $('p:first-of-type').replaceWith('<p>Correct</p>');
            
            $('p:last-of-type').replaceWith('<p>You have tried :'+plus+' times.</p>');
        }
    });

## Exercice 4
Construisez une page html avec 5 boutons et un rectangle. Chaque bouton provoque une action sur le rectangle.
- Bouton 1 : augmente la hauteur de 10px, si il dépasse 100px, il remet la hauteur à 10px
- Bouton 2 : met le rectangle en vert
- Bouton 3 : remet les couleurs initiales
- Bouton 4 : fait disparaître le rectangle
- Bouton 5 : fait réaparaître le rectangle


    // gaffe aux setter et aux getter .
    //<div>
    $('div').css('border','1px solid black');
    
    //bouton 1 :
    
    var hauteur=0;
    $('button:first-of-type').click(function(){
        
        console.log($('div').height());
        
        if($('div').height() <= 100 ){
            
            hauteur = hauteur +10;
        
        $('div').height(hauteur)
        //console.log(hauteur)

        } 
        else if( $('div').height() > 100 ){
            hauteur = 10;
            $('div').height(hauteur);

        }
    })

    // Bouton 2: 

    $('button:nth-of-type(2)').click(function(){
        $('div').css('border','1px solid green')
    })
    // Bouton 3 :
    $('button:nth-of-type(3)').click(function(){
        $('div').css('border','1px solid black')
    })
    //Bouton 4:
    $('button:nth-of-type(4)').click(function(){
        $('div').hide()
    })
    //bouton 5:
    $('button:nth-of-type(5)').click(function(){
        $('div').show()
    })

   
## Exercice 5
Construisez une page html avec un carré et un champ de saisie de texte dans un formulaire.
Lorsque l'on appuie sur une touche de direction le carré se déplace de 10 px dans la bonne direction.  
BONUS : Quand le bloc atteint un bord de la page, il doit réaparaître de l'autre côté.

