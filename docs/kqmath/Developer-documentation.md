# Developer documentation
*

## Release Policy

1. lag release branch (release/x.x) branching from develop (development, devel depending on project)
   Merk: to tall i branch-navnet for ikke å blande med tags.  Det tredje tallet (patch-nummer) brukes kun til hotfixes.
2. oppdater version.php
2. build JS files (hvis nødvendig)
2. oppdater CHANGELOG.md (Keep a Changelog)
2. release branch -> pull request til master
2. pull request må være ok -> grønt lys
    1. Hvis ikke, må man se gjennom loggen og gjøre en vurdering
    1. Trykk på merge pull request
6. Lag github release med versjon nummer vX.Y.Z
    1. Velg «Releases» fra kode-siden og fyll inn skjema
    1. Merk, alltid tre tall i versjonsnummeret, major.minor.patch
    1. Første release fra en ny release-gren er vX.Y.0
    1. Github lager automatisk tag fra release navnet.
    1. Husk å velg master branchen som target branch
6. release branch -> pull request til develop
6. Trykk på merge pull request
6. Updating a registered plugin (after you have created the tag and branch)
    1. Click on Developer Zone in the plugin's page, and click Add a new version.
    1. On the top right, you will see a form where you can select the tag you have created. When you have selected your tag (vx.y.z), click the Release button, and the zip file will automatically be retrieved from github and attached .
    1. Be sure to click Show more and select the supported Moodle and PHP versions.
    1.  noen små steg, sett in tracker url… main branch,

    1. Sjekk at. Readme er ok, trenger av og till litt fiksing.

The branching and tagging norms follows the GitFlow model. Ved hotfixes hopper man over steget med ny gren, og bygger heller videre på tidligere release-gren.
