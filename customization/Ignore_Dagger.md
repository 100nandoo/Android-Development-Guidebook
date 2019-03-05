## Ignore Dagger Generated Class

you can prevent these from coming up in the ```Ctr-N``` or ```Cmd-O``` dialog by adding them to the ignored files list in ``File / Settings / Editor / FileTypes`` and adding the appropriate wildcards to the Ignore files and folders.

```*_MembersInjector.java; *_Factory.java;``` will cause most of the generated classes to be ignored

[source](https://stackoverflow.com/questions/44922055/remove-dagger-generated-classes-from-android-studios-global-search)