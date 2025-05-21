WinTimer1
Лабораторная работа 3. Создание элементов управления
Упражнение 1. Создание составного элемента управления
Разработка составного элемента управления
1. Создайте в Visual Studio новое приложение Windows Forms. Назовите его WinTimer1.
![image](https://github.com/user-attachments/assets/519617cd-d10b-49b2-abe3-31c149bc1ead)
2. В меню Project выберите Add User Control и щелкните Add в
диалоговом окне Add New Item. Укажите имя UserControlTimer и
нажмите Добавить. К вашему проекту будет добавлен пустой
пользовательский элемент управления, который откроется в конструкторе.
![image](https://github.com/user-attachments/assets/8d891f92-231e-438b-b14d-d85f3d0e5df0)
![image](https://github.com/user-attachments/assets/02cfba40-85c6-4c79-a01e-5039e958caef)
3. Из Toolbox перетащите Label в пользовательский элемент
управления.
![image](https://github.com/user-attachments/assets/688c9bdf-3c3d-4972-89f0-c047f2d84b2f)
4. Удалите данные из свойства Text ЭУ Label.
 ![image](https://github.com/user-attachments/assets/d7fb9b22-a955-4c8c-a081-6873c9b21dd4)
![image](https://github.com/user-attachments/assets/226db67b-02d9-44c7-8ac6-1b174bc30d5b)
5. Измените размеры пользовательского элемента управления так,
чтобы он был приблизительно равен размеру элемента управления Label.
![image](https://github.com/user-attachments/assets/619cf26a-a195-492a-99d3-85957fe55235)
![image](https://github.com/user-attachments/assets/7ca05a9b-8f71-456d-925f-8ab1a554479e)
6. Из Toolbox перетащите в пользовательский элемент управления
компонент Timer.
![image](https://github.com/user-attachments/assets/9aab1410-bfe1-43d8-9375-477c56ea945f)
7. В окне Properties компонента Timer присвойте свойству Interval
значение 1000 и свойству Enabled значение True.
![image](https://github.com/user-attachments/assets/3d5633fb-585d-452f-9c23-3105c3da7eb0)
8. Дважды щелкните компонент Timer, чтобы открыть в окне кода
обработчик события Timer.Tick по умолчанию и добавьте следующую
строку программы:
label1.Text = DateTime.Now.ToLongTimeString();
![image](https://github.com/user-attachments/assets/ab9c72ca-1b7d-42df-85e0-98293edce1c0)
9. В окне кода добавьте следующее объявление свойства:
public bool TimeEnabled
{
get { return timer1.Enabled; }
set { timer1.Enabled = value; }
}
![image](https://github.com/user-attachments/assets/2725af23-d6bc-4c50-be39-8f81dffca364)
10. В меню File выберите Save All, чтобы сохранить ваше решение.
    ![image](https://github.com/user-attachments/assets/8e70f860-0675-4350-b43b-6b4a6623b758)
11. В меню Build выберите Build Solution
![image](https://github.com/user-attachments/assets/fefa691c-c85f-4638-9ffb-b3cacce2b6fc)
Вывел пустое окно

Применение составного элемента управления
12. Выберите вкладку конструктора Form1. Из Toolbox перетащите
UserControlTimer в форму. К форме добавится экземпляр вашего
пользовательского элемента управления и начнет отсчитывать каждую
секунду. Обратите внимание, что вы можете приостановить это, присвоив
свойству TimeEnabled значение False в окне Properties.
![image](https://github.com/user-attachments/assets/7732bb80-b65f-4868-a51d-704eaebf4454)
В TimeEnabled установил значение False – таймер остановился.

13. Постройте и запустите приложение. Обратите внимание, что
пользовательский элемент управления во время выполнения действует так
же, как в конструкторе.
![image](https://github.com/user-attachments/assets/cc9c6a68-478d-48d5-8575-f920a953ff0f)

Разработка библиотеки классов элементов управления
14. Чтобы разработать библиотеку классов элементов управления,
выполните следующие действия:
a.	Создайте в Visual Studio новое приложение – Библиотека элементов управления Windows.
![image](https://github.com/user-attachments/assets/9c01f9a1-1c91-4a6d-b10a-72c06373c0f1)

b. По умолчанию проект содержит составной элемент
управления.
c. Добавьте элементы управления и код, как описано в
упражнении 1.
d. Выберите элемент управления, который не должен изменяться
при наследовании классов (в данном случае это и label1, и
timer1), и задайте для свойства Modifiers (Модификаторы)
этого элемента управления значение Private.
![image](https://github.com/user-attachments/assets/0edf77ea-dfcf-4e4c-8420-e03639bd9dc4)
![image](https://github.com/user-attachments/assets/56744cad-2862-4ea2-abad-3aa4621cf662)

e. Создайте библиотеку DLL, построив проект.
![image](https://github.com/user-attachments/assets/1d718fcc-b0ac-465d-b348-82e991a4a09c)
![image](https://github.com/user-attachments/assets/7833f343-a802-4c98-b830-cde5b0f3cf5b)

Упражнение 2. Создание специализированного элемента управления
Разработка специализированного элемента управления
1. Создайте в Visual Studio новое приложение Windows Forms.
Назовите его WinTimer2.
![image](https://github.com/user-attachments/assets/421ad104-fc28-449a-aa51-646443dc4c77)

2. В меню Project выберите Add New Item. Выберите Custom
Control в диалоговом окне Add New Item и щелкните Add. Укажите имя
UserControlTimer2 и нажмите Add (Добавить). К проекту будет добавлен
новый специализированный элемент управления. Откройте и просмотрите
его код.

![image](https://github.com/user-attachments/assets/6818e861-b3f6-4954-b6e6-7f6f4aaa26c6)
![image](https://github.com/user-attachments/assets/14d80444-8f43-43b8-99da-9d5e4f220896)
![image](https://github.com/user-attachments/assets/20eeb9f2-fe5b-4921-b47d-df372f29d7d6)

3. Перейдите на вкладку конструктор. В конструкторе UserControlTimer2 перетащите компонент Timer из Toolbox на поверхность конструктора.
   ![image](https://github.com/user-attachments/assets/9b79f9f8-63f9-434f-813a-b69a1394f259)
   
4. В окне Properties присвойте свойству Interval компонента Timer
значение 1000 и свойству Enabled значение True.
![image](https://github.com/user-attachments/assets/9f4f5f9a-6d7b-4fc3-befe-e980225ae8aa)

5. Дважды щелкните компонент Timer чтобы открыть окно кода в
обработчике события Timer.Tick по умолчанию и добавьте следующую
строку программы:
this.Refresh();
![image](https://github.com/user-attachments/assets/0293c3a3-9f06-4899-b4bb-ba0e9477f3c6)

6. Переопределите метод OnPaint и укажите код для отображения
прямоугольника, залитого синим цветом, заполняющего весь элемент
управления:
protected override void OnPaint(PaintEventArgs pe)
{
base.OnPaint(pe);
Graphics g = pe.Graphics;
g.FillRectangle(Brushes.Blue, 0, 0, this.Width,
this.Height);
}
![image](https://github.com/user-attachments/assets/1c199d8f-5a5f-4d5d-8f30-962626f86b55)

7. Для отображения времени добавьте следующий код к методу
OnPaint ниже определения прямоугольника:
pe.Graphics.DrawString(DateTime.Now.ToLongTimeString(),
this.Font, new SolidBrush(this.ForeColor), 0, 0);

![image](https://github.com/user-attachments/assets/0cb7fda5-6907-4766-8b75-2d91294217b9)

8. В меню File выберите Save All, чтобы сохранить ваше решение.
Сохранил

9. В меню Build выберите Build Solution.
Выбрал
Применение специализированного элемента управления


10. Выберите вкладку конструктора Forml. Из Toolbox перетащите
UserControlTimer2 в форму. К ней будет добавлен экземпляр вашего
специализированного элемента управления, который начнет отсчитывать
каждую секунду.
![image](https://github.com/user-attachments/assets/89a43742-07c7-46ab-8691-8293eb04c679)

11. Постройте и запустите приложение. Обратите внимание, что
пользовательский элемент управления действует во время выполнения
таким же способом, как в конструкторе.
![image](https://github.com/user-attachments/assets/c13953c4-56d4-4d69-8d56-766e587f918c)

