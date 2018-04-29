# osx-bootstrap-npm

The role to install some global node.js packages with npm.

## Requirements

You should have ```homebrew``` installed.

## Role Variables

* ```node_brew_package``` -- the name of homebrew packaage with node.js and npm, ```node@8``` is the default value.
* ```npm_global_packages``` -- the list of packages you want to install, default value is an empty list.

## Dependencies

No.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```playbook.yml```:
```yml
---
- host: localhost
  vars_files:
    - vars/npm.yml
  roles:
    - 0x4e3.osx-bootstrap-npm
```

```vars/npm.yml```
```yml
---
npm_global_packages:
  - name: gulp
    version: 3.9.1
  - name: ember-cli
    version: 2.11.1
  - name: react-native-cli
    version: 2.0.1
  - name: phantomjs
    version: 2.1.7
```

## License

BSD
