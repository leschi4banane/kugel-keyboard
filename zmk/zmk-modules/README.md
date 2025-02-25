# zmk modules info

zmk modules must be contained in github repos  
the module's path must be relative zmk application folder (our case: modules/custom/)

to make the module useable you have to add the module in app/west.yml  
under remotes you have to add a remote with a name and your github link like this:

```yml
- name: <your remote name>
  url-base: <remote without the .git at the end>
```

and under projects you have to add:

```yml
- name: <your module name>
  path: <realtive path like modules/custom/<your module>>
  remote: <your remote name>
```

to test if your module is useable you can use the `west list` command and see if your module pops up.
