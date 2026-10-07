# microsoft-azure-image-Processing

## Experiment Setup

This experiment uses **Microsoft Azure Blob Storage** and **Python** to process images stored in the cloud.

The images are uploaded to an Azure Blob Storage container. A Python program downloads the images, resizes them to **300 × 300 pixels**, converts them to **grayscale**, and uploads the processed images back to Azure.

### Technologies Used

- Microsoft Azure
- Azure Blob Storage
- Python
- Azure Storage Blob SDK
- Pillow (PIL)

---

## Experiment Steps

### Step 1: Create Azure Account

1. Open the [Azure Portal](https://portal.azure.com).
2. Sign in to your Azure account.
3. Open the Azure Portal Dashboard.

---

### Step 2: Create a Storage Account

1. Search for **Storage accounts**.
2. Click **+ Create**.
3. Create a new Resource Group.
4. Enter a unique Storage Account name.
5. Select a suitable region.
6. Select **Standard** performance.
7. Select **Locally-redundant storage (LRS)**.
8. Click **Review** and then **Create**.
9. After deployment is completed, click **Go to resource**.

---

### Step 3: Create a Blob Container

1. Open the Storage Account.
2. Go to **Data storage → Containers**.
3. Click **+ Container**.
4. Enter the container name:

```text
images
```

5. Configure the required access level.
6. Click **Create**.

---

### Step 4: Upload Images

1. Open the `images` container.
2. Click **Upload**.
3. Select 2–3 `.jpg` or `.png` images.
4. Click **Upload**.
5. Verify that the images are displayed in the container.

---

### Step 5: Get the Connection String

1. Open the Storage Account.
2. Go to **Security + networking → Access keys**.
3. Open **key1**.
4. Show the **Connection string**.
5. Copy the connection string.
6. Keep the connection string private.

> **Note:** Never upload your actual Azure connection string or account key to GitHub.

---

### Step 6: Install Required Python Libraries

Open Command Prompt or Terminal and run:

```bash
pip install azure-storage-blob pillow
```

These libraries are required for Azure Blob Storage access and image processing.

---

### Step 7: Create the Python Program

Create a file named:

```text
process_images.py
```

The program performs the following operations:

1. Connects to Azure Blob Storage.
2. Gets the images from the `images` container.
3. Downloads each image.
4. Resizes the image to **300 × 300 pixels**.
5. Converts the image to **grayscale**.
6. Saves the processed image as JPEG.
7. Uploads the processed image back to Azure with the prefix `processed_`.

---

### Step 8: Run the Python Program

Navigate to the folder containing `process_images.py`.

Example:

```bash
cd /d E:\DOWNLOAD
```

Run the program:

```bash
python process_images.py
```

If required, you can also use:

```bash
py process_images.py
```

Expected output:

```text
Processed and uploaded: processed_image1.jpg
Processed and uploaded: processed_image2.jpg
All images processed successfully.
```



---

### Step 9: Verify the Processed Images

1. Open the Azure Portal.
2. Go to **Storage accounts**.
3. Open your Storage Account.
4. Go to **Containers → images**.
5. Click **Refresh**.
6. Check for the processed images.

The output files will be named similar to:

```text
processed_image1.jpg
processed_image2.jpg
```

The processed images can be opened or downloaded to verify that they have been resized and converted to grayscale.

---

## Result

The images were successfully processed using **Python and Azure Blob Storage**.

The original images were downloaded from Azure, resized to **300 × 300 pixels**, converted to **grayscale**, and uploaded back to the Azure Blob Storage container.

## Conclusion

This experiment demonstrates the integration of **Microsoft Azure Blob Storage with Python** for cloud-based image processing.
