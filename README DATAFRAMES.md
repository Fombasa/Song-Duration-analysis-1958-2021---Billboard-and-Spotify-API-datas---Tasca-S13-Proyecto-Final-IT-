# Documentacion de Dataframes

A continuacion se describen todos los dataframes generados en las 4 fases del proyecto.

---

## **1. billboard_weekly_ready.csv**

**Fase:** 1
**Filas:** 330087
**Columnas (9):**

* date
* rank
* song
* artist
* last-week
* peak-rank
* weeks-on-board
* year
* song_artist

**Descripcion:**
Dataset Billboard limpio y preparado para integracion con Spotify.

---

## **2. billboard_top100_annual.csv**

**Fase:** 1
Dataset auxiliar (no usado en fases siguientes).
Ranking anual basado en posiciones medias.

---

## **3. spotify_weekly_integrated.csv**

**Fase:** 2
**Filas:** 330073
**Columnas (16):**

* year
* position
* song
* artist_main
* song_and_artist
* date
* track_id
* track_name
* track_popularity
* album_name
* release_date
* duration_ms
* explicit
* artist_id
* artist_name
* spotify_genres

**Descripcion:**
Dataset Billboard enriquecido con metadatos Spotify.

---

## **4. spotify_weekly_errors.csv**

**Fase:** 2
Generalmente vacio; contiene errores de API.

---

## **5. mismatch_artist_para_api.csv**

**Fase:** 3
**Filas:** 49799
**Columnas (7):**

* id
* year
* date
* position
* song
* artist_main
* song_and_artist

**Descripcion:**
Registros descartados por mismatch entre Billboard y Spotify.

---

## **6. spotify_clean_full.csv**

**Fase:** 3
**Filas:** 279424
**Columnas (40):**

* id
* date
* position
* song
* album_name
* artist_main
* primary_macro_genre
* macro_genres_all
* spotify_genres_list
* duration_min
* track_popularity
* track_id
* track_name
* artist_id
* artist_name
* explicit
* spotify_genres
* duration_ms
* release_date
* song_and_artist
* year
* era_tecnologica
* genre_afro_african
* genre_christian_gospel
* genre_classical_orchestral
* genre_country
* genre_electronic_dance
* genre_experimental_alternative
* genre_folk_acoustic
* genre_hiphop
* genre_jazz
* genre_latin_caribbean
* genre_metal
* genre_pop
* genre_punk
* genre_r&b_soul
* genre_reggae_ska
* genre_seasonal_holiday
* genre_vintage_traditional_musical
* genre_rock

**Descripcion:**
Dataset completo para analisis y visualizaciones.

---

## **7. spotify_clean_for_anova.csv**

**Fase:** 3
**Filas:** 279424
**Columnas (8):**

* id
* duration_min
* primary_macro_genre
* era_tecnologica
* track_popularity
* position
* explicit
* year

**Descripcion:**
Dataset reducido preparado para ANOVA y pruebas estadisticas.

---

## Notas finales

* Todos los dataframes se generan de forma secuencial a traves de las 4 fases.
* Los datos mismatch representan ~15% del total y se guardan aparte para trazabilidad.
