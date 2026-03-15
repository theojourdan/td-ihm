# td-ihm

TD4 - HELP

3. N'oubliez pas tous les imports nécessaire.

4. (Aide a,b,c)
  1. D'abord constituez dans Model.java, les données que vous allez manipulez dans le     Viewer. Normalement vous manipulerez pour l'instant 2 données. Le choix de l'action à réaliser sur l'AnchorPane (Select/Move, Ellispse, Rectangle, Line) et le choix de la couleur:

  ```
  public enum monChoixAction {
		SelectMove,
		Ellipse,
		Rectangle,
		Line
	}
  private monChoixAction choixActuel = monChoixAction.SelectMove;
  ```
  
  Pour l'object de couleur, pensez à utiliser la classe: 
  ```
  import javafx.scene.paint.Color;
  ```

  Enfin pour chacune de ces deux données créez des setters et getters pour avoir accès et modifier les valeurs de ces données. Puis faites le lien avec le Controller.


  2. Pour chaque element de l'interface: 

    ```
    @FXML
    RadioButton radiobutton_selectmove;
    @FXML
    RadioButton radiobutton_ellipse;
    @FXML
    RadioButton radiobutton_rectangle;
    @FXML
    RadioButton radiobutton_line;
    @FXML
    ColorPicker colorpicker;
    @FXML
    Button button_delete;
    @FXML
    Button button_clone;
    @FXML
    AnchorPane graphicalpane;
    ```
  Mettez les RadioButton dans un ToggleGroup afin de garantir que si un RadioButton est selectionné les autres ne le sont pas (voir https://docs.oracle.com/javase/8/javafx/api/javafx/scene/control/ToggleGroup.html). 
  Creez un eventHandler pour chaque element de l'interface. Laissez les vides pour ceux dont vous n'avez pas encore besoin. Example d'eventHandler:
    ```
    radiobutton_selectmove.setOnMouseClicked(new EventHandler<MouseEvent>() {
			@Override
			public void handle(MouseEvent event) {
				// ICI JE MET L'ACTION QUE JE VEUX
			}
		});
    ```
  Pour ce qui de votre AnchorPane graphicalpane, utilisez setOnMousePressed pour créer un objet du type selectionné quand on clique dans l'AnchorPane.
    ```
    graphicalpane.setOnMousePressed(new EventHandler<MouseEvent>() {
      @Override
			public void handle(MouseEvent event) {
      }
		});
    ```
  
  Pour récupérer les coordonnées de l'endroit où l'on a cliqué: 
  ```
  double mouseXOnClick = event.getX();
  double mouseYOnClick = event.getY();
  ```


