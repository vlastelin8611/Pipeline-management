# Pipeline-management
Pipeline technical condition monitoring and control system in the oil industry (basic, requires polishing)
The program itself automatically creates a database if it does not find the required file in the directory with the code file. Edits are required, in particular, to make the interface of the general program more pleasant, to make interaction with the database more intuitive, to create open ports for each block of the program so that additional modules can be easily integrated, especially when the program SIMULATES receiving data from other modules (for example, the program simulates receiving data from measuring pipeline detectors). The original language of the program is Russian. I hope you like my work, I am waiting for comments. Thank you.
Description in scientific language:
The software is developed based on the Python programming language using libraries for working with data and a graphical user interface. The main modules of the program will be listed in the order of use, they include:

The authentication module allows you to recognize the desired user, so that only competent people appointed by the management can monitor the pipeline readings and regulate its operation. This module provides buttons for inserting a key card, which are due only to experiments, the inaccessibility of the ability to check the system on real equipment. When inserting an incorrect key card, an alarm notification is sent (Fig. 3). An alarm notification in case of checking an incorrect key card. The alarm signal is sent whether this is a real situation, otherwise an alarm notification is displayed, also due to the experiment.

The main interface window is divided into 8 main blocks and 1 experimental. The details of each block will be described below. The main interface window is delimited blocks in the manner of a push-button telephone keyboard for user convenience (3 blocks at the top, 3 blocks in the middle, 2 blocks at the bottom). The experimental block did not get into the main interface window due to its specificity, since the experimental block directly affects the experiment, adjusting those parameters that cannot be adjusted in a real situation on real pipeline equipment.

Each block of the main interface is separated from each other so that the information blocks are close to each other, so that as much information as possible is in the field of view, while the control blocks are at a greater distance, in order to ensure the lowest possible probability of accidental use.

The pipeline cell block shows 4 vertical lines symbolizing 4 pipes going in the same direction. Each line is divided into 10 cells. Cell division is necessary in order to quickly identify possible malfunctions and see the specific location of the problem area. The cells have a gradually lit and fading green glow, which is necessary for visual assessment of the pipeline condition. By emitting visual signals, the human eye will better respond to changes in the colors of the cells, which means more attention will be paid directly to this block.

When a fault is detected, the system will highlight it, indicating a specific cell of the pipeline.

The breakdown is simulated by a pre-prepared function in the experimental block. In this case, it makes sense to completely disable a specific pipeline line in order to avoid leaks at the site of the accident, where an outlet may form. To disable such a line, there is a function in block 5, after which the pipeline line becomes marked in the block for monitoring the state of the pipeline (Fig. 7).

In the same way, the system user can start the pipeline line.

In the block with specific data, there are several scales that the system user can adjust, including in the case of use on real equipment. These scales are as follows:

- temperature inside the pipeline;

- pumping speed;

- pressure inside the pipeline.

There are also scales that display factors beyond the user's control. These scales can be adjusted in the experimental block. These scales are as follows:

- outside temperature;

- pipeline slope angle;

- pressure outside;

- pipeline vibration readings.

According to the scale readings of block 2, the user can track specific data and adjust them for the correct operation of the pipeline.

The operational block displays operational data on the pipeline status, which is necessary if the user needs to manage and share data on the pipeline status, as well as understand what information will be included in the report archive of block 6.

This block displays information about the current user. In a real situation, there should be a separate database of company employees, which is synchronized with the program and regulates the ability to control the system by specific users. In this case, the experiment demonstrated only 1 user.

In this block, the user can control the pipeline, adjusting the temperature inside it, the speed of pumping out oil products, and the pressure. The user also has the ability to turn on and off specific pipeline lines in order to avoid the loss of oil products in case of a possible violation of the integrity of the pipeline. In any cases that do not correspond to the normal operation of the pipeline, a repair team must be called, for which the block has a special function. In this particular case, the repair team can fix leaks, which is displayed in the pipeline cell block, and the team can also restore damaged copies of databases, which is displayed in the block with information on the status of databases.
The database block provides an archive of pipeline condition reports. The block works as follows: data is taken from the block with specific pipeline condition data indicators and helps generate a report in a special block that updates the report at certain intervals, and sends the old report to the archive, which is displayed in the block I am describing. To store this archive, the program creates a database file and loads archived reports into it.

The status block displays the availability and activity status of the databases. The data of the active (currently used) database is automatically copied to backup copies, so that in the event of a breakdown of the active database, the user would use one of the backup copies, eliminating losses in pipeline monitoring performance.

The activity status can be changed by the user in a special block for selecting backup copies, while the availability status of a specific database copy can be changed in the experimental block. In this case, the selected database becomes inactive, has the status "Not available", but this can be fixed by calling a repair team.

The backup block selects database copies, which is necessary in the event of a loss of functionality of the previous active copy.

Experimental functions block.

The purpose of the block: checking the system by simulating various phenomena beyond the user's control, be it natural phenomena, simulating a pipeline failure or one of the database copies. The block is separate, because it should not be in the conditions of real system operation.

Thus, the developed system not only ensures reliable monitoring in real time, but also provides users with tools for effective pipeline management, risk minimization and prompt response to any possible malfunctions.



--------------------------------------------------------------------------------------------------------------------------------------------------------


Система контроля и мониторинга технического состояния трубопроводов в нефтяной промышленности (базовая, требует доработки) Программа сама автоматически создает базу данных, если не находит нужный файл в каталоге с файлом кода. Требуются правки, в частности, сделать интерфейс общей программы более приятным, сделать взаимодействие с базой данных более интуитивным, создать открытые порты для каждого блока программы, чтобы можно было легко интегрировать дополнительные модули, особенно когда программа ИМИТИРУЕТ получение данных от других модулей (например, программа имитирует получение данных от измерительных детекторов трубопровода). Исходный язык программы — русский. Надеюсь, вам понравится моя работа, жду комментариев. Спасибо. Описание на научном языке: Программное обеспечение разработано на основе языка программирования Python с использованием библиотек для работы с данными и графического пользовательского интерфейса. Основные модули программы будут перечислены в порядке использования, в них входят:

Модуль аутентификации позволяет распознавать нужного пользователя, так что контролировать показания трубопровода и регулировать его работу могут только компетентные люди, назначенные руководством. В этом модуле предусмотрены кнопки для вставки ключ-карты, которые обусловлены только экспериментами, недоступностью возможности проверки системы на реальном оборудовании. При вставке неверной ключ-карты отправляется тревожное уведомление (рис. 3). Тревожное уведомление в случае проверки неверной ключ-карты. Тревожное уведомление отправляется, если это реальная ситуация, в противном случае выводится тревожное уведомление, также обусловленное экспериментом.

Главное окно интерфейса разделено на 8 основных блоков и 1 экспериментальный. Подробности каждого блока будут описаны ниже. Главное окно интерфейса разграничено блоками на манер кнопочной телефонной клавиатуры для удобства пользователя (3 блока вверху, 3 блока посередине, 2 блока внизу). Экспериментальный блок не попал в главное окно интерфейса из-за своей специфики, так как экспериментальный блок напрямую влияет на эксперимент, корректируя те параметры, которые невозможно отрегулировать в реальной ситуации на реальном трубопроводном оборудовании.

Каждый блок основного интерфейса отделен друг от друга таким образом, чтобы информационные блоки находились близко друг к другу, чтобы в поле зрения попадало как можно больше информации, а блоки управления — на большем расстоянии, чтобы обеспечить минимально возможную вероятность случайного использования.

Блок ячеек трубопровода показывает 4 вертикальные линии, символизирующие 4 трубы, идущие в одном направлении. Каждая линия разделена на 10 ячеек. Разделение ячеек необходимо для того, чтобы быстро определить возможные неисправности и увидеть конкретное место проблемного участка. Ячейки имеют постепенно загорающееся и затухающее зеленое свечение, что необходимо для визуальной оценки состояния трубопровода. Издавая визуальные сигналы, человеческий глаз будет лучше реагировать на изменение цвета ячеек, а значит, больше внимания будет уделяться непосредственно данному блоку.

При обнаружении неисправности система подсветит ее, указав на конкретную ячейку трубопровода.

Поломка имитируется заранее подготовленной функцией в экспериментальном блоке. В этом случае имеет смысл полностью отключить конкретную линию трубопровода, чтобы избежать утечек в месте аварии, где может образоваться выход. Для отключения такой линии в блоке 5 предусмотрена функция, после чего линия трубопровода становится отмеченной в блоке мониторинга состояния трубопровода (рис. 7).

Точно так же пользователь системы может запустить линию трубопровода.

В блоке с конкретными данными есть несколько шкал, которые пользователь системы может настраивать, в том числе и в случае использования на реальном оборудовании. Это шкалы:

температура внутри трубопровода;

скорость перекачки;

давление внутри трубопровода.

Также есть шкалы, отображающие факторы, не зависящие от пользователя. Эти шкалы можно настраивать в экспериментальном блоке. Это шкалы:

температура снаружи;

угол наклона трубопровода;

давление снаружи;

показания вибрации трубопровода.

По показаниям шкал блока 2 пользователь может отслеживать конкретные данные и настраивать их для корректной работы трубопровода.

Оперативный блок отображает оперативные данные о состоянии трубопровода, что необходимо, если пользователю необходимо управлять и делиться данными о состоянии трубопровода, а также понимать, какая информация будет включена в архив отчетов блока 6.

В этом блоке отображается информация о текущем пользователе. В реальной ситуации должна быть отдельная база данных сотрудников компании, которая синхронизируется с программой и регламентирует возможность управления системой конкретными пользователями. В данном случае эксперимент продемонстрировал только 1 пользователя.
nd off определенных ниток трубопровода, чтобы избежать потери нефтепродуктов в случае возможного нарушения целостности трубопровода. В любых случаях, не соответствующих нормальной эксплуатации трубопровода, необходимо вызывать ремонтную бригаду, для чего в блоке предусмотрена специальная функция. В данном конкретном случае ремонтная бригада может устранить утечки, что отображается в блоке ячеек трубопровода, а также бригада может восстановить поврежденные копии баз данных, что отображается в блоке с информацией о состоянии баз данных. Блок баз данных обеспечивает архив отчетов о состоянии трубопровода. Блок работает следующим образом: данные берутся из блока с определенными показателями данных о состоянии трубопровода и помогают сформировать отчет в специальном блоке, который обновляет отчет с определенной периодичностью, а старый отчет отправляет в архив, который отображается в описываемом мной блоке. Для хранения этого архива программа создает файл базы данных и загружает в него архивные отчеты.

Блок статуса отображает доступность и статус активности баз данных. Данные активной (используемой в данный момент) базы данных автоматически копируются в резервные копии, чтобы в случае выхода из строя активной базы данных пользователь мог воспользоваться одной из резервных копий, исключив потери производительности мониторинга трубопровода.

Статус активности может быть изменен пользователем в специальном блоке выбора резервных копий, а статус доступности конкретной копии базы данных может быть изменен в экспериментальном блоке. В этом случае выбранная база данных становится неактивной, имеет статус «Недоступна», но это можно исправить, вызвав ремонтную бригаду.

Резервный блок выбирает копии базы данных, что необходимо в случае потери работоспособности предыдущей активной копии.

Блок экспериментальных функций.

Назначение блока: проверка системы путем моделирования различных явлений, находящихся вне контроля пользователя, будь то природные явления, имитация аварии трубопровода или одной из копий базы данных. Блок является отдельным, т.к. не должен находиться в условиях реальной работы системы.

Таким образом, разработанная система не только обеспечивает надежный мониторинг в режиме реального времени, но и предоставляет пользователям инструменты для эффективного управления трубопроводом, минимизации рисков и оперативного реагирования на возможные неисправности.
