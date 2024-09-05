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
