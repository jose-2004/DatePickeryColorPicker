##  codigo

Componentes principales:
Controles de la interfaz:

Label: Etiquetas para los textos descriptivos.
DatePicker: Selector de fecha.
ColorPicker: Selector de color.
Button: Botón para confirmar la selección.
Label: Etiqueta para mostrar el resultado.

Diseño y disposición:

VBox: Un layout vertical con un espaciado de 10 píxeles entre los componentes, centrado y con un padding de 10 píxeles.




        

    package Main;
    import javafx.application.Application;
    import javafx.geometry.Insets;
    import javafx.geometry.Pos;
    import javafx.scene.Scene;
    import javafx.scene.control.Button;
    import javafx.scene.control.ColorPicker;
    import javafx.scene.control.DatePicker;
    import javafx.scene.control.Label;
    import javafx.scene.layout.VBox;
    import javafx.stage.Stage;
    
    public class InterfzaGUI extends Application {



    @Override
    public void start(Stage primaryStage) {
        // Crear controles
        Label fechaLabel = new Label("Selecciona una fecha:");
        DatePicker fechaPicker = new DatePicker();
        Label colorLabel = new Label("Selecciona un color:");
        ColorPicker colorPicker = new ColorPicker();
        Button botonConfirmar = new Button("Confirmar");
        Label resultadoLabel = new Label("Resultado:");

        // Crear layout vertical (VBox)
        VBox root = new VBox(10);
        root.setPadding(new Insets(10));
        root.setAlignment(Pos.CENTER);

        // Agregar controles al layout
        root.getChildren().addAll(fechaLabel, fechaPicker, colorLabel, colorPicker, botonConfirmar, resultadoLabel);

        // Acción al presionar el botón
        botonConfirmar.setOnAction(e -> {
            String fechaSeleccionada = fechaPicker.getValue().toString();
            String colorSeleccionado = colorPicker.getValue().toString();
            resultadoLabel.setText("Fecha seleccionada: " + fechaSeleccionada + "\nColor seleccionado: " + colorSeleccionado);
            System.out.println("Fecha seleccionada: " + fechaSeleccionada + ", Color seleccionado: " + colorSeleccionado);
        });

        // Crear escena y mostrarla
        Scene scene = new Scene(root, 300, 250);
        primaryStage.setTitle("Fecha y Color GUI");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args); 
    }
  }


![image](https://github.com/jose-2004/DatePickeryColorPicker/assets/80079088/25f702bf-3579-4c6c-b9f7-bd447ac3e09f)

![image](https://github.com/jose-2004/DatePickeryColorPicker/assets/80079088/49ddcf4a-b2d8-4bc9-b9e9-a9725b2bb688)

![image](https://github.com/jose-2004/DatePickeryColorPicker/assets/80079088/79d47064-4d36-4358-b4ad-d15dad7a47b5)


