Infra Framework For Delphi
=============================

The InfraFramework4Delphi it is an API that provides a base infrastructure for the Delphi application development using a layered architecture. 

It is important to stress that the InfraFramework4Delphi not forces any type of architecture for applications, which may consist of many layers as necessary. However, it is prudent not exaggerate! For those who do not know where to start, I suggest an architecture widely used by market standards in order to facilitate maintenance and to better modularize your project.

Usually, applications are composed of at least three layers, so it is common to separate the logic of presentation, business rules and persistence. The InfraFramework4Delphi provides mechanisms to make this clearer separation. For organizational reasons, it is recommended that no layer is circumvented. In practical terms, the presentation layer accesses the business layer, which, in turn, accesses the persistence.

Its premise is to facilitate the use layering without losing productivity, ie, enables the use of all the power of DBware components. In InfraFramework4Delphi the Persistence layer is represented by Data Modules with their corresponding data access components, the Business layer is represented by a derived class of TDriverController and is responsible for all business rule, and the View layer is represented by Form and components of interaction with the user.

The InfraFramework4Delphi further provides libraries useful auxiliary for developing any Delphi application.


Drivers Adapters
=================

The InfraFramework4Delphi is available for the following data access drivers:

- FireDAC
- IBX
- UniDAC


External Dependencies
=====================

The InfraFramework4Delphi makes use of some external dependencies. Therefore these dependences are included in the project within the "dependencies" folder. If you use the library parser you should add to the Path SQLBuilder4Delphi.

- SQLBuilder4Delphi: [https://github.com/ezequieljuliano/SQLBuilder4Delphi](https://github.com/ezequieljuliano/SQLBuilder4Delphi)


Samples
=========

Within the project there are a few examples of API usage. In addition there are also some unit tests that can aid in the use of InfraFramework4Delphi.


Using InfraFramework4Delphi
==========================

Using this API will is very simple, you simply add the Search Path of your IDE or your project the following directories:

- InfraFramework4Delphi\dependencies\SQLBuilder4Delphi\dependencies\gaSQLParser\src
- InfraFramework4Delphi\dependencies\SQLBuilder4Delphi\src
- InfraFramework4Delphi\src

Then you must add to your project the Persistence Module Data according to Driver Adapter used, so that you can make to your heritage DAO's:

- InfraFwk4D.Driver.FireDAC.Persistence.pas
- InfraFwk4D.Driver.IBX.Persistence.pas
- InfraFwk4D.Driver.UniDAC.Persistence.pas
