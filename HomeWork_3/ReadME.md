# HW3 Инструменты визуализации: Jupiterplot и Circos. Изучение повторов.

## Jupiterplot

На этом графике показаны геномные перестройки между геномами референса и нашего изучаемого генома: `GCA_036937505.1_ASM3693750v1_genomic.fna` (экотип Kar-1). Линии, соединяющие различные сегменты, представляют собой синтенические блоки или области гомологии между геномами. Видны несколько типов геномных перестроек:

- **Инверсии** (показаны перекрещивающимися линиями)
- **Делеции/инсерции**
- **Транслокации**
![image](https://github.com/user-attachments/assets/3a2cc8b4-0b88-4bcd-82df-012b94bde4ca)

В принципе, по большей части сравниваемые геномы очень схожи между собой.

## Визуализация с помощью Circos
![image](https://github.com/user-attachments/assets/a1e16298-ff5a-4c6d-94d3-bd19b0aec59b)


- **Зеленый круг** – GC-состав, **синий** – плотность повторов.
- GC – относительно равномерен по всей длине генома, но в каждой хромосоме наблюдается резкое снижение GC-состава в одном участке. Скорее всего – это центромерные участки.
- Плотность повторов резко возрастает к концам и началам каждой из хромосом. Также повторы прямо коррелируют с проседанием GC-состава, также резко падая в концентрации в этих областях.

## График Кимуры

Проводим визуализацию процентного соотношения повторов к геному и их типы:
![image](https://github.com/user-attachments/assets/14988126-f3f6-40fa-8746-a66f23133fa9)


- **Гистограмма** показывает распределение повторов по уровню замен Кимуры. График имеет пик около значения 5 на оси X, что указывает на преобладание повторов с этим уровнем дивергенции.
- **Круговая диаграмма** отображает долю различных компонентов в геноме:
  - Немаскированный геном (черный сегмент) занимает 82%
  - Неопределенные повторы (серый сегмент) составляют 16.2%
  - Простые повторы (желтый сегмент) занимают оставшиеся 1.8%