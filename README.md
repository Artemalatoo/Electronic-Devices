1.I create javafx project so that i could have interface.
By creating Device class i extend it for subclasses(Smartphone, Laptop and Tablet)
so that they will be able to inherite some attributes and methods of Device class,
and type so that each of them could have their own properties. Likewise i created
enum Type so that i could ensure that only valid device types are used and improving readability.
2.Then i opened scene builder where i used vbox and tabpane then in each tabs
Smartphone, Tablet and Laptop i used textfield included it, i opened prompt text
and write name, weight and so on instead of labels. Then i add listview and 
buttoms Add Device and Remove Device. Then in the fx:id i wrote names for @FXML and
and in view(Show Sample Controller) took the code. Then i used buttoms setOnAction
so that i could tap on them, used int selectedIndex = listView.getSelectionModel().getSelectedIndex();
so that i could to obtain the index of the currently selected item in a ListView.
Then i used private void addDevice() {
        Device device = null;

        if (!smartphoneName.getText().isEmpty()) {
            device = new Smartphone(
                    smartphoneName.getText(),
                    Double.parseDouble(smartphonePrice.getText()),
                    Double.parseDouble(smartphoneWeight.getText()),
                    Double.parseDouble(screenSize.getText()),
                    cameraResolution.getText()
            );... so that on the textfield i could get Text and used
if (device != null) {
            listView.getItems().add(device);
        } so that it will display String.format of classes. And after adding 
device the textfields will be cleaned by this code  private void clearFields() {
        smartphoneName.clear();
        smartphoneWeight.clear();
        smartphonePrice.clear();
        screenSize.clear();
        cameraResolution.clear();
