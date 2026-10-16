# Pracownia Tortów

Przeglądarkowy projektant tortów dla cukierników. Warstwy, pokrycie i dekoracje są widoczne w obracanym podglądzie 3D. Projekty oraz ich miniatury zapisują się lokalnie w przeglądarce.

## Uruchomienie

Otwórz `index.html` w przeglądarce. Można też uruchomić lokalny serwer:

```powershell
python -m http.server 8000
```

Następnie otwórz `http://localhost:8000`. Projekt nie wymaga instalacji zależności ani procesu budowania.

## Edycja

- Wybierz liczbę biszkoptów przy tworzeniu projektu.
- Dodawaj warstwy z zakładek, zmieniaj ich nazwy, kolory i grubość.
- Ustaw pokrycie i dekoracje. W trybie ręcznym przeciągaj ponumerowane punkty na podglądzie albo użyj suwaków w panelu po prawej.
- Zapisuj torty w bibliotece, eksportuj PNG, PDF lub plik projektu JSON.

Zapis odbywa się w `localStorage` tej przeglądarki. Wyczyszczenie danych strony usunie lokalną bibliotekę, dlatego ważne projekty warto eksportować jako JSON.

## Rendering

Aktualny podgląd używa wbudowanego WebGL i ma tryb przekroju. Przy dalszym rozwoju jakości obrazu warto przejść na Three.js: `MeshPhysicalMaterial` dla masy i polewy, cienie z `WebGLRenderer` oraz model warstw z geometrią przygotowaną pod przekrój. Taka migracja pozwoli dopracować światło i materiały bez utrzymywania własnego shadera dla każdego składnika.
