## Custom (Advanced) Installation Using GParted

The Custom (Advanced) setup menu allows launching GParted. GParted is an open-source graphical partitioning tool.

**Actions
- Create custom partitions on the system disc.
- Perform data rescue on a hard drive.

1. Select **Modify Partitions.

2. Create a partition table in Device -> Create Partition Table. The GParted supports these partition table types: 

    - aix
    - amiga
    - bsd
    - dvh
    - gpt
    - mac
    - msdos
    - pc98
    - sun
    - atari
    - loop

3. Choose a partition table and click Apply. Most Linux systems will use the GPT partition table.

4. Select the document icon in the upper left corner to open the Create New Partition table.

5. The Create New Partition menu allows users to:

	- Specify the partition size and free space preceding the partition. 
	- Alignment to MiB or Cylinder. 
	- Creating the partition as the Primary, Logical, or Extended partition.
	- Naming the partition and specifying a partition label.
	- Choosing a file system for the partition.

> Tip: Go to View -> File System Support. to view file format information. This window describes the various formats, supported actions, restrictions, and software required to use the format. 

6. Use these two methods to make changes to an existing partition: 

    - Resize the partition by clicking the >| icon in the upper left, or right click the partition and choose Resize/Move.
    - Change the format of the partition by right clicking the partition and selecting Format To.

7. Apply drive configurations in Edit -> Apply All Operations.

### Data Rescue with GParted

GPart must be installed for this feature. Install GPart by launching a terminal and typing `sudo apt-get install gparted`.

1. Choose the Custom (Advanced) installation option.
2. Go to Device -> Attempt Data Rescue.
3. Confirm the scan.