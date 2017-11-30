# VIPER
iOS VIPER Architecture

* `View`——This is a UIViewController which has outlets to views and handles user interaction. View has 2 protocols.
    View Input——implemented in View Layer and called from Presenter Layer.<br>
    `*`Display info on View. e.g. showProgress()<br>
    View Output——implemented in Presenter Layer and called fromw View Layer.<br>
    `*`Notify presenter about User actions. e.g. addNewItem()<br>
* `Presenter`——This is a class which communicates with View,Router and Interactor using next protocols.
    View Ouput——look at View section.<br>
    Interactor Output——implemented in Presenter Layer and called from Interactor Layer.<br>
    `*`Notify presenter about updates. e.g.dataDidLoad()<br>
    View Input——look at View section.
    Interactor Input——implemented in Interactor Layer and called from Presenter Layer.<br>
    `*`Asks for updates. e.g.loadItems()<br>
    Router Input——implemented in Router Layer and call from Presenter Layer.<br>
    `*`Navigate between modules. e.g.showDetailModule()<br>
* `Interactor`——Thhis is a class that communicates with Presenter and Entities.<br>
    Interactor have 2 protocols.<br>
    Interactor Input——look at Presenter section.<br>
    Interactor Output——look at Presenter section.<br>
* `Entity`——These any data representation like CoreData Entity,Realm Object,etc.<br>
* `Configurator`——One more thing.<br>
    VIPER has lots of components that we need inject between.<br>
    Configurator injects layers between them.<br>
