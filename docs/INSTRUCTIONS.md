# Don't Repeat Yourself - Component Library
Ontwikkel een website voor een opdrachtgever op basis van een component library.

## Context
Deze leertaak hoort bij sprint 16 Don't Repeat Yourself. Dit is een opdracht die je deels individueel en deels als team uitvoert voor een opdrachtgever.

Bij deze leertaak hoort de deeltaak:

* [Component Building Block](https://github.com/fdnd-task/dont-repeat-yourself-component-building-block)

## Doel van deze opdracht
Je leert hoe je herbruikbare stukken code op een systematische manier ontsluit zodat jij en jouw mede frontenders ze kunnen gebruiken in andere projecten.

## Werkwijze
Bij elke leertaak wordt de development-lifecycle doorlopen. Hierdoor ontwikkel je een standaard aanpak voor frontend praktijkvraagstukken, werk je systematisch aan leertaken, ervaar je de relevantie van het geleerde en verwerf je de kennis, houding en vaardigheden die de beroepspraktijk van je vraagt. De development lifecycle bestaat uit de stappen: Analyseren, Ontwerpen, Bouwen, Integreren en Testen.

De component library (letterlijk: een bibliotheek met componenten) die je gaat maken bestaat uit een serie herbruikbare bouwblokken voor een opdrachtgever in een apart project. Het voordeel van het gebruiken van een component library is dat alle projecten die voor deze opdrachtgever gemaakt worden terug kunnen verwijzen naar dezelfde component library. 

Door op deze manier te werken wordt de *developer experience* (hierna DX) beter omdat: 
1. Uniformiteit wordt afgedwongen
2. Atomic Design wordt omarmd
3. Herhaling niet meer hoeft (DRY!)
4. Bugs oplossen eenvoudiger wordt
5. Samenwerken makkelijker wordt

Het omarmen van deze ontwikkelstrategie vereist wel enig schakelen in de manier waarop je over code denkt. Het wordt abstracter omdat er meer afhankelijkheden en abstracties in je code gaan plaatsvinden. Je gaat denken in termen van NPM packages in plaats van in componenten in één repository. Waarschijnlijk heb je vorige sprints de kracht van componenten in een lokaal project al ontdekt, nu is het tijd om externe componenten in te laden!

### Aanpak

In deze leertaak vind je slechts een partiële instructie, namelijk voor het [opzetten van de structuur](#structuur-opzetten-team) die nodig is om een component library als project in NPM te krijgen. Als dit gelukt is begint eigenlijk de leertaak pas. Je gaat je component library inzetten bij de [doorontwikkeling van projecten](#doorontwikkeling-individueel) (lees user-stories) voor jouw opdrachtgever.

#### Structuur opzetten (team)

Het opzetten van de structuur voor een component library is een beetje een gedoe maar het loont als je dit eenmaal gedaan hebt.

1. Fork deze leertaak, in deze leertaak ga je de implementatie van de component library maken. Met andere woorden, je linkt in deze repository een andere repository welke de component library bevat.
2. Maak een nieuwe repository aan op jouw GitHub omgeving, geef deze een logische naam, bijvoorbeeld: fdnd-components, bij de volgende stappen staat *CLib* als het om deze ‘andere’ repository gaat.
3. *CLib* Initialiseer een nieuw SvelteKit library project!
4. *CLib* Check package.json voor de benodigde scripts. Als alles gelukt is zie je het commando `package` bij het lijstje staan.
5. *CLib* Maak om te testen een nieuw eenvoudig component aan in de /src/lib map, bijvoorbeeld `HelloWorld.svelte`
6. *CLib* Roep het commando `npm run package` aan om in de repository een package klaar te zetten.
7. *CLib* Bekijk de nieuw gegenereerde map `/package`
8. *CLib* Pas in de gegenereerde `package.json` de belangrijke velden aan, zoals `name`, `version`, `description`, enzovoorts.
9. *CLib* Publiceer gegenereerde package (dus niet het hele project!) als *scoped public package* via npm (zie bronnen). Het kan goed zijn dat je eerst een gebruiker en een organisatie moet aanmaken.
10. Check npmjs.com en zoek jouw organisatie/package (supertof!)
11. Initialiseer een SvelteKit skeletten project.
11. Link jouw package als dependancy door `npm install organisatie/package` uit te voeren.
12. Importeer jouw component door `import { HelloWorld } from 'organisatie/package`, zet het ergens neer met `<HelloWorld />` en test of het werkt.
13. Ga verder bij [Doorontwikkeling](#doorontwikkeling-individueel)

##### Bronnen:
- [Don’t Repeat Yourself](http://wiki.c2.com/?DontRepeatYourself)
- [SvelteKit](https://kit.svelte.dev/) voor het opstartscript
- [svelte-package](https://kit.svelte.dev/docs/packaging) voor het verpakken van de componenten uit `/src/lib` in een nieuwe package. N.B.: Je krijgt een melding dat de package `svelte2tsx` geïnstalleerd moet worden, dat kan je doen met `npm install -D svelte2tsx`
- [How to Create Svelte Component Libraries with SvelteKit (iets verouderd!)](https://medium.com/mkdir-awesome/how-to-create-svelte-component-libraries-with-sveltekit-98fd2ff12f0f)
- [npm Docs](https://docs.npmjs.com/)
- [Creating and publishing scoped public packages](https://docs.npmjs.com/creating-and-publishing-scoped-public-packages)
- [How to Publish Your First npm Package](https://bretcameron.medium.com/how-to-publish-your-first-npm-package-b224296fc57b)
- [How to publish packages to npm (the way the industry does things)](https://zellwk.com/blog/publish-to-npm/)

#### Doorontwikkeling (individueel)

Als de structuur staat kan je verder gaan aan de ontwikkeling voor jouw opdrachtgever. Eventueel kan je wat tijd besteden aan het overhevelen van herhaalde stukken code uit je oude projecten maar dat hoeft niet per se, je kunt ook opnieuw beginnen.

1. Kies een user story uit de backlog van het project waar je aan gaat werken. De projecten staan bij [FDND Agency](https://github.com/fdnd-agency).  
2. Kopieer/plak de user story waar jij aan gaat werken naar de Wiki van de geforkte repository, dit ga je ontwerpen en maken
3. Documenteer je proces a.h.v de development life cycle
4. En schrijf een goede readme
5. Ga terug naar 1 tot de sprint voorbij is.

## Criteria


Deze opdracht is done als:

- [ ] je een component library hebt gemaakt.
- [ ] je hebt gewerkt volgens de verschillende fases van de development-lifecycle
- [ ] je hebt je werk gedocumenteerd in de Readme en Wiki (user story, ontwerpbeslissingen, schetsen en code voorbeelden)
- [ ] de website op Github staat en een live url heeft

