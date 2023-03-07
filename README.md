# Qualification-work(NUFT)
 Розробка системи автоматизованого керування машини розливу в ПЕТ пляшку

# Зміст

- [Опис об’єкта автоматизації](https://github.com/danya-andrienko/Qualification-work-NUFT-/blob/main/README.md#опис-об'єкта-автоматизації)
    - Технологічний опис об’єкта автоматизації
    - Розробка завдання на систему автоматизації
- [Система автоматизації]()
   - Обґрунтування вибору технічних засобів для вимірювання, виконавчих механізмів (ВМ) та регулюючих органів (РО)
   - Схема автоматизації
   - Специфікація засобів автоматизації. 3. Проєктне компонування промислового логічного контролера (ПЛК) та схеми підключення.
- [Проєктне компонування промислового логічного контролера (ПЛК) та схеми підключення]()
    - Проєктне компонування промислового логічного контролера (ПЛК).
    - Загальна схема підключення датчиків та ВМ до ПЛК.
    - Розширені схеми підключення для окремого контуру.
- [Креслення встановлення технічного засобу]()
- [Опис спеціального програмного забезпечення для промислового логічного контролера (алгоритм та програма для ПЛК)]()
- [Розробка людино-машинного інтерфейсу оператора технолога]()
    - Переліки вхідних та вихідних сигналів та даних SCADA/HMI.
    - Відеокадри дисплейних мнемосхем оператора.
- [Комп’ютерне моделювання системи автоматичного регулювання]()
    - Постановка задачі дослідження.
    - Вибір об'єкта керування та його математичної моделі.
    - Моделювання САР.
    - Опрацювання результатів моделювання та формулювання висновків.

## Опис об’єкта автоматизації

**Технологічний опис об’єкта автоматизації**

Автоматизація є невід'ємною частиною технологічних процесів та розвитку людства загалом. Основною метою будь-якої автоматизації є збільшення продуктивності виробництва та зменшення впливу людського фактору на протікання технологічного процесу.
Будь-яке виробництво складається з багатьох пов'язаних між собою ділянок, на кожній з яких виконується певний процес, який є частиною виробництва продукту. Значний вклад в розвиток автоматизації дало покращення контрольно вимірювальних пристроїв та методів зв'язку.
З розвитком інформаційних технологій системи автоматизації почали ставати інтелектуальними а з появою нейромереж та штучного інтелекту системи ставатимуть ще більш автоматизовані а вплив людини на протікання процесу буде мінімізований і помилка буде можлива лише на етапі розробки та впровадження системи.
Велику роль для покращення якості продукції що виготовляється та покращення технологічних процесів загалом відіграє збір та аналіз інформації про проходження процесів та контролю якості вихідної продукції. Для забезпечення ефективного збору інформації використовують бази даних різних типів, також для того, щоб покращувати існуючі системи автоматизації ведеться збір інформації виникнення аварійних ситуацій різного характеру, як і з боку операторів на лініях так і з боку недосконалості системи та виходу обладнання з ладу.
Також великий вклад на покращення протікання технологічних процесів та збільшення об'ємів виробництв в цілому лежить на покращенні контрольно-вимірювальної техніки та засобів управління. Наразі всі показники відображаються на моніторі ПК або на панелі оператора, що спрощує контроль протікання процесу та дає можливість передбачення виникнення аварійних ситуацій.
Система розливу в ПЕТ пляшку сама по собі являється одним з етапів виробництва рідин різного характеру та призначення. Розлив рідин є одним із завершальних етапів у виробництві рідких продуктів таких як вода, молоко, пиво та інші. З появою автоматизованих ліній стало можливим суттєве збільшення об'ємів виробництва, але з ускладненням систем щоб покращити виробництво ускладнюються і системи контролю цих систем і це слід враховувати при розробці та впровадженні у виробництво.

Технологічна схема – це графічне зображення технологічного процесу, у вигляді послідовних виробничих функцій. На технологічних схемах зображуються основні елементи системи, технологічні ділянки та об'єкти. Технологічна схема машини розливу у ПЕТ пляшку із зазначенням розташування датчиків та ВМ показано на рисунку 2.1.

На технологічних схемах можуть зображати, як всю систему від початку і до її завершення так і схему окремих технологічних ділянок з метою більш детального розгляду конкретного процесу на виробництві

![Image alt](https://github.com/danya-andrienko/Qualification-work-NUFT-/blob/main/image/Технологічна_схема.png)

Рис.2.1 – Технологічна схема машини розливу у ПЕТ пляшку

На даній схемі зображено модель машини розливу, напрямок сировини та розташування датчиків та виконавчих механізмів. Технологічна схема дає інформацію про розташування елементів системи та інформацію про послідовність і напрямок протікання технологічного процесу.
Машина розливу у ПЕТ пляшку показана на рисунку 2.1 працює за наступним алгоритмом.
Спочатку перевіряється наявність рідини у ємності з якої ведеться розлив. Якщо рівень у ємності вище мінімального машина почне роботу в іншому випадку відкриється клапан наповнення ємності і вона заповниться до максимального рівня, контроль за витратою рідини ведеться за допомогою витратоміра.
На вхід машини по конвеєру подається порожні пляшки, при досягненні безпосередню місця розливу спрацьовує безконтактний датчик наявності, при першому спрацюванні датчика подається сигнал на пневмоциліндр, який блокує вихід з апарату таким чином пляшки розташовуються у потрібній точці.
Коли датчик на вході апарату спрацює тричі конвеєр зупиниться і за допомогою пневмоцилінтра в середину пляшок зануряться трубки наповнення. Коли спрацює датчик кінцевого положення трубок відкриються клапани наповнення пляшок і по досягненню необхідного рівня спрацюють сигналізатори рівня, що встановлені навпроти пляшок і клапани закриються.
Після закриття клапанів йде сигнал на пневмоциліндр з метою виймання трубок з пляшок і коли датчик кінцевого положення дасть відповідний сигнал пневмоциліндр, що блокує вихід отримає сигнал на зворотню дію та розблокує вихід з установки також запуститься конвеєр та наповнені пляшки підуть на вихід з машини де ведеться додатковий контроль за наявністю пляшки з метою запобігання виникнення закупорювання у випадку якщо одна або кілька пляшок перекинуться.
На будь-якому етапі проходження процесу ведеться контроль за виникненням аварійних ситуацій для цього на клапанах та пневмоциліндрах встановлюються датчики кінцевого положення а на конвеєрі встановлено датчик обертів для контролю швидкості обертання транспортеру.

**Розробка завдання на систему автоматизації**

Таб.1 – технологічні вимоги до системи

| № | Машина, агрегат, установка | Параметр, місцевідборусигналу | Припус-тимезначенняпараметра | Видавтомати-зації | Характерконтролючиуправління | Засобиуправліннятаконтролю, реалізаціїуправляючоїдії | Додатковіумови |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Конвеєр подачі ПЕТ пляшки | Швидкість подачі | 6000 од/год | Регулювання | Стабілізація | Вплив на двигун конвеєра |
| Контроль наявності пляшки | Є/нема | Контроль | Відображення реєстрація | АРМ оператораЩит управління | На виході з апарату |
| 2 | Блок розливу | Контроль наявності пляшки | Є/нема | Контроль | Відображення реєстрація | АРМ оператораЩит управління | На вході апарату |
| Вирівнювання пляшок | Вімк/Вимк | Управління | Стан | Вплив на пневмоциліндр |
| Контроль трубок наповнення | Опущені/Підняті | Управління | Стан | Вплив на пневмоциліндр |
| Наповнення пляшок | Вімк/Вимк | Управління | Стан | Вплив на клапани наповнення |
| 2 | Блок розливу | Контрольрівня в пляшках | 100% | Контроль | Відображення Реєстрація | АРМ оператораЩитуправління
| 3 | Ємність з продуктом | Рівень в ємності | 10-100% | Контроль | Відображенння Реєстрація | АРМ оператораЩитуправління | За допомогою сигналізаторів рівня |
| Подача продукту в ємність | 10-100% | Регулування | Стабілізація | Вплив на клапан набору в ємність |
 | Витрата продукту | 4000 л/год. | Контроль | Відобра-женняРеєстрація | АРМ оператораЩит управлінняАРМ оператора |


# Система автоматизації

# Проєктне компонування промислового логічного контролера (ПЛК) та схеми підключення
# Креслення встановлення технічного засобу
# Опис спеціального програмного забезпечення для промислового логічного контролера (алгоритм та програма для ПЛК)
# Розробка людино-машинного інтерфейсу оператора технолога
# Комп’ютерне моделювання системи автоматичного регулювання

