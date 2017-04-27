# gsavalik
KeM avaliku GeoServeri kaardikihtide definitsioonid ja SLD kujundused.

## Taust
Siin repositooriumis töötame KeM (Keskkonnaministeeriumi)
[avalikul kaardiserveril](http://gsavalik.envir.ee/geoserver) avaldatud
kaardikihtide definitsioonide ja SLD kujundusfailide kallal. Kaardikihid on
üldjuhul saadaval nii OGC WMS (
[WebMapService](https://en.wikipedia.org/wiki/Web_Map_Service)) kui ka WFS (
[WebFeatureService](https://en.wikipedia.org/wiki/Web_Feature_Service))
teenuste kaudu, v.a juhul kui konkreetse andmehulga omanik pole seadusest vms
kohustustest tulenevalt otsustanud teisiti.

KeM avaliku kaardiserverina on kasutusel [GeoServer](http://geoserver.org) ja
siin repos töötame `GEOSERVER_DATA_DIR` kallal. Repositooriumi struktuur on
üles seatud selliselt, et oleks võimalik kõik kaustad [src](src) alt
paigaldada kaardiserveri masinas `GEOSERVER_DATA_DIR` määratud rajale.

WMS kaardikihtide kujundused on loodud SLD (
[StyledLayerDescriptor](https://en.wikipedia.org/wiki/Styled_Layer_Descriptor))
formaadis. Kihtidele määratud vaikekujundused on üldjuhul ilma mõõtkavaliste
piiranguteta (s.t objekte näidatakse kõikidel mõõtkavadel). Samas võib
kaardikihi kuvamise mõõtkava vahemikele olla määratud erinevad kujundused.
Näiteks väikestel mõõtkavadel kuvatakse objektid punktidena, suurematel
mõõtkavadel aga objektid ise.

SLDde nimetused järgivad kuju `väljundi_tähis.kujundatav_objekt.stiil`,
nt `kkr.jaakreostus.default` tähistab Keskkonnaregistri jääkreostusobjektide
vaikekujundust. Kujunduste nimedes kasutame ainult väiketähti, väldime
täpitähti ja erisümboleid. Kirjavahemärkidest kasutame ainult punkti.

Hea ülevaate SLD kujundustest koos näidetega annab
[MassGIS wiki](https://wiki.state.ma.us/display/massgis/Home) kodulehe
[SLD lehekülg](https://wiki.state.ma.us/display/massgis/GeoServer+-+WMS+-+Styled+Layer+Descriptor+-+SLD).
Samuti pakub hea taustainfo
[GeoServeri dokumentatsioon](http://docs.geoserver.org/latest/en/user/styling/sld/index.html).

## Löö kaasa
Soovi korral võid ka ise kaasa lüüa KeM avaliku kaardiserveri teenuste
arendamises. Ava [õssu](https://github.com/e-gov/kem-gsavalik/issues) (_issue_)
või osale arutelus - WMS kujunduste muudatused, hoopistükkis uued kujundused või
grupikihid, teenuste / kaardikihtide metaanded jms.

Uute kaardikihtide lisamise soovide osas võiks üle käia teemad
[okestonia/opendata-issue-tracker](https://github.com/okestonia/opendata-issue-tracker/issues)
lehel ning oma soovid ja vajadused sinna kommunikeerida. Seeläbi saame teabe
huvipakkuvatest andmetest ühes koos hoida.

Kui soovid ise teha täiendusi/muudatusi/parandusi, siis võid avada tõmbepalve
(_pull request_). Märgi sel juhul end kindlasti ka kaastööliste nimekirja
[contributors.md](contributors.md). Sellegipoolest oleks hea kui arutame enne
üheskoos vajalikud muudatused läbi. Me jätame endale õiguse muudatuste
mestimisest loobuda.

## Litsents
See töö on avaldatud CC BY 4.0 litsentsi alusel (vt [LICENSE](LICENSE) fail).
Kujundusfailide taaskasutamisel palume viidata
`CC BY 4.0: KEMIT ja kaastöölised` võimalusel http-lingiga
[contributors.md](contributors.md) lehele.