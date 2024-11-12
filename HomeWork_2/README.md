# HW2 Изучение геномных перестроек на примере *Arabidopsis thaliana*

## Введение

В данной работе мы сосредоточились на сравнении геномов различных экотипов арабидопсиса, включая референсный геном и несколько исследуемых образцов. Основной целью было проведение анализа синтении и выявление ортологичных генов между этими геномами.

### Важные пояснения:

- `GCA_000211275.1_ASM21127v1_genomic.fna` - это экспериментальная сборка, которая была найдена для анализа, несмотря на ее недостатки. (Называется далее как Study2)
- `GCF_000001735.4_TAIR10.1_genomic.fna` - Референсный геном (иногда обозначается как Ref)
- `GCA_036937505.1_ASM3693750v1_genomic.fna` – геном, выданный по заданию, не используется в анализе синтении из-за отсутствия аннотации в формате .gff на NCBI.
- `GCA_904420315.1_AT9943.Cdm-0.scaffold_genomic.fna` – канадский экотип, выбранный из-за наличия .gff (иногда в работе обозначается как Study)

## Инструменты и методы

- **MUMmer**: numcer и mummerpot – выравнивание двух геномов и дальнейшая визуализация их наложения друг на друга с отображением их различий.
- **Пакет JCVI**: автоматически выполняет задачи по выравниванию и построению синтении, используя такие инструменты, как BLAST, LAST, MCScanX, и MCSynteny, в зависимости от конфигурации и формата данных.

## Результаты и их интерпретация

- **GCA_036937505** с помощью MUMmer выравниваю на референс GCF_000001735 и получаю такую картину:
  - **Анализ**: Основная диагональная линия (пурпурная) указывает на области высокой схожести между последовательностями. Голубые и пурпурные точки вне основной диагонали могут указывать на перестройки, инверсии или дупликации в геномах.

- С помощью JCVI визуализирую попарное сравнение каждого генома:
  - **GCA_904420315 (CDM-0: Study)** сравниваю с **GCF_000001735 (Ref)**. Здесь наблюдается небольшая инверсия.
  - Теперь сравниваю **GCA_000211275 (Study2)** с референсом. Здесь наблюдается большое количество транслокаций.
  - Сравниваю **GCA_000211275 (Study2)** и **GCA_904420315 (CDM-0: Study)**. Наблюдаются транслокации и одна инверсия в середине.

- Также были построены две столбчатых диаграммы, которые показывают соотношение синтенических блоков между исследуемым геномом (CDM-0: Study) и референсным геномом:
  - **Левая диаграмма**:
    - Основная часть генома (93%) соответствует паттерну 1:1, где на один референсный ген приходится один блок.
    - 6% генома не имеют соответствия (0 блоков на референсный ген).
  - **Правая диаграмма**:
    - 97% генома также соответствуют паттерну 1:1, где на один блок исследования приходится один референсный блок.
    - 2% генома не имеют соответствия (0 референсных блоков на блок исследования).

В целом, графики показывают, что большая часть генома в исследуемом и референсном образцах имеет соотношение 1:1, что указывает на высокую степень синтении между ними.

При сравнении **GCA_000211275 (Study2)** и референса (Ref) наблюдаются же результаты похуже, что было ожидаемо, поскольку об этом геноме было предупреждение о его фрагментированности.

Визуализировала макросинтению сразу на трех геномах. Сравнение ASM с референсом показывает достаточно большие отличия, что может быть свидетельством как действительных различий, так и последствием плохой сборки генома, в то же время сравнение CDM и референса показывают некоторое количество небольших инсерций и делеций, что в свою очередь может быть обычным свидетельством хода эволюции.