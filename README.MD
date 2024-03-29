<h3>Общая информация</h3>
<p>Цель работы - закрепление навыков использования абстрактных классов и интерфейсов.</p>
 <p>Объекты приложения должны описывать сущности стратегической военной мини-игры и их поведение.
 По условию задачи в нашей игре должно быть два типа юнитов: техника и живая сила (солдаты).
 У всех юнитов (и техники, и живой силы) есть две характеристики - максимальная скорость и уровень брони.
 У техники есть дополнительная характеристика - объем горючего.
 У солдат есть дополнительная характеристика - здоровье.
 
 Некоторые, но не все юниты могут стрелять. Юниты, которые могут стрелять обладают дополнительной характеристикой - сила выстрела.
 
 Некоторые, но не все юниты реагируют на то что в них стреляют. Так, у солдата в которого стреляют, уменьшается здоровье, а у техники уменьшается объем горючего. 
 </p>

<h3>Уровень 1</h3>

<p>В пакете com.brunoyam.unit_2.army добавить два пакета: "soldiers" и "machines", и перенести в них соответствующие по смыслу классы</p>
<p>Добавить необходимые абстрактные классы, вынести в них общие для всех юнитов одного типа поля и методы.</p>

<h3>Уровень 2</h3>
<p>В пакете com.brunoyam.unit_2.army добавить интерфейс Shootable с методом getShot с одним параметром типа int.</p>
<p>В методе getShot всех классов, имплементирующих интерфейс shootable, уменьшать значение поля health на величину, переданную в параметре.</p>
<p>Имплементировать его так, чтобы он был реализован в классах 
<ul>
<li>com.brunoyam.unit_2. ... .Medic</li>
<li>com.brunoyam.unit_2. ... .Sniper</li>
<li>com.brunoyam.unit_2. ... .Trooper</li>
<li>com.brunoyam.unit_2. ... .Transport</li>
</ul></p>

<p>В пакете com.brunoyam.unit_2.army добавить интерфейс Shooter с методом shoot с одним параметром типа Shootable.</p>
<p>В методе shoot всех классов, инмлементирующих интерфейс Shooter, вызывать метод getShot переданного объекта передавая ему произвольное значение.</p>
<p>Имплементировать его так, чтобы он был реализован в классах</p>
<ul>
<li>com.brunoyam.unit_2. ... .Sniper</li>
<li>com.brunoyam.unit_2. ... .Trooper</li>
<li>com.brunoyam.unit_2. ... .Tank</li></ul></p>

<p>Написать реализацию методов shoot и getShot так, чтобы приложение иммитировало стрельбу юнитов друг по другу.
То есть, можно было вызвать метод shoot одного объекта, передав ему "цель" (ссылку на объект Shootable) и после выполнения метода
состояние объекта "цели" изменялось (уменьшалось "здоровье", либо "объем горючего")</p>

<h3>Уровень 3</h3>
<p>Добавить метод recalculateField c двумя параметрами - типа Shooter[] и Shootable[] в класс Application.</p>
<p>Метод должен иммитировать один ход в игре. Мы считаем что за ход все "стрелки" из массива Shooter[] стреляют по всем "целям" из массива Shootable[]</p>
<p>Создать в методе main два массива, содержащих произвольный набор юнитов. Вызвать метод recalculateField, передав ему эти массива.</p>





