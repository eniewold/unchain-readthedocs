######################
Uploads
######################

Not all Exchanges support background transaction synchronization. For a number of those exchanges we've implemented a method of imported files that were exported from their system. 

Once such a file has been created, the file can be uploaded using the 'Uploads' page. After the page is opened, you can see all previously imported files.

======================
Step 1. Export file
======================

Before you can upload and import a file you will need to export a file containing transaction data from an exchange or wallet. 
Please refer to the appropiate documentation for the available exchanges. 

.. csv-table::
   :file: uploads.csv
   :header: "Name", "Link", "Comments"
   :widths: 20, 20, 20

======================
Step 2. Upload file
======================

.. note::

    Before uploading, make sure have already have created a Exchange Connection, see :doc:`connections`.

First select the Exchange Connection you want to import files for. The available exchange connections are displayed as cards with some details listed.

Some exchanges will need additional properties; these will appear under the selected exchange connection. Follow the instructions when displayed.

Last, select the file(s) you want to import by using the 'Browse' button. Make sure they match the exchange it was exported from.

===========================
Step 3. File processing
===========================

After upload, the file is queued for processing and you will be notified through alerts when the import is done. 

If errors occur during processing you will received details through :doc:`notifications`.

----------------------
Status Model
----------------------

There are a number of different states an uploaded file can be in. The following items explain the possible states:

* **Queued** - Upload successful, waiting for automatic processing and is queued for our server to start import the file and process transactions inside the file.
* **Syncing** - Background sync is currently being performed.
* **Error** - Some problem occurred during sync, check :doc:`notifications`. Unpause connection and re-upload file to retry.
* **Syncing** - Background sync is currently being performed.
* **Done** - File was imported and transactions processed accordingly.
* **Ignored** - The Exchange Connection is set to 'Ignored', thus import will not continue.

----------------------
Delete Uploads
----------------------

You can delete uploaded files when they are not being processed. Use the trash-can icon on the far side of each row in the table to delete individual uploaded files.

You can also use the 'Delete All' button to remove all uploads from our system. Uploaded files are automatically removed 30 days after upload. 