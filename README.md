# InsigniaNet: Deep Learning for Military Ribbon Bar Classification

### Wprowadzenie

FindMyOrder to aplikacja umożliwiająca identyfikację baretek Wojska Polskiego na podstawie zdjęć, wykorzystująca konwolucyjne sieci neuronowe (CNN). Do treningu modelu wykorzystano fotografie baretek pobrane z internetu oraz zdjęcia z mundurów żołnierzy Wojska Polskiego. Aby poprawić jakość predykcji nowych obrazów, zastosowano warstwę dropout (`keras.layers.Dropout`) jako technikę regularyzacji, która zapobiega nadmiernemu dopasowaniu modelu do danych uczących. Aplikacja potrafi rozpoznać nawet przyciemnione lub lekko wyblakłe baretki, osiągając skuteczność predykcji na poziomie około 95%. 

### Działanie aplikacji

Implementacja aplikacji została zrealizowana w środowisku Jupyter Notebook i jest dostępna w Google Colab. Kolejność wykonywania fragmentów kodu ma znaczenie! 

Na początku należy zaimportować z github całą strukturę katalogu „baretki” – co realizuje pierwszy fragment kodu. Obrazy znajdujące się w tej strukturze będą służyć jako dane treningowe dla modelu. Podany fragment kodu można wykonywać wielokrotnie, za każdym razem katalog "baretki" w Colab będzie nadpisywany.

Następnie należy uruchomić drugi fragment kodu, który buduje i trenuje model na podstawie danych wejściowych, jednocześnie weryfikując ich poprawność.

Ostatnim krokiem jest dodanie do folderu „baretki” nowego zdjęcia, które posłuży do identyfikacji. Domyślnie zdjęcie powinno być zapisane jako `test.png`, jednak można to zmienić w zmiennej `img_path`. Kluczowe jest, aby na fotografii znajdowała się tylko jedna baretka – model dokona predykcji i wskaże, z jakim prawdopodobieństwem zaklasyfikował ją do konkretnej klasy.
