Easy execution of [atl](http://www.eclipse.org/atl/) model transformations.
```
register( UMLPackage.eINSTANCE.eResource() );

Transformation<EMFModel, EMFModel> uml2ecore = new  Transformations.Builder()
.asm("uml2ecore.asm")
.in(get(UMLPackage.eNS_URI), "IN", "uml")
.out(ecore(), "OUT", "ecore")
.buildOneInOneOut();

EMFModel out = transform(inject(resource("model.uml"), get(UMLPackage.eNS_URI)), uml2ecore);
```

eclipse update site http://svn.codespot.com/a/eclipselabs.org/atl-commons/snapshots/

source code is on [github](https://github.com/ghillairet)