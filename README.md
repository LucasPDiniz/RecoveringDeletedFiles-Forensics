# Recovering Deleted Files - Forensics :detective:

* Did you know that even deleting a file from a device, it remains accessible? Did you know that we can recover this data? With this concept of file recovery, we can also mention the problems of leakage and unauthorized data access when a **HD/SSD/PENDRIVE** is discarded incorrectly. The people who may be looking for this data are called **Dumpster Diving**.

> [!IMPORTANT]
The **Dumpster diving** is looking for treasure in someone else's trash. In the world of information technology (IT), dumpster diving is a technique used to retrieve information that could be used to carry out an attack or gain access to a computer network from disposed items.

<p align="center">
  <img width="400" height="400" src="./img/1.png">
</p>

* In this document we will use one of the forensic techniques used to recover and analyze system files. For the study, we will **Create** and **Remove** files on drive 'E:', below.

<p align="center">
  <img width="400" height="180" src="./img/5.png">
</p>

# What will we use :question:

* In our study we will use 2 programs, one to create an image of the target disk and the other to analyze this data.

    * **FTK Imager** - FTK Imager is a free Digital Forensics tool. It has features especially for acquiring evidence derived from storage units. In this case, we will use the Windows version, available at [FTK Imager](https://www.exterro.com/ftk-product-downloads/ftk-imager-version-4-7-1)

    <p align="center">
        <img width="110" height="120" src="./img/2.png">
    </p>

    * **Autopsy** - Autopsy is a tools for cyber first responders to intrusions, crime scenes, and war zones. It will be used in conjunction with FTK to analyze the generated data. We can find it for Windows here [Autopsy](https://www.autopsy.com/download/)

    <p align="center">
        <img width="400" height="100" src="./img/3.png">
    </p>
    
# Disk Image :cd:

* A disk image file is a file that contains a bit-by-bit copy of a disk drive. A bit-by-bit copy saves all the data in a disk image file, including the metadata, in a single file. For this step, we will use **FTK Imager**.

1. Go to 'File -> Create Disk Image'.

<p align="center">
    <img width="500" height="200" src="./img/4.png">
</p>

2. Set 'Logical Driver'.
 <p align="center">
    <img width="500" height="300" src="./img/6.png">
</p>

3. Set your Drive.
 <p align="center">
    <img width="500" height="300" src="./img/7.png">
</p>

4. choose type 'E01', this type will be imported into autopsy.
 <p align="center">
    <img width="500" height="300" src="./img/8.png">
</p>

5. In Item Information, This field is used to record evidence, this information is not necessary. In the destination, we place where the record will be saved.
 <p align="center">
    <img width="600" height="300" src="./img/9.png">
</p>

6. Working... When finished, the **forense.E01** file will be generated.
 <p align="center">
    <img width="420" height="300" src="./img/10.png">
</p>

# Recovering the Files :floppy_disk:

* After generating the evidence files using FTK Imager, we can analyze and recover the deleted files using Autopsy. Let's go.

1. Let's generate a 'new case'.
 <p align="center">
    <img width="420" height="260" src="./img/11.png">
</p>

2. We inform the name of the case and the destination of the logs.
 <p align="center">
    <img width="500" height="300" src="./img/12.png">
</p>

3. Here we will select a disk image.
 <p align="center">
    <img width="700" height="300" src="./img/13.png">
</p>

4. We choose our E01 file.
 <p align="center">
    <img width="600" height="200" src="./img/14.png">
</p>

5. Here we can view all our deleted files.
 <p align="center">
    <img width="800" height="450" src="./img/15.png">
</p>

6. Extracting the files, we were able to access all the files again.
 <p align="center">
    <img width="800" height="250" src="./img/16.png">
</p>

# Final evidence :mag:

* Below we were able to open all the files that were deleted on our disk E:.

 <p align="center">
    <img width="800" height="400" src="./img/17.png">
</p>

* This happens because when deleting a file, only a reference to the Block/Sector where the file is located is removed, however, as long as the space is not overwritten, the file remains on the disk and can be recovered.

 <p align="center">
    <img width="500" height="300" src="./img/18.png">
</p>

* In the simple example above, we can see that when deleting a file, the block reference is removed, however, the file remains on the disk.

---

<p align="center">
  <img width="300" height="300" src="https://media1.giphy.com/media/m9eG1qVjvN56H0MXt8/giphy.webp?cid=790b7611dy3p1ek802ps94kbmmehkjotvafqlwoqkxq0qvey&ep=v1_gifs_search&rid=giphy.webp&ct=g">
</p>
<p align="center">
Hope this helps. To the next
</p>