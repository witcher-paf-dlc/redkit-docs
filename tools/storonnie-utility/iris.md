# Iris

[Ирис](https://github.com/Witcher-Tools/iris) это утилита, которая предоставляет набор инструментов для упрощения работы с картой в RedKit. Она предназначена для импорта текстурных карт, процедурной генерации вегетации (в разработке), а также нарезке и преобразования названий тайлов в формат, совместимый с RedKit (в разработке).

## Импорт текстур

Утилита позволяет импортировать текстурные карты, созданные в сторонних редакторах, таких как Gaea в RedKit.

Подготовленная карта должна иметь разрешение, соответствующее разрешению вашей карты в RedKit, и быть grayscale имея значения пикселей от 0 до 255.

Далее вы можете определить, какая текстура будет соответствовать определённому диапазону значений пикселей на карте. Для каждого диапазона можно настроить:

* Вертикальную текстуру.
* Горизонтальную текстуру.
* Slope Threshold.
* UV Scale.

**Для импорта текстурной карты:**

* **Шаг 1: Выбор карты текстур** \
  Сначала выберите подготовленную карту текстур. После выбора утилита отобразит предварительный просмотр карты.
*   #### Шаг 2: Выбор папки с тайлами

    Выберите папку с тайлами (terrain\_tiles), которая находится в директории вашего уровня.
*   #### Шаг 3: Добавление текстур

    Чтобы назначить текстуры, нажмите кнопку "Добавить текстур&#x443;**"**. Эта кнопка добавляет новый диапазон на шкалу значений, далее вы можете нажать на этот диапазон что бы отредактировать его текстуру и увидеть как он применится.
*   **Шаг 4: Импорт текстур**

    После завершения настройки кнопка "Импортировать" должна стать активной.&#x20;
* **Шаг 5: Синхронизация LOD в RedKit**\
  После импорта карты и текстур откройте или переоткройте ваш уровень в RedKit и зайдите в **TerrainEditTool**. Перейдите на вкладку **Materials**, затем нажмите кнопку **Texture usage**. Выберите самую верхнюю текстуру и замените её на ту же самую. Это необходимо для синхронизации LODs в файлах тайлов, так как утилита записывает только нулевой LOD. После этого перезагрузите уровень еще раз.

{% hint style="danger" %}
Обратите внимание, что при добавлении диапазона утилита пересортирует все диапазоны, уже находящиеся на шкале. Если требуется добавить ещё однин диапазон с его текстурой, вы можете разделить выбранную текстуру на два с помощью кнопки **"Insert"**.
{% endhint %}

### Шкала текстур

Шкала отображает диапазоны текстур. При выборе диапазона на шкале он подсвечивается зелёным на предварительном просмотре карты, позволяя увидеть область применения. Также при активации определенного диапазона вы можете отредактировать текстуру которая должна примениться в этом диапазоне.&#x20;

Горячие клавиши для управления шкалой:

* **Стрелки вверх/вниз** — переключают выбранную текстуру на шкале.
* **Insert** — разделяет выбранный диапазон, добавляя новую текстуру.
* **Delete** — удаляет выбранную текстуру.
* **Колёсико мыши вверх/вниз** — изменяет диапазон текстуры.
* **Ctrl + колёсико мыши вверх/вниз** — зумирует шкалу для детального.
* **Средняя кнопка мыши + движение** — перемещает шкалу вверх или вниз при зумировании.

### Резервное копирование

Утилита автоматически создает резервную копию ваших тайлов, но только **при первом импорте**, далее эти копии не перезаписываются. Копии сохраняются в папке, которая создается в месте, где находится исполняемый файл приложения.

### Пример импорта

{% embed url="https://youtu.be/ds9GwyU2d08" %}
