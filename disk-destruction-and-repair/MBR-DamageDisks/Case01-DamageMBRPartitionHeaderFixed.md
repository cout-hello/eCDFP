### How to Fix MBR Partition Header Using 010 Editor

Here are the steps to fix the MBR Partition Header using the 010 Editor:

1. *Open the Corrupt Disk in 010 Editor:*
   - Drag the corrupt disk into the 010 Editor.

2. *Apply Templates:*
   - From the top menu, select "Template" and then choose "Drive".
   - Select "Drive" again to display the template results.

3. *Analyze the Results:*
   - From "Template Results", select "Drive" and then "MBR".
   - Go to the fourth partition "Partition (4)".

4. *Modify Values:*
   - Change the "Boot Indicator" value to "0 (No Boot)".
   - Modify the "Starting Head" to an insignificant value.
   - The third option is also insignificant and can be ignored.
   - In the "System ID" field, select "Partition_SystemId_NTFS_HPFS_ExFAT (7)".
   - Set the "Ending Head" value to zero.

5. *Find Relative Sectors:*
   - From the top menu, select "Search" and then choose "Find" using "ASCII".
   - Type "NTFS" and click "Find All".
   - Click on the first "NTFS" that appears and note the number on the left (e.g., 128).
   - Enter this number in the "Relative Sector" field.

6. *Calculate Total Sectors:*
   - From the same "NTFS" results, go to the third entry, which is a backup of the first.
   - Note the number (e.g., 41087).
   - Use a calculator to subtract the first number (128) from the third number (41087). The result will be (40959).
   - Enter this result in the "Total Sectors" field.

7. *Adjust Subsequent Partitions:*
   - Follow the same steps for the subsequent partitions, with differences in identifying relative and total sectors.
   - Select the fifth "NTFS" for the relative sector number (e.g., 41088).
   - For total sectors, select the seventh "NTFS" (e.g., 61567) and subtract the fifth number (41088).
   - The result (20479) is entered in the "Total Sectors" field.

8. *Save Changes:*
   - Save the modifications made to the disk.

9. *Verify the Fix:*
   - Run the disk in the FTK Imager program to ensure everything is correct.

---

By following these steps, you can successfully fix the MBR Partition Header and ensure the disk operates correctly.
