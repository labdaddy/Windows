### Delete Partitions on a Windows USB Drive

You can do this by using diskpart on Windows:

- Open an elevated command prompt.
- Run `diskpart`
- `list disk`
- Note the disk number that corresponds to your USB drive (it should be obvious going by size)
- select disk `X` where `X` is the number from step 4
- `list partition` - There should be two, numbered 0 and 1, each about 7 GB
- `select partition 0`
- `delete partition`
- `select partition 1`
- `delete partition`
- `create partition primary`
- `exit`
- Exit Command Prompt (type exit or just close the window)
- In Windows, go to Computer(or This PC for Windows 10) and try to open the disk. It will ask you to format it.
- Format it with the default settings and give it a name if you want.
- It should now a single, unified partitioned drive.
