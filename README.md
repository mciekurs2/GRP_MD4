# GRP_MD4
Grafikas programmēšanas 4.md

## Izpildes laiks
Darbs tika veidots apmēram 6-8h, varbūt pat ilgāk.

## Problēmas, ar kurām saskāros izpildes laikā
1. Problēmas sagādāja veicot glTF failu saglabāšanu masīvā, jo nācās izmantot `dragArray.push(child);` nevis `dragArray.push(gltf);`.
2. Problēmas arī sagādāja kā tiek pārvietoti objekti. Tie tiek pārvietoti nekontrolējami ātri. Centos izmantot:
```javascript
dragControls.addEventListener('dragstart', function ( event ) { controls.enabled = false;});
dragControls.addEventListener('dragend', function ( event ) { controls.enabled = true;});
```
bet tie tikai strādā priekš `THREE.TrackballControls` un āri nemaina gala rezultātu.

3. Arī palika nesalabots, kā strādā `console.log()` priekš izmēriem, jo tiek tiek printēti līdz ko pele pieskarās objektam, nevis tiek nospiesta.
