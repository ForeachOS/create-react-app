## Vragen foreach-create-react-app

    Hoe zetten we die op binnen een across project, zodat we deze kunnen gebruiken om te compileren naar static resources
        - De te volgen stappen zijn quasi altijd toevoegen van de deps, paths goedzetten binnen across & docker image voorzien. Ik stel voor hier een bootstrapped ax project voor te voorzien, en daar dan een PR op maken met de changes voor FE compilatie in

    Is er een verschil qua setup tussen mmev2 en andere projecten, maw is er een verschil tussen het opzetten voor een bis-project en een primarily react-based project?
        - Geen verschil. React is optioneel, bundling gebeurd volgens volledig dezelfde manier

    Welke wijzigingen zitten er in ten opzicht van de standaard create-react-app
        - Multiple entrypoint support (voor code bundle splitting)
        - Uitbreiding op asset handling in dev mode (EMIT support, standaard CRA worden er geen files ge-emit naar fs in dev mode)
        - emotion babel plugin standaard ondersteunt (voor CSS in JS styling)
        - yarn-workspaces (monorepo) support
        - dev server imitation naar custom BE (adhv browser-sync).
        - jest-bamboo-parser toegevoegd voor results correct te parsen op bamboo
        - stylelint toegevoegd voor linting van css/scss files

    Hoe moeten we omgaan met css/js files, assets...
        - Mij niet zo duidelijk wat hiermee bedoeld wordt?

    Waar staat deze code, wat hebben we nodig om deze te onderhouden, welke tools worden er achterliggend gebruikt
        - https://github.com/ForeachOS/create-react-app
        - webpack/babel/eslint
        - [changesets](https://github.com/atlassian/changeset) voor changelog & publishing naar npm

    Hoe deployen/publishen we wijzigingen
        - master wordt gepublished naar npm adhv een PR dat automatisch geupdate wordt naarmate er zaken gemerged worden naar `master`, versionering en changelog wordt opgebouwd adhv https://github.com/atlassian/changesets , waarbij je gewenste versie per PR definieerd

    Hoe werkt de ‘watch’ environment binnen de frontend setup (deze served de resources op een andere poort), is er een verschil tussen een watch binnen een afzonderlijk frontend project (zoals MMEv2) en een across project (resources worden geserved vanuit de static resources folder)?
        - mmev2 is technisch gezien nog hetzelfde als andere across projecten, assets komen ook nog uit static resources folder
        - frontend watch mode(port `3000`) gaat eigenlijk proxy'en naar een backend java server(bijv port `8099`), en integreert `browser-sync` op de `3000` poort, zodat bij changes aan frontend src code gecompileerd zijn, de browser automatisch refreshed
