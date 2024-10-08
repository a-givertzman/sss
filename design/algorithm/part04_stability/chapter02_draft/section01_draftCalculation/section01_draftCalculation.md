### Расчет параметров посадки судна
Исходя из объемного водоизмещения $\nabla$ по таблицам элементов теоретического чертежа судна на ровный киль определяются:
- отстояние центра величины погруженной части судна при посадке на ровный киль (без крена и дифферента):
  - по длине от миделя $x_с$;
  - по ширине от ДП $y_с$;
  - по высоте от ОП $z_с$;
- отстояние центра тяжести ватерлинии по длине от миделя $x_f$;
- поперечный $r$ и продольный $R$ метацентрические радиусы, м;
- среднюю осадку $d$.
- площадь ватерлинии $S_{wl}$, м<sup>2</sup>;

> [!NOTE] 
> Осадки измеряются в связанной с судном системой координат т.е. расстояние от ватерлинии до основной плоскости судна 

Аппликата продольного метацентра $Z_m$, м, определяется по формуле
> $$Z_m = z_с + R$$

Поправка к продольной метацентрической высоте на влияние свободной поверхности жидкости в цистернах $Δm_H$, м, определяется по формуле
> $$Δm_H = \cfrac{M_{f.syБЦ} + M_{f.syЦЗ}}{\Delta}$$

Продольная метацентрическая высота без учета влияния поправки на влияние свободной поверхности $H_0$, м, определяется по формуле
> $$H_0 = Z_m - z_g$$

Продольная исправленная метацентрическая высота $H$, м, - продольная метацентрическая высота с учетом влияния свободной поверхности жидкостей в цистернах, определяется по формуле
> $$H = H_0 - \Delta m_H$$

Момент дифферентующий на 1 см осадки $MCT$, т∙м/см, - момент, который необходимо приложить к судну для создания дифферента судна $t$ в 1 см, определяется по формуле
> $$MCT = \cfrac{\Delta \cdot H}{100 \cdot LBP}$$

Дифферент судна $t$, м, - разница осадок носом и кормой в ДП, определяется по формуле:
> $$t = \cfrac{\Delta \cdot (xg - xс)}{100 \cdot MCT}$$

|Дифферент судна $\psi$, градус, определяется по формуле:||
> $$\psi = arctg \cfrac{t}{LBP}$$

Осадка на носовом перпендикуляре длины $LBP$ в ДП $d_f$, м, определяется по формуле:
> $$d_f = d + (0.5 - \cfrac{x_f}{LBP}) \cdot t$$

Осадка на кормовом перпендикуляре длины $LBP$ в ДП $d_a$, м, определяется по формуле:
> $$da = d - (0.5 + \cfrac{x_f}{LBP}) \cdot t$$

Осадка на миделе в ДП, м, определяется по формуле
> $$d_{middle} = \cfrac{d_f + d_a}{2}$$

Число тонн на 1 см осадки рассчитывается $TPC$, т, по формуле
> $$TPC = 0.01 \cdot ρ \cdot S_{wl}$$

Осадка $d_{xiДП}$, м, в ДП в точке с координатой $x_i$, м, равна
> $$d_{xiДП} = d + (0,5 - \cfrac{xi+xf}{LBP}) \cdot t$$

Осадка $d_{xi,yi}$, м, точки с координатами $x_i$, $y_i$ , м, равна
> $$d_{xi,yi} = d_{x_iДП} + y_i \cdot tg(\theta)$$

где $\theta$ – угол крена судна.

