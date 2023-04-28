# Developer documentation
*

## Release Policy

1. Create a release branch (release/x.x) branching from *develop* (development, devel depending on project)
    + **Note:** to tall i branch-navnet for ikke å blande med tags.  Det tredje tallet (patch-nummer) brukes kun til hotfixes.
2. Last updates:
    1. Update version.php
    2. Build JS files (if required)
    3. Update CHANGELOG.md (Keep a Changelog)
3. Make pull request to *master* from the release branch 
4. Pull request må være ok -> grønt lys
    1. Hvis ikke, må man se gjennom loggen og gjøre en vurdering
    1. Trykk på merge pull request
5. Make github release with version number vX.Y.Z
    1. Velg «Releases» fra kode-siden og fyll inn skjema
    1. Merk, alltid tre tall i versjonsnummeret, major.minor.patch
    1. Første release fra en ny release-gren er vX.Y.0
    1. Github lager automatisk tag fra release navnet.
    1. Husk å velg master branchen som target branch
6. Make pull request to *develop* from the release branch 
    + Push *merge pull request*
7. Updating a registered plugin (after you have created the tag and branch)
    1. Click on Developer Zone in the plugin's page, and click Add a new version.
    1. On the top right, you will see a form where you can select the tag you have created.
       When you have selected your tag (vx.y.z), click the Release button,
       and the zip file will automatically be retrieved from github and attached .
    1. Be sure to click Show more and select the supported Moodle and PHP versions.
    1. noen små steg, sett in tracker url… main branch,
    1. Sjekk at. Readme er ok, trenger av og till litt fiksing.

The branching and tagging norms follows the GitFlow model. Ved hotfixes hopper man over steget med ny gren, og bygger heller videre på tidligere release-gren.
