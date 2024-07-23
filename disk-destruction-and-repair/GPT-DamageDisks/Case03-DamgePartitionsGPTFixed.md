1. *Open 010 Editor:*
   - Launch the 010 Editor application.
   - Drag and drop the disk that needs repair into the program.

2. *Load Templates:*
   - Once the disk is loaded, go to the top menu and select Templates.
   - Navigate to Drives and select Drive.
   - You should now be able to read the template results. If the results do not appear after selecting Drive, go to the View menu and select Template Results.

3. *Fix the Drive:*
   - Go to the Template Results pane.
   - Select efi.
   - Then go to Partitions.
   - If there is an error in the partition, follow these steps to fix it:

4. *Search and Copy Basic:*
   - Click on Search at the top, then select Find.
   - Change the search type to Unicode, enter Basic, and initiate the search.
   - Four instances of Basic will appear.
   - Copy the entire range from the hexadecimal value of the first Basic entry starting with A2 A0 D0 EB to the last Basic entry, approximately 480 bytes in total.

5. *Insert Basic Values:*
   - Return to the efi section in Template Results.
   - Go to header.
   - Select the range from byte 1024 to byte 15360.
   - Go to Edit at the top, scroll down to Insert/Overwrite, and select Overwrite Bytes (fourth option).
   - Enter the value 0 and click Overwrite. This should turn the selected area into .........
   - Now, go to byte 1024, select the next 480 bytes, and paste the copied Basic values.

6. *Save and Verify:*
   - Save the file.
   - Open the saved file in FTK Imager to verify the repair.

---

These steps should guide you through the process of repairing the partition using 010 Editor.
