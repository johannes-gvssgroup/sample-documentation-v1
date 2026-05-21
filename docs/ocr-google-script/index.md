# ⚙️ Google Apps Script OCR Setup Guide

This guide covers the backend setup required to deploy the OCR processing script across the GVVSS Google Drive environment.

---

## Step 3.1 — Prepare Your Folder Structure
1. Open your Google Drive.
2. Navigate to: **Shared Drives > Customer Feedback > Pennsylvania > GVB**
3. Ensure the following two folders exist:
    * `Raw Images`
    * `OCR Output`
4. **Repeat this process** for all branches (`GVB`, `GVW`, `GVF`, `GVL`, `GVO`, `GVT`).

## Step 3.2 — Create the Master Google Sheet
1. In the `Customer Feedback` drive, create a new Google Sheet.
2. Name it exactly: **`📄 OCR Processor`**
3. *(This sheet will serve as the GUI where users click a button to start the OCR process).*

## Step 3.3 — Open the Script Editor
1. Open your `OCR Processor` sheet.
2. In the top menu, navigate to: **Extensions → Apps Script**.
3. A new tab will open displaying the Script Editor.

## Step 3.4 — Inject the Code
Copy the standard GVVSS OCR Script and paste it into the editor, completely replacing the default `myFunction()` block.

## Step 3.5 — Enable the Drive API
To allow the script to read and write files, you must enable Google's native API:
1. On the left sidebar of the Apps Script editor, click the **(+)** next to **Services**.
2. Scroll down and select **Google Drive API**.
3. Click **Add**.

## Step 3.6 — Replace Folder IDs
The script needs to know exactly where to look for files. You must map the variables in the code to your specific Google Drive folders.

!!! tip "How to find a Folder ID"
    Open the folder in Google Drive and look at the URL. The ID is the long string of characters at the end:
    `https://drive.google.com/drive/folders/`**`xxxxxxxxxxxxxxxxxxxx`**

**Variables to update:**
* Replace `FOLDER_ID_GVB_RawImages`, etc. → with the actual ID of each `Raw Images` folder.
* Replace `OUTPUT_FOLDER_ID_GVB`, etc. → with the actual ID of each `OCR Output` folder.

## Step 3.7 — Create the GUI Trigger (The Button)
1. Go back to your `OCR Processor` Google Sheet.
2. In the top menu, click **Insert → Drawing → New**.
3. Draw a shape and add the text: **"Run OCR"**.
4. Click **Save and Close** to drop the button onto your sheet.
5. Click the button once, then click the **three vertical dots** in the top-right corner of the button.
6. Select **Assign Script**.
7. Type in the exact function name: `runOCR`
8. Click OK. *(Clicking this button will now trigger the script!)*

## Step 3.8 — Verify Output
When the script runs, the converted text from the scanned form images will automatically appear inside the `/OCR Output` folder of the respective branch as a Google Doc.

!!! note "Future Enhancement"
    A secondary script can be deployed later to automatically scrape these individual Google Docs and compile them into a main summary sheet.