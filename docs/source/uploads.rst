######################
Uploads
######################

Not all Exchanges support background transaction synchronization. For a number of those exchanges we've implemented a method of imported files that were exported from their system. 

Once such a file has been created, the file can be uploaded using the 'Uploads' page. After the page is opened, you can see all previously imported files.

======================
Upload new file
======================

To upload a new file; use the 'Upload File(s)' button above the table. This will display the 'Upload File(s)' dialog. 

.. note::

    Before uploading, make sure to create a Exchange Connection for the exchange first, see :doc:`connections`.

First select the Exchange Connection you want to import files for. This can be done using the drop-down interface. Only supported exchanges are listed here.

Some exchanges will need additional properties; these will appear under the selected exchange connection. Follow the instructions when displayed. For example; the Midas file import needs to have an asset selected. 

Last, select the file(s) you want to import. Make sure they belong to the exchange that was selected first. 

After upload, the file is queued for processing and you will be notified through alerts when the import is done. 

======================
Status Model
======================

There are a number of different states an uploaded file can be in. The following items explain the possible states:

* **Queued** - Upload successful, waiting for automatic processing and is queued for our server to start import the file and process transactions inside the file.
* **Syncing** - Background sync is currently being performed.
* **Error** - Some problem occurred during sync, check :doc:`notifications`. Unpause connection and re-upload file to retry.
* **Syncing** - Background sync is currently being performed.
* **Done** - File was imported and transactions processed accordingly.
* **Ignored** - The Exchange Connection is set to 'Ignored', thus import will not continue.

======================
Delete Uploads
======================

You can delete uploaded files when they are not being processed. Use the trash-can icon on the far side of each row in the table to delete individual uploaded files.

You can also use the 'Delete All' button to remove all uploads from our system. Uploaded files are automatically removed 30 days after upload. 