# Phylogenetic-Analysis
Zadaniem projektowym jest przeprowadzenie analizy filogenetycznej sekwencji białka S wirusa SARS-CoV-2. Celem projektu jest zbudowanie prostego drzewa filogenetycznego szczepów wirusa oraz oszacowanie tempa ich ewolucji. Dla uproszczenia zadania analizowane będą wyłącznie sekwencje aminokwasowe białka S (spike) odpowiedzialnego za rozpoznawanie celu na powierzchni komórki hosta. Białko S jest powierzchniową glikoproteiną, która z jednej strony musi rozpoznawać białka gospodarza umożliwiając wejście do wnętrza komórki, a z drugiej musi „ukrywać swoją prawdziwą naturę“ przed komórkami układu odpornościowego. Dlatego spodziewać należy się w tym białku dużej zmienności sekwencji i szybkiej ewolucji.

# Struktura repozytorium
W folderze notebooks znajdują się trzy główne części dokumentacji:
- sequences_filtering.ipynb
- tree_simplification.ipynb
- analysis.ipynb

W pliku sequences_filtering.ipynb znajduje się kod odpowiadający za pobranie sekwencji białkowych oraz odflitrowanie niepełnych lub zduplikowanych sekwencji, a także stworzenie drzewa przewodniego.

W pliku tree_simplification.ipynb załączona jest implementacja algorytmu służącego do przetransformowania drzewa przewodniego, czyli łączenie węzłów o małej liczbie dzieci z ich sąsiadami (braćmi). 

Reszta analizy przeprowadzona jest w analysis.ipynb, a składa się na nią:

- wybór reprezentantów,
- obliczenie wartości uliniowień,
- obliczenie dystansów ewolucyjnych,
- implementacja algorytmu UPGMA,
- sprawdzenie bliskości geograficznych wykrytych sekwencji w klastrach,
- obliczenie tempa mutacji dla reprezentantów.

# Wnioski

- wysokie wyniki uliniowień świadczą o dużym pokrewieństwie sekwencji,
- najwyższy dystans ewolucyjny dla reprezentantów to 8, co świadczy o dość szybkim tempie mutacji,
- różnice tempa mutacji wskazują na to, że niektóre szczepy są dużo bardziej zaraźliwe (nawet 2-3-krotnie)
