# File_Recovery-using-Autopsy

## Aim
The objective of this guide is to demonstrate how to:  
 - Create a **Virtual Hard Disk (VHD)**.  
 - Add images to the disk, delete them, and recover them using **Autopsy**.  
 - Understand the forensic recovery process for deleted files.  
 - Learn how to remove the virtual disk after completing the experiment.

## Virtual Disk Creation & File Recovery using Autopsy 


## Step 1: 
   Create a Virtual Hard Disk (VHD) 

### **1. Open Disk Management**  
- Press **Windows + X** → Click **Disk Management** 

![image](https://github.com/user-attachments/assets/9aa78e70-a8cf-44a8-a7a0-7eaac0c69372)


### **2. Create a New VHD**  
- Click **Action** (top menu) → **Create VHD**.  

![image](https://github.com/user-attachments/assets/50f24727-d73c-4954-ba52-7bdfdcccd5e7)


### **3. Choose File Location & Size**  
- Click **Browse** and select where to save the VHD file (e.g, `C:\new VHD.vhd`)
- Set the **size** (e.g: `1GB`) 
- Choose **VHD (Fixed Size)** and Click **OK**

![image](https://github.com/user-attachments/assets/6f852ba5-1601-4866-9b9d-7f5df6fd8dd3)


### **4. Initialize the Disk**  
- In **Disk Management**, find your new disk (marked as "Not Initialized").  

![image](https://github.com/user-attachments/assets/2dfffbf5-f649-4034-950a-690e86ba1ac5)


- Right-click the disk → Click **Initialize Disk**.

![image](https://github.com/user-attachments/assets/e9bffd52-078f-4f8b-9518-d688c48ae356)


- Select **MBR (Master Boot Record)**. 

![image](https://github.com/user-attachments/assets/b185457d-c65b-4c68-87cb-8dcc04b1ed51)


### **5. Create & Format the Partition**  
- Right-click the **Unallocated Space** → Click **New Simple Volume**.  

![image](https://github.com/user-attachments/assets/04adde83-cd05-433c-bb21-fdc4a46ff15f)

![image](https://github.com/user-attachments/assets/88522c57-c36e-4ed4-8e32-5f92c4ec41da)

![image](https://github.com/user-attachments/assets/c960e606-2dbe-49af-bde7-b2306c11c402)


- Click **Next** → **Click on Mount in the following empty NTFS folder** → **Browse** → **Assign a drive letter (e.g., `C: or D:`)** → **New folder** → **OK**

![image](https://github.com/user-attachments/assets/8e8a011b-e085-4ceb-b394-a7d9224ddf0b)

![image](https://github.com/user-attachments/assets/ed0bb61d-289a-433d-a37e-c740ef7133b6)


- Click **next** → **Finish**. 

---

## **Step 2: Add & Delete Files for Recovery** 

### **1. Copy Files to the Virtual Disk**  
- Open **File Explorer** → Go to the new drive (`C: or D:`), where the folder created in the previous step
- Create a new folder (`TestFolder`) and copy **images or files** into it.  

### **2. Delete the Files**  
- Select any one or two images → Press **Delete**.  
- Empty the **Recycle Bin** to permanently delete them.  

---

## **Step 3: Recover Deleted Files Using Autopsy**  
### **1. Open Autopsy & Create a New Case** 

- Launch **Autopsy** and **Run as a administrator**  
- Click **Create New Case**.  

![image](https://github.com/user-attachments/assets/5d9bd404-9b49-46f1-a43e-713265b2afed)


- Enter a **Case Name** (e.g., `Autopsy1`).  
- Choose a **Case Folder** location.  
- Click **Next** → Click **Finish**.  

![image](https://github.com/user-attachments/assets/9a87796b-9da2-40de-8e42-28c672314bbf)


### **2. Add the Virtual Disk as an Evidence Source**  
- Click **Add Data Source**  → **Select Host**

![image](https://github.com/user-attachments/assets/a4d14b60-5603-4ef6-950e-f94537b1918b)


- Select **Local Disk** → **next** 

![image](https://github.com/user-attachments/assets/e8d49368-5759-41e0-9511-1a3adcf8095b)


- Select Disk → **Choose the VHD drive (`Drive1`)**

![image](https://github.com/user-attachments/assets/59e57b17-f8be-437e-8659-27a2478c4a5d)

- Click **Next** → Keep default settings → Click **Finish**.  
- Wait for Autopsy to process the disk.  

### **3. Recover Deleted Files**  
- Go to **File Views** (left panel).  

![image](https://github.com/user-attachments/assets/011f5f15-38dc-4964-a44a-6de57331f469)

- Click **Deleted Files** → Find your deleted images.  
- Right-click an image → Click **Extract File**.  

![image](https://github.com/user-attachments/assets/7f94b080-72c7-422c-b0ad-d0477e2cd48a)


- Select a folder to see the recovered files (e.g., `C:\image_recovery`).  

**Your deleted images are now recovered!**  

---

## **Step 4: Delete the Virtual Disk (Optional Cleanup)** 

### **1. Detach the VHD**  
- Open **Disk Management** (`Win + X` → Disk Management).  
- Find the **virtual disk** (`C: or D:`).  
- Right-click the disk (not the partition) → Click **Detach VHD**.  

### **2. Delete the VHD File**  
- Open **File Explorer**.  
- Go to the location where you saved the `.vhd` file (e.g., `C:\new VHD.vhd`).  
- **Delete** the `.vhd` file.  
- Empty the **Recycle Bin**.  

**Your virtual disk is completely removed!**  
 
---
 

## Result :
 This guide covers creating a Virtual Hard Disk (VHD), adding, deleting, and recovering images using Autopsy, and safely deleting the virtual disk after the experiment.
