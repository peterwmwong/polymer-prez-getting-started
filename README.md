# Presentation Checklist

- [ ] **Setup**
    > python -m SimpleHTTPServer 8080


- [ ] **Import Polymer**
    > git checkout c8d5f4406fbe2fcfb4c0969036f391e0dc25e900


- [ ] **Setup HTML / Import polymer**
    > git checkout e212e7b12e3bcbdb02634acc4839f460361963d5

  - Added `index.html`
    - `<script src="polymer/polymer.min.js"></script>`


- [ ] **Define a polymer-element (<greeter>)**
    > git checkout 0211fb342c426d2e368cfafb6bc0ec8db3d7ef9e

  - Added `elements/greeter.html`
    - `<polymer-element>`
      - `<template>`
      - `<script>`


- [ ] **Import and use polymer-element (<greeter>)**
    > git checkout 1cc66743b7f074c6fb468ff897f0493d61382d02

  - Modified `index.html`
    - `<link rel="import" href="elements/greeter.html">`
      - `<greeter/>`


- [ ] **Define a model. Render data from the model.**
    > git checkout c692d8700235e0fb27f140bcb3ffc1e1d5db810c

  - Added `person-model.html`
    - @name property

  - Modified `greeter.html`
    - `<link rel="import" href="person-model.html">`
    - `<person-model id="person">`
    - `{{ $.person.name }}`


- [ ] **Bind the model**
    > git checkout 02c5afcdb3ffc1d80846db133eac57ef207bab6e

  - Modified `greeter.html`
    - `<input type='text' value="{{ $.person.name }}">`


- [ ] **Pass data to a polymer-element**
    > git checkout 2150e617252bcb4bd96aa187bea01ae597225755

  - Added `greeter-message.html`
    - `attributes="person"`

  - Modified `greeter.html`
    - `<greeter-message person="{{ $.person }}"></greeter-message>`


- [ ] **Template logic with if**
    > git checkout cc94adeb4d2cf12691ddd4b722eb2a7e6c4ff60b

  - Modified `greeter-message.html`
    - `<template if="{{ person.name == 'Dave' }}">`
