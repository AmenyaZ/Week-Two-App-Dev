## What is Flutter?
It is a "tool" that allows you to build native cross-platform (iOS, Android) apps with one programming language and codebase.

## What is Dart?
It is a programming language which is focussed on building frontend user interfaces though it is not limited on mobile apps only. 

It is developed by Google

It is object oriented and strongly typed and its syntax is like a mixture of JavaScript, Java, C#


## Flutter Architecture
In flutter, everything is a widget including the whole page. So the entire app is built as a widget tree.

In flutter there are no drag & drop and there is no visual editor so we only code

There is one codebase and in you can have as many different dart files withing one project.

You can also choose to embrace the platform differences i.e

    child:  Theme.of(context).platform == TargetPaltform.iOS
        ? CupertinoButton(...) //Apple look & feel   
        : RaisedButton(...) // Material (Google) look & feel

By default flutter uses Material Design which is created and heavily used by Google.

Material Design is highly customizable and works on iOS devices too and it is built into Flutter but you can also find Apple-Styled (Cupertino) widgets

    N/B: Before we start bulding our app, I would recommend you start with hello-world branch as it has the starting point, then move to adding-stateful branch then finally the main branch.

    To switch between the branches, you need to use git checkout <branch name> or when in github there is a dropdown with the different branches.

## Building Our App (branch: hello-world)
Stateless widgets are immutable, meaning that their properties can't change—all values are final.

Stateful widgets maintain state that might change during the lifetime of the widget. Implementing a stateful widget requires at least two classes: 1) a StatefulWidget that creates an instance of a State class. The StatefulWidget object is, itself, immutable and can be thrown away and regenerated, but the State object persists over the lifetime of the widget.

### Adding a Stateful Widget (branch: adding-stateful)

In this step, you'll add a stateful widget, RandomWords, which creates its State class, _RandomWordsState. You'll then use RandomWords as a child inside the existing MyApp stateless widget.

### Create an infinite scrolling ListView (branch: main)
In this step, you'll expand _RandomWordsState to generate and display a list of word pairings. As the user scrolls, the list (displayed in a ListView widget) grows infinitely. The builder factory constructor in ListView allows you to lazily build a list view on demand.
