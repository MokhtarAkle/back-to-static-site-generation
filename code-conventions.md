# Code conventies · Hallo Strandeiland

## Inhoudsopgave
* Inleiding
* HTML
* CSS
* Javascript

## Inleiding
Om het samenwerken makkelijker te maken, gebruiken we code conventies. Zo komt onze code goed overeen. 

## Tech-stack
Voor dit project maken we gebruik van het framework SvelteKit en het headless cms Hygraph. We kiezen hiervoor omdat onze opdrachtgever deze techstack wilt en omdat wij als studenten zijn begonnen met deze techstack.

## HTML
In HTML schrijven we in semantische html om zo de toegankelijkheid. Zo vermijden het gebruik van `<div>` en weten screenreaders wat ze moeten voorlezen. 

```html
	<article id="customView" class="grid-overview">
        {#if data && data.wishes && data.wishes.length > 0}
            <ul>
                {#each data.wishes as wish}
                    <li>
                        <img src={wish.image.url} alt="Afbeelding van {wish.heading}" />
                        <a href="/contact">
                            <h3>{wish.heading}</h3>
                        </a>
                    </li>
                {/each}
            </ul>
        {:else}
            <p>Geen wensen gevonden.</p>
        {/if}
    </article>
```

Voorbeelden van semantische html zijn: header, aside, main, footer, details, section etc.

### Prettier
Om het inspringen van HTML zo netjes mogelijk maken, gebruiken we de extentie Prettier. Elk teamlid heeft deze extenstie 

## CSS
In CSS hanteren we de meeste conventies. Omdat SvelteKit de mogelijkheid biedt om in de componenten scoped css te stoppen, proberen we zoveel mogelijk de selector aan te spreken. Als het niet anders kan, schrijven we een duidelijke naam. Bijvoorbeeld:

```css
header nav ul li {
    ...
}

#customView {
    ...
}

.grid-overview {
    ...
}
```

### Custom properties
De naam van de repository zegt het al: "Don't Repeat Yourself". Hiermee willen we ons zelf binnen CSS zo min mogelijk herhalen. Daarom gebruiken we custom properties voor onder meer: Animatie, Kleur, Eenheden en eventueel schaduw. De custom properties schrijven we alsvolgt:

**--unit-default**: **waarde**;

## Javascript

In Javascript maken we gebruik van camelCasing. Zo schrijven we de naam aan elkaar en is het eerste woord met een kleine letter en het tweede woord met een Hoofdletter. Omdat we de theorie van Progressive Enhancement willen aanhouden bouwen we zoveel mogelijk functionaliteit in HTML en CSS. 

De volgorde in javascript die we hanteren is: 
* Het importeren en definiëren van objecten d.m.v. variabelen
* Het event aangeven (aanklikken, hoveren)
* Functies aangeven

### ESLint

Om met javascript fouten snel te vinden, gebruiken we ESLint. Deze extentie geeft errors aan en highlight de code waar het misdreigd te gaan. Ook wijst die door naar ESLint's eigen documentatie voor verdere informatie.
