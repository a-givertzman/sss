# Этоапы расчета прочности и остойчивости  по 3d модели
Имеем:
- 3d модель корпуса (может состоять из разных частей)
- 3d модель помещений (цистерн, грузовой трюм, прочее если надо);
- распределение массы судна порожнем по длине;
- массу судна порожнем и положение центра тяжести;
- грузовой план с объемом воды в цистернах и прочих грузов.

Порядок расчета остойчивости:
1. Определяем общую массу, из общей массы получаем объемное водоизмещение
2. Определяем общий момент судна порожнем и несмещаемых грузов (кроме цистерн)
3. Путем перебора дифферента, осадки и крена совмещаем центр масс (он изменяется с учетом наклонения жидкости в цистернах)  с центром объема корпуса, получаем осадку, крен и дифферент.
> [!NOTE]
> Иногда для повышения производительности, если это требуется, прибегают к следующим приемам:
> 1. Цистерны делят на 2 группы: запасов и балласта. Цистерны запаса учитывают через таблицы, балласт как описано выше. 
> 2. Все учитывают через таблицы как мы делаем сейчас.
4. Для полученного осадки, дифферента и крена  считаем ДСО (фактичеки тот же расчет что и выше с дополнительным моментом по ширине)
5. Дальше то что мы делаем сейчас без изменений.
  
Порядок расчета прочности:
1. Определяем эпюру масс судна порожнем и несмещаемых грузов (кроме цистерн);
2. Путем перебора дифферента, осадки (крен не учитывается) совмещаем центр масс (он и эпюра масс изменяется с учетом наклонения жидкости в цистернах) эпюры масс с центром объема корпуса, получаем осадку и дифферент.
3.  для полученного дифферента и осадки считаем перерезывающие силы и изгибающие моменты.