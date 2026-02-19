# td-ihm

TD2 - HELP

6. Vous pouvez selectionner le dernier element de la liste des dossiers avec la méthode:
   X.getSelectionModel().selectLast(); /* avec X votre ComboBox */

7. Creer un EventListener a toujours la meme structure:
   EventHandler<ActionEvent> nameEvent = new EventHandler<ActionEvent>() {
			@Override
			public void handle(ActionEvent e) {
          /* Mon action */
			}
		};
    X.setOnAction(nameEvent); /* avec X mon objet (ex: ComboBox, Button) */

   Pour savoir quel type d'event on doit mettre (ex: ActionEvent, KeyEvent) voir le pdf ici associé.
   Dans cette Q7. vous avez uniquement besoin de mettre à jour votre majListView avec en argument
   avec le nouveau repertoire qui a été sélectionné.

8.    Vous pouvez choisir de mettre un bouton en "non-clickable" avec:
   X.setDisable(true); (avec X votre bouton)

9. Vous devez créer un nouveau EventListener pour le bouton Cancel et fermer le Stage avec:
    System.exit(0);

10. Vous devez créer un nouveau EventListener sur listViewFile pour que quand un element est selectionné, le bouton Open devient clickable. Chercher le bon type d'évènement dans le pdf associé.
    Vous pouvez utiliser pour ajouter l'Event a la liste:
      listViewFile.setOnMouseClicked(monEvent);

    Ensuite créer un nouveau EventListener pour le bouton Open:
    Pour vérifier si l'element sélectionné est un dossier, créer un objet File avec l'adresse de l'objet de la list selectionné, puis appliquer la fonction isDirectory() sur l'objet File.
    Si c'est bien un dossier mettre à jour ComboBox.

11. Pour vérifier s'il y a eu un double click:
      monEvent.getClickCount() == 2
    Pour déclencher le bouton Open:
      btnOpen.fire();

    
    
