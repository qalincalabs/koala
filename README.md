# [Koala](https://docs.google.com/spreadsheets/d/1tjktUMx26vcGmk0r5E-Esn6EIexSXl6BBZ2JEsAOu_k) (beta)

Analyse and simulate local food systems logistics to stimulate and support collaboration between local actors. ([check the model](model.graphql))

> **FR** Outil digital d'analyse et de simulation des activités logistiques à destination des acteurs des circuits courts (alimentaires et de proximité) en vue d’identifier les opportunités de collaboration et leurs mises en œuvre.

Koala is an online spreadsheet ([showcase](https://docs.google.com/spreadsheets/d/1911VmU56UkR1faytEkeM-cnDhJSywItnhr506cJV-C0)) where you define all the logistic model data (local actors, their product flows, vehicles, drivers and tours). The spreadsheet is like a logistic workspace.

*(To implement)* Once all the logistic data is defined, you can start making scenarios (select flows,…) and simulate them. The tool (backend script) will for instance solve the multi-vehicle routing problems.

*(To implement)* Scenario can be compared (based on cost, time, …). You can see what’s the difference if all the producers would use their car in turn to move all the products or would only use it to move their own produce.

## Model

The model can be explored through [Graphql voyager](https://apis.guru/graphql-voyager/). Copy paste the [raw model](https://raw.githubusercontent.com/qalincalabs/koala/main/model.graphql) into `Graphql voyager > Change schema > SDL`

## Multilingual

You can change the language through the [language property in *Settings*](https://docs.google.com/spreadsheets/d/1tjktUMx26vcGmk0r5E-Esn6EIexSXl6BBZ2JEsAOu_k/edit#gid=1719152079&range=B1) (try *fr* or *en*, *nl* and *de* were not checked). Translation for other languages or improvements can be done in [*I18n*](https://docs.google.com/spreadsheets/d/1tjktUMx26vcGmk0r5E-Esn6EIexSXl6BBZ2JEsAOu_k/edit#gid=268125426)

## Technical documentation *(in design)*

The code behind the spreadsheet (backend code) can be found through the menu `Tools > Script` editor

## Integrations *(in planning)*

The backend code can directly use google workspace services and communicate with Open batra and Open Food Network through API (http requests). 

* [Le Chemin Des Mûres](https://www.lechemindesmures.fr/). Koala solves the multi-vehicle routing problem through their API
* Open batra. Koala can use this service to get the full GS1 product description from a GTIN (example : https://www.batra.link/01/00230229184407/00230229184407.json)
* [Open Food Network](https://www.openfoodnetwork.org/). Koala can use this service to load actors, hubs, product flows (from orders) into the workspace
Google workspace. Koala will use Google Calendar, Google Maps services (to show tour routes, availability calendars, …) for planning and simulation.

