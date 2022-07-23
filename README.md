# LASoT : A visual studio code plugin to visualize Descartes and Reneri reports 

LASoT plugin incorporates in Visual Studio Code informations generated by [Descartes](https://github.com/STAMP-project/pitest-descartes) engine and [Reneri](https://github.com/STAMP-project/descartes-reneri) to help students to refine the assertions of their tests. [Read more](https://github.com/STAMP-project/pitest-descartes#mutation-testing) about extreme mutation testing.

## Features

LASoT extension for VS Code provides : 

<details open>
<summary>Explorer</summary><br>

The extension provides a treeView to execute Maven Descartes, Reneri and LASoT commands.  <br>

![LASoT Explorer](img/lasot-explorer.PNG)

- <strong>Descartes:mutationCoverage</strong> goal execute generates extreme transformations to the code and provides reports.  Those reports are accessibles in the target/pit-reports folder. 
- <strong>Reneri:observeMethods</strong> goal observes the execution of the original method and each transformed variant of the method. 
- <strong>Reneri:observeTests</strong> goal observes the execution of each test case for the original methods and the transformed variants. 
- <strong>Reneri:hints</strong> goal Generates improvement hints according to the results obtained with the execution of the two previous goals. 
- <strong>LASoT:highlightsHints</strong> goal decorates code based on the reporting of the previous goals. 

To be able to display the decorations, each goals must be executed in the presented order (Descartes->Reneri->LASoT) 

</details>

<details closed>
<summary>Wizard</summary><br>

A Wizard to guide users to follow the steps correctly. To launch the wizard enter "LASoT Wizard" in the command palette (Ctrl+Shift+P).<br>

![Wizard](img/lasot-wizard.PNG)

</details>

<details closed>
<summary>Status bar</summary><br>

Quick indication of survived mutations in the status bar.<br>

![Status bar](img/lasot-statusbar.PNG)

You can click on it to show more informations about the undected mutations.

![Dialog](img/lasot-statusbar-dialog.PNG)


</details>
<details closed>
<summary>Decorations</summary><br>

The extension decorates the signature of the methods in your classes and in the code of your tests suites.  It incorporates informations showed in an overlay when you hover the decoration.<br> 

The overlay of <strong>signaled methods</strong> indicates the classification of this method (uncovered, partially-tested or pseudo-tested).  It also gives more informations about the undetected mutations and killed mutations.

![Methods Decorations](img/lasot-decorations-methods.PNG)

The overlay of <strong>signaled tests</strong> indicates the value and type of the decorated part for the original version of the program and the undetected mutation.

![Methods Decorations](img/lasot-decorations-tests.PNG)

</details>

## Requirements

The Java project on which this extension is applicated must includes Descartes and Reneri extensions.  Reneri extension needs an installation of [Maven](https://github.com/apache/maven) to properly operates. 

