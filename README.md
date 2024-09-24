<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/c/cb/Ec_Council_Logo.png">
<img src="https://dfir.blog/content/images/2019/01/autopsy-margin.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Analyze File System of Linux Image using Autopsy</h1>

This lab was purchased through EC- Council. Copyright © 2021 by EC-Council.

This tutorial outlines the analysis of file system using Autopsy. 
Performing file system analysis allows an investigator to determine the following information:

•	File system type 

•	Metadata information

•	Content information

<h2>Environments and Technologies Used</h2>

- Active Directory Domain Services
- Autopsy Forensic Tool

<h2>Task</h2>

- Task 1. Create New Case and Add Data Source
- Task 2. Analyze Linux File System.
- Task 3. Validate the integrity of files using MD5 Hash.
- Task 4. Analyze Images/Videos, Timeline using editor menu.
- Task 5. Generate HTML Report.

<h2>Configuration Steps</h2>

Task 1. Create New Case and Add Data Source

Step 1. Click on AD Domain Controller to select the AD Domain Controller machine. Click Ctrl+Alt+Delete.

![image](https://github.com/user-attachments/assets/8891b189-470b-4266-8d28-fff1bf08b0fe)

Step 2. By default, the CCT\Administrator user profile is selected. Click admin@123 to paste the password in the Password field and press Enter to login.

![image](https://github.com/user-attachments/assets/f2168531-14f2-4243-8150-b96db8fa6613)

Step 3. In this lab, we will be using Autopsy tool to examine the filesystem of a Linux image.

Step 4. Double-click the Autopsy 4.14.0 shortcut icon on the Desktop

![image](https://github.com/user-attachments/assets/48a072ca-4f25-4eea-8431-a633b5e19f72)

Step 5. Autopsy Welcome window will appear along with Autopsy main window in the background. In the Welcome window, click New Case.

![image](https://github.com/user-attachments/assets/c6d2256a-094b-494c-81f3-bdb1541086f9)

Step 6. A New Case Information window opens asking you to input the base Case Name and the Base Directory. The base directory is the location where the case data will get stored. The case name may be entered according to your identification purpose. In this lab, we are assigning the case name as Linux_Analysis.

![image](https://github.com/user-attachments/assets/f1775606-9a80-4273-a423-4f664f371c6c)

Step 7. Before specifying the base directory, we will be creating a folder on the Desktop with the name Image File Analysis and setting the path of the Base directory to this folder.

![image](https://github.com/user-attachments/assets/4abb6b8f-ff48-4a5b-932a-d33a5f7cbb67)

Step 8. Upon setting the base directory, click Next.

![image](https://github.com/user-attachments/assets/d78bc42d-cdad-4cf8-a174-b7b9b3b5373d)

Step 9. The New Case Information window now shows the Optional Information section where you can specify details such as name of the examiner and case number. For this lab, let us enter the name of the examiner as Jonathan and the case number as 1001-125. You may also fill out the other optional fields. Click Finish after entering the details for optional fields.

![image](https://github.com/user-attachments/assets/52e02b10-e836-4ad3-9738-435b22966c6f)
 
Step 10. The Add Data Source window now appears displaying the section Select Type of Data Source To Add. Here, you need to select the type of data source to be provided as an input. In this lab, we will be analyzing a disk image; therefore, select the option Disk Image or VM File and click Next.

![image](https://github.com/user-attachments/assets/e8a632b7-1a1d-4c3f-9913-824a2868d52c)

Step 11. The Add Data Source window now displays the section Select Data Source where you need to select the location of the Image that you are going to examine. Click Browse.

![image](https://github.com/user-attachments/assets/889b7260-2dd7-4962-8a22-dad6c725643c)

Step 12. An Open window will appear where you need to specify the forensic image. Navigate to Z:\CCT Module 20 Computer Forensics\Evidence, select Linux_Evidence_001.img and click Open.

![image](https://github.com/user-attachments/assets/2ce58727-27b9-48c5-bf14-4581c3e7f013)

Step 13. Once you set the path of the image file, click Next.

![image](https://github.com/user-attachments/assets/af47f767-ab02-44b2-a904-59ac46cacb57)

Step 14. The Add Data Source window now displays the Configure Ingest Modules section, which contains lists of options that are checked. Select the options according to your requirement and click Next.

![image](https://github.com/user-attachments/assets/2aa2e896-30d5-4022-8831-2dc059cb266e)

Step 15. The Add Data Source window now displays the Add Data Source section, stating that the data source is successfully added. Click Finish.

Autopsy will take some time to completely analyze the evidence file. You can proceed to the next steps of this lab even when the analysis of the evidence file is still in progress.

![image](https://github.com/user-attachments/assets/0c3c2ff7-908e-48c9-856d-17abd85a00ff)

Step 16. The application now displays the result in the Autopsy main window. Expand the Data Sources node in the left pane and click on the image file i.e., Linux_Evidence_001.img. This will show the contents of the image file, as shown in the following screenshot:

![image](https://github.com/user-attachments/assets/21f8eee7-b459-462a-bc0c-eb84962db6ba)

Step 17. Expand the image file Linux_Evidence_001.img to see its contents. Upon expanding the image, Autopsy displays the filesystem of the Linux image as shown in the following screenshot:

![image](https://github.com/user-attachments/assets/b6b1136f-72db-49fa-984f-29eab45f5118)

Step 18. You may examine all the required files stored in the image as a part of filesystem analysis. In this lab, we are going to view the passwd file that is stored in \etc location. Therefore, select the etc folder from the left pane.

Step 19. Upon selecting the folder, all the files and folders present in etc are displayed in the right pane of the window.

![image](https://github.com/user-attachments/assets/bd7d3188-5660-4891-a674-629422718b4f)

Step 20. Scroll down the window and select the passwd file.

![image](https://github.com/user-attachments/assets/43772a72-8863-401c-8933-54f55cf40be2)

Step 21. Click the Text tab.

Step 22. Autopsy displays all the text (user account information) present in the passwd file, under the Strings tab, as shown in the following screenshot:

![image](https://github.com/user-attachments/assets/29bf6c2f-bec5-461c-b277-f4c8eb95f734)

Step 23. Similarly, click on the File Metadata, Hex, and Annotations tabs to view other details pertaining to the selected file.

![image](https://github.com/user-attachments/assets/232e2f7c-adc8-42f0-8dd3-6a4cdbcf50bd)

File Metadata

![image](https://github.com/user-attachments/assets/e11fc8eb-d772-467d-806e-61a3897b2fe0)

Hex

![image](https://github.com/user-attachments/assets/c083fe0f-c0c1-4e10-86e6-2df18a69660b)

Annotations

Step 24. This way, you can analyze all the other files and folders of your choice to get detailed information on them.

Step 25. Apart from examining the file system, you can also calculate the hashes of the files that you examine, which helps in validating the integrity of the evidence. In this lab, we will be calculating the MD5 hash of a file named SeatPlan.xls, which is located within /home/roger/Documents.

![image](https://github.com/user-attachments/assets/bc260064-db2c-487d-b55b-edb101ac0359)

Step 26. To view the MD5 hash value of this file, expand home --> roger --> Documents in the left pane. The SeatPlan.xls file appears in the right pane of the Autopsy window. Click the file.

![image](https://github.com/user-attachments/assets/f17c3e62-2650-461c-a472-0a7ba5755c3c)

Step 27. The File Metadata section displays the selected folder/file’s metadata information such as the file’s created, modified, and accessed times followed by its MD5 hash value.

![image](https://github.com/user-attachments/assets/ced3d345-091c-4238-b18f-ebb6576581f3)

Step 28. Click on File Metadata and scroll down the section to find the MD5 value for the SeatPlan.xls file.

![image](https://github.com/user-attachments/assets/71696dc3-c652-48d1-9207-c257b46a30a1)

Step 29. Click on Results tab and you can view information such as Source File Path, Artifact ID and it shows that the file is password protected.

![image](https://github.com/user-attachments/assets/ba41dae1-1f08-4551-9c5c-b101b4f05a29)

Step 30. Now, click on Images/Videos option from the toolbar to view all the images and videos present in the evidence file.

![image](https://github.com/user-attachments/assets/68c99a11-3f76-4878-aa9a-17cbbf5722be)

Step 31. Image/Video Gallery - Editor window appears, maximize the window. It displays only image and video files.

![image](https://github.com/user-attachments/assets/40363c41-c34b-4b35-b0ac-4ed1ade10600)

Step 32. Close the Image/Video Gallery - Editor window to navigate back to Autopsy main window.

Step 33. Now, click on Timeline from the menu bar.

![image](https://github.com/user-attachments/assets/568cfc4f-c9eb-4466-88af-c07cd0741628)

Step 34. The Timeline-Editor window opens, displaying a bar graph. Click on GMT/UTC radio button from the left pane under Display Times In section. 

![image](https://github.com/user-attachments/assets/c2db2862-a1a4-47e0-acdd-c0876e72c45c)

Step 35. Now, right click on the longest bar (here 2016) and select Zoom into Time Range option from the context menu.

![image](https://github.com/user-attachments/assets/70bf4531-7d0f-4ed4-bc7e-cb8c70ca4b81)

Step 36. In the next window, right click on a bar (here June) and click on Zoom into Time Range option from the context menu.

![image](https://github.com/user-attachments/assets/1fdeb8ab-6381-438d-a9de-753ec541dfda)

Step 37. In the next window, right click on a date (here 09) and click on Zoom into Time Range option from the context menu. In the following window, right click on a time interval (here 09) and select Zoom into Time Range option from the context menu.

![image](https://github.com/user-attachments/assets/0b0e587b-f41a-4f77-857b-f79d17b7e24d)

![image](https://github.com/user-attachments/assets/b0df571d-1b51-4319-956d-e8d674374634)

Step 38. Click on List from the View Mode options.

![image](https://github.com/user-attachments/assets/593add15-d4a1-4432-9ae8-ff2c930ad1ab)

Step 39. The events will be listed in a time sequence; you can select any entry and click on Hex, Text, or File Metadata at the bottom of the window to view the Hex, Text or Metadata of the event.

![image](https://github.com/user-attachments/assets/fa1ed1b1-6a44-4ab3-b3e4-9d08164da0ea)

Step 40. Now close the Timeline-Editor window to navigate back to Autopsy main window. In the Autopsy window click on the Generate Report option from the menu bar.

![image](https://github.com/user-attachments/assets/87e6f72c-f6df-42ea-a703-6986788a473f)

Step 41. A Generate Report window appears. By default, HTML Report will be selected under Report Modules, enter Header and Footer details in the respective fields and click on Next.

Here we are giving Linux_Analysis as the Header and CCT-Report as the footer.

![image](https://github.com/user-attachments/assets/07f3507f-f445-47d0-be15-0c1f4af7c35b)

Step 42. In the Configure Report window, select All Results radio button and click on Finish.

![image](https://github.com/user-attachments/assets/47cafb7e-a27a-4d2c-af54-364434e2a3d5)

Step 43. A Report Generation Progress… windows appears showing the progress, wait for it to complete.

![image](https://github.com/user-attachments/assets/04407a89-3263-416e-8fe3-5c9a28d83f66)

Step 44. After completion of report generation click on Close to close the window.

![image](https://github.com/user-attachments/assets/ad2abeef-1bae-4029-88d4-c374b3d21b3f)

Step 45. Minimize the Autopsy window, navigate to the Image File Analysis folder located on the Desktop. After this, navigate to Linux_Analysis/Reports/Linux_Analysis HTML Report 08-27-2021-05-54-00 and double-click on report.

The name of the HTML Report folder might vary in your lab environment.

![image](https://github.com/user-attachments/assets/adaf443f-48e9-4df9-ada3-f7210e77d91e)

Step 46. When the report opens in the default browser, you can explore the report by selecting the options under the Report Navigation menu.

![image](https://github.com/user-attachments/assets/31d0fda9-9287-45f3-94af-b5cb57c91515)

![image](https://github.com/user-attachments/assets/f13afc43-0177-4724-9fa0-165a39c54525)

![image](https://github.com/user-attachments/assets/bf039574-c294-4544-a04b-2d3a86a83fe7)

![image](https://github.com/user-attachments/assets/d91b75c0-837a-4a50-be18-611e707f6b0a)

Step 47. This concludes the demonstration showing how to analyze file system of a Linux image using Autopsy tool.

Step 48. Close all open windows.
