Degree of interdependence between software modules
* Interdependency among modules
* Interaction coupling through message passing
* Law of Demeter/ AKA Message Chains Code smell. Messages should be sent only by an object (methods should only be invoked on objects):
  * to itself
  * to objects contained in attributes of itself or a superclass
  * to an object that is passed as a parameter to the method
  * to an object that is created by the method
  * to an object that is stored in a global variable
  * Or - You can only play with toys
    * you own
    * you build
    * you are given
